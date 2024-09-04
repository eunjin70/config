# config
spring config test

# config-files
The HTTP service has resources in the following form:
- {application}, which maps to spring.application.name on the client side.
- {profile}, which maps to spring.profiles.active on the client (comma-separated list).
- {label}, which is a server side feature labelling a "versioned" set of config files.

/{application}/{profile}[/{label}]<br/>
/{application}-{profile}.yml<br/>
/{label}/{application}-{profile}.yml<br/>
/{application}-{profile}.properties<br/>
/{label}/{application}-{profile}.properties<br/>

For example:

curl localhost:8888/foo/development<br/>
curl localhost:8888/foo/development/master<br/>
curl localhost:8888/foo/development,db/master<br/>
curl localhost:8888/foo-development.yml<br/>
curl localhost:8888/foo-db.properties<br/>
curl localhost:8888/master/foo-db.properties<br/>


* Config Samples
  - configclient-test.properties
  - configclient-test2.yml
      
* Development
  - app-dev.yml
  
* Testing
  - app-test.yml

* Production
  - app-prd.yml

