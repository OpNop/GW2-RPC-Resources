# Guild Wars 2 Discord RPC Resources 
The goal of this repo is to give people looking to add Discord RPC support to their Guild Wars 2 addons a stating point and ability to stay under the 150 RPC assets limit. Instance maps tend to be duplicated maps from the main Public instances, just with a different ID. The method used here is to hash the `continent_rect` from the API and "map" it to the main Public map.

## Format
The format of the file is a standard jsonc file and structured as follows

`"hash": mapid"`

`mapid` can then be mapped to the IMAGE KEY `map_<mapid>` 

## Usage

I tried to use an algorithm that any language could easily reproduce and would be able to use data only contained inside the result of an API query to `https://api.guildwars2.com/v2/maps/<Current Map>`. The hash is the first 8 characters of the SHA1 hash of the following string

`SHA1(<continent_id><continent_rect[0][0]><continent_rect[0][1]><continent_rect[1][0]><continent_rect[1][1]>)`


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## License
[MIT](https://choosealicense.com/licenses/mit/)

## Credits
Original idea and images are from [Freesnöw](https://github.com/dlamkins) and [Blish HUD](https://blishhud.com/)  
Map file by [Tiny Taimi](https://github.com/OpNop) of [The TINY Army](https://tinyarmy.org)