# hassioAemetGifGen

 hassioAemetGifGen is a script that generates from the radar images of the Spanish weather agency (AEMET) a GIF file to display in Home Assistant.

# New Features!

  - Select province you want to generate.
  - Select directory in which saves the file generated.

### Installation

hassioAemetGifGen requires [imagemagick](https://imagemagick.org/index.php) to run.

Install imagemagick.

```sh
$ sudo apt-get install imagemagick
```

Copy generateGif.sh in your desire directory...


Create a cron that fires uo every 10 minutes
```sh
$ sudo crontab -e
```

````
*/10 * * * * /<install-dir>/generateGif.sh <properties>
````


License
----

GNU


**Free Software, Hell Yeah!**
