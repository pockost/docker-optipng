# Usage

## One file optimization

You have to mount image folder to optimized into /app directory. Example :

  docker run --rm -v "$( pwd ):/app" pockost/optipng -o2 images/*.png

## Get help

If you run the container without any option help will be show.

  docker run --rm pockost/optipng

## Multiple file optimization

You can also pipe the result of a find command

docker run --rm -v "$( pwd ):/app" -w /app alpine find -iname '*.png' -o -iname '*.bmp' -o -iname '*.gif' -o -iname '*.png' -o -iname '*.tiff' |  xargs docker run --rm -v "$( pwd ):/app" pockost/optipng

# User feedback

If you have any problems with or questions about this Docker image, please contact us through a Github issue.
