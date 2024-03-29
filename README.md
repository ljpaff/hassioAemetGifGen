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


Add this lines to automation.yaml
```
- id: <automation.id>
  alias: Generate AEMET image
  trigger:
  - minutes: /10
    platform: time_pattern
  condition: []
  action:
  - service: shell_command.aemet_rain_image
```
And add a new shell_command to your home assistant

````
aemet_rain_image: /bin/bash /<installation-dir>/generateGif.sh -o <directory to save image>
````


### Execution

```
generateGif.sh [-h] [-c province] [-d dir] -o output_dir -- program for generating GIF from AEMET Rain Radar images

where:
    -h  show this help text
    -c  set province value (default: Madrid)
    -d  set temporary directory to download images (default: /tmp/img)
    -o  set output full path

provinces:
        am Almería
        sa Asturias
        ba Barcelona
        cc Cáceres
        pm Illes Balears
        ca Las Palmas
        ma Madrid
        ml Málaga
        mu Murcia
        vd Palencia
        se Sevilla
        va Valencia
        ss Vizcaya
        za Zaragoza

```

### Example

![radar-rain](examples/radar_rain.gif)


License
----

GNU


**Free Software, Hell Yeah!**
