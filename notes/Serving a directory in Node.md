# Serving a directory in Node
Sometimes things just work better when they're served by a web server over http: instead of being opened locally as file:. For those moments, Node can run a very simple web server.

```
// Install via shell
npm install http-server -g

// Serve a directory
http-server

// Serve a directory at a specified port
http-server -p 2020
```

(via [David Walsh](https://davidwalsh.name/serve-directory-nodejs))

#node