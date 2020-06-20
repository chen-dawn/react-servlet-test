# React Frontend with Java Servlet Backend
## Create React App
```
npx create-react-app frontend
brew install yarn
```

## Config React project
```
yarn add google-cloud
yarn add stable
yarn add serve
```
also add `app.yaml` and update `scripts`,`engines` sections in `package.json`.

## Run locally
```
// From frontend directory
yarn local
// From backend directory
mvn appengine:devserver
```

## Deploy to gcloud
```
gcloud init
gcloud config set project [Project_ID]
yarn build // From frontend directory
gcloud app deploy // From frontend directory
mvn package appengine:deploy // From backend directory
gcloud app deploy dispatch.yaml // Config routing
```

## Change node version
```
node -v // Check node version
sudo npm install -g n
sudo n 10.21.0  // Change node version to 10.21.0

```