# Hobo Disc Golf Website

THe live site can be found at https://www.hobodiscgolf.com

## Overview

The Hobo Disc Golf website is developed using the Hugo static code generator, is loosely based on the ???? Hugo theme, and uses tailwindcss. It is deployed to GitHub Pages using github actions workflows defined in this repo.

## Procedures

### Adding a Map to an Article

1. Generate a map image at Snazzy Maps
   1. Navigate to the [Modest theme at Snazzy Maps](https://snazzymaps.com/style/287720/modest)
   1. Enter the address in the search bar (little magnifying glass at top-right of map)
   1. Click the `Download Image` icon towards top-left of map
   1. Keep dimensions at 500px x 500px and scale factor of 1
   1. Click the `Download Image` button
   1. Rename the image to `map-<location>.png` (ook in `static/img/` dir for examples)
   1. Move image to `static/img/` directory
1. Get a Google Maps link for the location
   1. Navigate to google maps
   1. Enter the address in the search bar
   1. Copy the link in the browser bar
1. Add a Hugo googlemaps shortcode to your article
   Usage:
   ```
   googlemaps addr0="Housename" addr1="69 Street Address" addr2="Town followed by postcode 420" img="/path/to/gmaps/screenshot.jpg" url="https://maps.google.com"
   ```
   Example:
   ```
   {{< googlemaps img=/img/map-bayville-park.png addr0="Bayville Park" addr1="4132 First Ct Rd," addr2="Virginia Beach, VA 23455" url="https://www.google.com/maps/place/Bayville+Farms+Disc+Golf+Course/@36.9018639,-76.1212732,18z/data=!4m10!1m2!2m1!1sBayville+farms+Park+disc+golf+-+Virginia+Beach,+Virginia!3m6!1s0x89ba953f04ddd349:0x5ea664d76f48c809!8m2!3d36.9003867!4d-76.1204914!15sCjhCYXl2aWxsZSBmYXJtcyBQYXJrIGRpc2MgZ29sZiAtIFZpcmdpbmlhIEJlYWNoLCBWaXJnaW5pYVo3IjViYXl2aWxsZSBmYXJtcyBwYXJrIGRpc2MgZ29sZiB2aXJnaW5pYSBiZWFjaCB2aXJnaW5pYZIBBHBhcmuaASNDaFpEU1VoTk1HOW5TMFZKUTBGblNVUXljRFpFV0VGbkVBReABAA!16s%2Fg%2F11rccxnj_f" >}}
   ```
