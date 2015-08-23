---
layout: post
title: Connect R to Teradata via JDBC in Windows 7
categories: [howto]
tags: [r, teradata]
published: True

---

I recently had the opportunity to conduct some ad hoc exploration of a large data set. The data was stored in a Teradata environment, and given Teradata's public support of R, I did not expect it to be a problem to connected the two. While Teradata did open source a module to connect R to Teradata, it is no longer supported and does not work out-of-the-box. Teradata's recent work has been limited to expensive enterprise products, so if you want a supportd solution to connect the two, be prepared to pay for a license to Revolution R Enterprise. However, if you are adventuresome, below is how to get the outdated and unsupported teradataR module working:

## Prerequisites:
- Download [teradataR](https://github.com/Teradata/teradataR) to a local path e.g 'C:\teradataR_install'
- Download and install [Teradata Studio Express 15](https://downloads.teradata.com/download/tools/teradata-studio-express) or the most reecnt version
	- Make note the the install location of the files as you will need them in the connection string below:
		- terajdbc4.jar

``` 
C:\\Program Files (x86)\\Teradata\\Client\\15.10\\Teradata Studio Express\\plugins\\com.teradata.datatools.terajdbc_15.10.0.201504291406\\terajdbc4.jar
```
		- tdgssconfig.jar

```
C:\\Program Files (x86)\\Teradata\\Client\\15.10\\Teradata Studio Express\\plugins\\com.teradata.datatools.terajdbc_15.10.0.201504291406\\tdgssconfig.jar
```

- Upgrade your JAVA installation to the latest 64-bit version
- Upgrade your R and R Studio installations and set to 64 bit mode
- RJDBC and others are prerequisites as well, but will be called from code to be installed from CRAN

## Steps in R
- Install teradataR from your local source (yes the double backslashes are necessary):
```r
install.packages("C:\\teradataR_install\\teradataR_1.1.0.tar.gz", repos=NULL,type="source");
```

- Define the host and default database for your connection string, plus user name and password (optional):
```r
	teraHost <- "jdbc:teradata://terdatahost.companydomain.co/TMODE=ANSI,DATABASE=my_default_db_here"
	teraUSR <- "my_user_name_here"
	teraPWD <- "my_password_here"
```

- Connect using the JAR files from the Teradata Studio Express install in the prerequisites, and the host, database, user name, and password from the last step

```r
library(RJDBC)
library(teradataR)
drv = JDBC("com.teradata.jdbc.TeraDriver","C:\\Program Files (x86)\\Teradata\\Client\\15.10\\Teradata Studio Express\\plugins\\com.teradata.datatools.terajdbc_15.10.0.201504291406\\terajdbc4.jar;C:\\Program Files (x86)\\Teradata\\Client\\15.10\\Teradata Studio Express\\plugins\\com.teradata.datatools.terajdbc_15.10.0.201504291406\\tdgssconfig.jar")
con <- dbConnect(drv,teraHost,teraUSR,teraPWD)
rm(teraHostTemp,teraHost,teraUSR,teraPWD)
print("Teradata connection established in variable 'con'")
```

- From here you can use the Teradata source as if it were any other JDBC source

## Other Hints
- I found it very helpful to increase my Java heap size. You can do this with the following command in R, but only the 64-bit version supports memory sizes this large:
```r
	options(java.parameters = "-Xmx2048m")
```

- To close reduce the overhead on the Teradata source, use these commands in R:
```r
# Clears you result from Teradata, assuming your result variable is titled CURRENT_QUERY_RESULT
dbClearResult(CURRENT_QUERY_RESULT)

# Disconnects from Teradata, assuming your connection variable is named con
dbDisconnect(con)
```

**Good luck and happy querying!**

