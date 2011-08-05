# iptools

## About

`iptools` is a collection of 3 scripts which are used for doing simple IPv4 address calculations and builds on the wonderful `ipcalc` tool provided by Krischan Jodies. `iptools` does conversions of IP to 32-bit int, 32-bit int to IP and has a tool for telling you whether an IP is inside a subnet.

Before you can use these tools, you must install `ipcalc` first. `ipcalc` can be found at: http://jodies.de/ipcalc

## The Tools

### ip2int

`ip2int` will take a provided IPv4 address (using dotted octet notation) and return it as a 32-bit integer.

Usage:

    ip2int <ip_address>
    
Example:

    $ ./ip2int 10.0.0.1
    167772161

### int2ip

`int2ip` takes a provided 32-bit integer representation of an IPv4 address and returns it in dotted octet notation.

Usage:

    int2ip <ip_address_int>
    
Example:

    $ ./int2ip 167772161
    10.0.0.1
    
### insubnet

`insubnet` is a tool used to figure out whether a given IPv4 address (in dotted octet notation) is in the provided subnet (in CIDR notation). `insubnet` will return 0 if the address is inside the subnet and 1 if not.

Usage:

    insubnet <ip_address> <cidr>
    
Example:

    $ ./insubnet 10.1.1.15 10.1.1.0/24
    10.1.1.15 is inside 10.1.1.0/24
    
Example:

    $ ./insubnet 12.1.1.15 10.1.1.0/24
    12.1.1.15 is NOT inside 10.1.1.0/24
    
## Author

The `iptools` package is written by Spike Grobstein (spikegrobstein@mac.com) and is licensed under the MIT license.

Feel free to modify and re-distribute, but don't forget proper attribution.

http://sadistech.com
http://spike.grobste.in
https://github.com/spikegrobstein