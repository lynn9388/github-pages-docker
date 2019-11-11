# github-pages-docker

Docker image for running GitHub Pages. More specifically, this image is created to run [light-blog](https://github.com/lynn9388/light-blog) or any site that uses it as a remote theme.

## Build from Dockerfile

You can use the following command to build a new release with tag. (Replace `USERNAME` and `VERSION` as appropriate).

```sh
docker build -t USERNAME/github-pages-docker:VERSION .
```

like

```sh
docker build -t lynn9388/github-pages-docker .
```

## Use the image

Execute the following command in the root directory of your site

```sh
docker run --rm -p 4000:4000 -v $(pwd):/site lynn9388/github-pages-docker
```

You may need to delete the `Gemfile.lock` file of your site.
