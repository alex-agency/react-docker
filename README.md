alexagency/react-yeoman
==========================

**Dockerfile for [Yeoman](http://yeoman.io/) with [React](https://facebook.github.io/react) generators**

### Installation

Install [Docker Machine](https://docs.docker.com/machine/install-machine/).

Create virtual machine:
```
docker-machine create -d virtualbox dev
```

Get IP address:
```
docker-machine ip dev
```

Connect to virtual machine:
```
docker-machine ssh dev
```

Go to shared (between host and virtualbox) home directory:
```
cd /Users/<MAC USER>
cd /c/Users/<WINDOWS USER>
```

Run **alexagency/react-yeoman** container from [Docker Hub](https://hub.docker.com/r/alexagency/react-yeoman/):
```
docker run -it --rm -p 3000:3000 -p 3001:3001 -v $(pwd)/react:/app alexagency/react-yeoman
```

Initiate one of Yeoman generators:

[React Starter Kit](https://github.com/kriasoft/react-starter-kit):
```
yo react-fullstack
```
[React Static Boilerplate](https://github.com/koistya/react-static-boilerplate):
```
yo react-static
```
[ReactJS and Webpack](https://github.com/newtriks/generator-react-webpack):
```
yo react-webpack
```

Check generated project:
```
/Users/<MAC USER>/react
/c/Users/<WINDOWS USER>/react
```

Install Node.js components:
```
npm install
```

Run unit tests:
```
npm test
```

Compile and launch:
```
npm start
```

Browse to React webapp:

React Starter Kit and React Static Boilerplate:
```
http://<virtual machine ip>:3000/
http://<virtual machine ip>:3001/
```
