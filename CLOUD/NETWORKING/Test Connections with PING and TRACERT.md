
With the ICMP → Internet Control Message Protocol we can validate the status of a network or service in the internet.


**`PING`**: tests the status of the dns, ip we pass to it and shows information such as the IP addresses, how many bytes it has, time of the request and the TTL.

```shell
ping google.com
```


Keep in mind that the TTL is reduced by one each time it goes for a router.


**`tracert`**: it shows how many hops a request does, showing the status of each router.

```shell
tracert google.com # windows
tracerouter google.com # linux
```


