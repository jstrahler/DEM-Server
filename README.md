# Elevation-Data-Server
Repository for the backend request handling of elevation data for the BRIDGES project

The elevation data server for BRIDGES takes in a bounding box and returns an ArcGIS ascii grid formatted set of elevation values. This server is powered by the [NOAA Grid Extraction tool](https://www.ngdc.noaa.gov/mgg/global/) and uses the ETOPO1 elevation map with a resolution of 1 arc minute.

## Making Requests
The structure for making elevation data requests is as followed (using this will use the default resoultion values of 1 arc min or .0166)
```html
https://cci-bridges-elevation-t.uncc.edu/elevation?minLon=6.0205581&minLat=46.10757&maxLon=9.707863&maxLat=47.77059
```



### The resolution of a map is what each incriment will be on the x and y axis. 

To use your own density values format it like
```html
https://cci-bridges-elevation.uncc.edu/elevation?minLon=6.0205581&minLat=46.10757&maxLon=9.707863&maxLat=47.77059&resX=.01&resY=.01
```

## Running this Server
### Python Library Requirements
    - flask
    - wget

### Launching the Server
From the servers main directory run the command
```bash
python run
```


