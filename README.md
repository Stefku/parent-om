#parent-pom [![Build Status](https://travis-ci.org/Stefku/parent-pom.svg?branch=master)](https://travis-ci.org/Stefku/parent-pom)

Parent pom to fullfill requirements to publish to maven Central Repository.

http://central.sonatype.org/pages/apache-maven.html

# Prerequisits

To be able to upload to Central Repository you must

## 1. gpg installed and setup a key pair
[http://central.sonatype.org/pages/working-with-pgp-signatures.html](http://central.sonatype.org/pages/working-with-pgp-signatures.html)
## 2. Authentication for ossrh in settings.xml
```
<settings>
	<servers>
		<server>
			<id>ossrh</id>
			<username>your-jira-id</username>
			<password>your-jira-pwd</password>
		</server>
	</servers>
</settings>
```

# Release
```
mvn release:clean release:prepare
mvn release:perform
```
