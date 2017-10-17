## docker-nginx-static-spa

A simple nginx container that serves Single Page Applications:
- Redirects all requests to the `index.html` file
- Assets compression using `gzip` in stylesheets and javascript files.

[Docker Hub](https://hub.docker.com/r/iamfreee/docker-nginx-static-spa/)

Very small size: ~7 MB (alpine based). Uses about 2 MB RAM when running.

## Instructions

**Dockerfile:**
```
FROM iamfreee/docker-nginx-static-spa:latest
COPY /dist /var/www/html
```

In the example above, the production build of the app is in the local `dist` folder and is moved to the default nginx serve path to be served.

## License
MIT
