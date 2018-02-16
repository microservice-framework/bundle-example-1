# bundle-example-1

API example with 1 service with secure key authentification only (no oAuth. Example is coming).

- Install mfw-cli
  ```sh
  # npm install @microservice-framework/mfw-cli -g
  ```

- Clone this repo
  ```sh
  # git clone https://github.com/microservice-framework/bundle-example-1.git
  Cloning into 'bundle-example-1'...
  remote: Counting objects: 9, done.
  remote: Compressing objects: 100% (8/8), done.
  remote: Total 9 (delta 1), reused 5 (delta 1), pack-reused 0
  Unpacking objects: 100% (9/9), done.
  # cd bundle-example-1
  ```
  Application folder is a bundle for all your services.
  
- Install all services that a part of this bundle
  ```sh
  # mfw setup
	-	downloading microservice-router
	-	downloading example-3
	-	copiyng example-3 to /Volumes/DATA/gor/bundle-example-1/services/example-3
	-	updating dependencies for example-3
	-	copiyng microservice-router to /Volumes/DATA/gor/bundle-example-1/services/microservice-router
	-	updating dependencies for microservice-router
	[ok]	/Volumes/DATA/gor/bundle-example-1/services created.
	[ok]	/Volumes/DATA/gor/bundle-example-1/logs created.
	[ok]	/Volumes/DATA/gor/bundle-example-1/pids created.
	[ok]	/Volumes/DATA/gor/bundle-example-1/configs created.
	[ok]	github:microservice-framework/example-3 updated.
	[ok]	@microservice-framework/microservice-router updated.
	[war]	/Volumes/DATA/gor/bundle-example-1 already exists.
	[war]	.gitignore already exists
  ```

- start all service
  ```sh
  # mfw start all
	-	starting example-3:start
	-	starting microservice-router:start-admin
	-	starting microservice-router:start-proxy
	[ok]	example-3:start started
	[ok]	microservice-router:start-admin started
	[ok]	microservice-router:start-proxy started
	[war]	failed to read .env file. Creating default one.
  ```

- open [API explorer](http://localhost:3100) via browser
- enter `a55c05d2ba33cef033df9c63b63c28bd52e03ab419393e21` as a access Token
- now you can perform basic CRUD operations via API explorer
