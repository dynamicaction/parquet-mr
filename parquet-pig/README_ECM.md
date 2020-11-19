cd ~/git/parquet-mr/parquet-pig

mvn jar:jar
mvn source:jar

mvn install:install-file -DpomFile=pom.xml -Dversion=1.11.0-ecm -Dsource=target/parquet-pig-1.11.0-sources.jar -Dfile=target/parquet-pig-1.11.0.jar

mvn deploy:deploy-file -DpomFile=pom.xml -Dversion=1.11.0-ecm -Dsource=target/parquet-pig-1.11.0-sources.jar -Dfile=target/parquet-pig-1.11.0.jar -DrepositoryId=itrader-internal -Durl=http://build1.dev1.dynamicaction.com:8081/archiva/repository/internal/


