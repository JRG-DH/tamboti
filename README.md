# NOTE
For the latest and greatest in Tamboti development please visit [https://github.com/exc-asia-and-europe/tamboti/]( https://github.com/exc-asia-and-europe/tamboti/)

This fork is no longer maintained. 

### Notes for Developers - 

Icon stock is from - [http://www.famfamfam.com/lab/icons/silk/](http://www.famfamfam.com/lab/icons/silk/)

To install:

cd into the tamboti directory and call ant; a file, `tamboti-X.XX.xar`, is created.

log in as admin to eXist, go to the Package Reposistory, choose `tamboti-X.XX.xar` and upload it.

click "Install" and access tamboti at `<http://localhost:8080/exist/apps/library/>` or `<http://localhost:8080/exist/apps/tamboti/>`.

Note that in `$EXIST_HOME/webapp/WEB-INF/controller-config.xml`, the following mappings have to be set

```xml
  <root pattern="/apps/library" path="xmldb:exist:///db/tamboti"/>
  <root pattern="/apps/tamboti" path="xmldb:exist:///db/tamboti"/>
```  

before
``` 
  <root pattern="/apps" path="xmldb:exist:///db"/>
```  
  To build with maven 3.1.1+:
  For user test instance of tamboti, use `clean package -Puser-test-build`.
  For general (stable) test instance of tamboti, use `clean package -Pgeneral-test-build`.
  For production instance of tamboti, use `clean package -Pproduction-build`.
