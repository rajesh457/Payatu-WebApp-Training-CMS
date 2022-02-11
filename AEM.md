Adobe Experience Manager (AEM) is a legacy CMS used to manage content and web-applications at a large scale.
This brings about the existence of Access Control Issues, wherein proper filters are not enforced, leading to potential attackers accessing them to perform a given function.

# AEM security checklist
https://experienceleague.adobe.com/docs/experience-manager-64/administering/security/security-checklist.html?lang=en

# Blog to learn AEM
https://aem4beginner.blogspot.com/

# AEM QueryBuilder
AEM query builder is a tool/framework developed by adobe for writing simple and efficient queries in AEM. Providing anonymous user access to Querybuilder API lets any attacker enumerate internal nodes(viz files and folders) by supplying different JCR SQL queries.

https://www.example.com/bin///querybuilder.json.css?path=/etc&p.limit=-1

The Querybuilder documentation here https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/querybuilder-api.html, lists other queries that can be further used to disclose internal secrets, passwords, etc


# AEM GQL Search servlet 
GQL is a simple fulltext query language, which supports field prefixes similar to Lucene or Google queries.
GQL basically consists of a list of query terms that are optionally prefixed with a property name. E.g.: title:jackrabbit. When a property prefix is omitted, GQL will perform a fulltext search on all indexed properties of a node. There are a number of pseudo properties that have special meaning:


#### Payload Breakdown:
https://<DOMAIN>bin/wcm/search/gql.json/<DISPATCHER-BYPASS>?query=path:/<NODE-NAME>%20<ITEM-TYPE>%20limit:...<QUERY-LIMIT>&pathPrefix=&p.ico

#### Test
  https://example.com/bin/wcm/search/gql.json/TRt.css?query=path:/etc%20type:file%20limit:...1&pathPrefix=&p.ico
  
  
# AEM Metadata Servlet XSS
  https://labs.f-secure.com/blog/securing-aem-with-dispatcher/
  
 # Remote code Execution (RCE)
https://medium.com/@SecTech/adobe-experience-manager-exploitation-24bd9eb75ed9  
  
  
# Tools and resources

  ## Open source tool
  https://github.com/0ang3el/aem-hacker
  
  ## Youtube
  https://www.youtube.com/watch?v=EQNBQCQMouk&ab_channel=Bugcrowd
  
  ## Slides
https://speakerdeck.com/0ang3el/hunting-for-security-bugs-in-aem-webapps
  

  ## Writeups
  * https://medium.com/@vsr061/adobe-experience-manager-security-issues-9b5bd24e0eb0
  * https://medium.com/@byq/how-to-get-rce-on-aem-instance-without-java-knowledge-a995ceab0a83
