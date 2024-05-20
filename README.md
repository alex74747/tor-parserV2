## Tor Consensus and Server Descriptor Parser

This is the version of the script that formats the data in a way that it is compatible with [Torflow](https://github.com/unchartedsoftware/torflow)

Script that parses Tor consensuses and server descriptors to create csv files
that can be used for Tor visualization data.

`parse.py` is for Python 3.3+

The generated CSV files are written in the `data/` directory (created if non
existent).

Example:

    $ python3 parse.py 2010 07 09
    > Only July 9th, 2010 will be processed.

    $ python3 parse.py 2010 08
    > August of 2010 will be processed.

    $ python3 parse.py 2010
    > All 2010 will be processed.

## Note

Decompression seems slower going through python, maybe a packet change could be beneficial?

## Requirements

    - Maxmind GeoIP2 city database in binary format (GeoLite2-City.mmdb).
      https://dev.maxmind.com/geoip/geolite2-free-geolocation-data

    - geoip2
    	$ pip install geoip2

    - tarfile (Only for parse3.py)
    	$ pip install tarfile

    - Stem library - https://stem.torproject.org/
    	$ pip install stem
