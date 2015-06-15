---
layout: post
title:  "AEM archetype"
date:   2015-06-15 10:05:59
categories: AEM6, Java8
---

In order to create a project to work with in AEM, use an [AEM archetype][create-archetype].

In the terminal paste below: (Note you can change any of the specifics like cssID and packageGroup, but do not change archetypeRepository, archetypeGroupId, archetypeArtifactId, or archetypeVersion)

~~~~~~

mvn archetype:generate \
    -DarchetypeRepository=https://repo.adobe.com/nexus/content/groups/public/ \
    -DarchetypeGroupId=com.adobe.granite.archetypes \
    -DarchetypeArtifactId=aem-project-archetype \
    -DarchetypeVersion=10 \
    -DgroupId=my-group-id \
    -DartifactId=myproject \
    -Dversion=1.0-SNAPSHOT \
    -Dpackage=com.mycompany.myproject \
    -DappsFolderName=myproject \
    -DartifactName="My Project" \
    -DcqVersion="6.1.0" \
    -DpackageGroup="My Company" \
    -DcontentFolderName="mycontent" \
    -DcssId="mycssId" \
    -DcomponentGroupName="mycomponents" \
    -DsiteName="mysite"

~~~~~~
Press Enter/Return 

Press "Y" when asked.  Now you have a project ready for AEM 6 and Java 8.

Download this code as a [bash file][aem-archetype-aem-6]

Check out the [6dlabs][6dlabs] for more info on AEM.

[6dlabs]:      http://labs.sixdimensions.com/
[aem-archetype-aem-6]: https://gist.github.com/kuckmc01/9616256f551bd6b5b535
[create-archetype]: http://maven.apache.org/guides/mini/guide-creating-archetypes.html