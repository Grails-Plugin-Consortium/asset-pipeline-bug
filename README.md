# asset-pipeline-bug

Do a publishMavenPublicationToMavenLocal on the plugin project before running the web project


main.gsp from web project that includes a foo.css from the plugin's assets dir.

```html
<!doctype html>
<html lang="en" class="no-js">
   <head>
       <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
       <meta http-equiv="X-UA-Compatible" content="IE=edge">
       <title><g:layoutTitle default="Grails"/></title>
       <meta name="viewport" content="width=device-width, initial-scale=1">
       <asset:stylesheet src="application.css"/>
       <asset:javascript src="application.js"/>

       <asset:stylesheet src="foo.css"/>

       <g:layoutHead/>
   </head>
   <body>
       <div id="grailsLogo" role="banner"><a href="http://grails.org"><asset:image src="grails_logo.png" alt="Grails"/></a></div>
       <g:layoutBody/>
       <div class="footer" role="contentinfo"></div>
       <div id="spinner" class="spinner" style="display:none;"><g:message code="spinner.alt" default="Loading&hellip;"/></div>
   </body>
</html>
```


![Screen 1](https://raw.githubusercontent.com/Grails-Plugin-Consortium/asset-pipeline-bug/master/ss1.png)
<br />
![Screen 1](https://raw.githubusercontent.com/Grails-Plugin-Consortium/asset-pipeline-bug/master/ss2.png)
<br />
![Screen 1](https://raw.githubusercontent.com/Grails-Plugin-Consortium/asset-pipeline-bug/master/ss3.png)