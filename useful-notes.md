## TTL - Time-to-live
Time-to-live (TTL) is a value for the period of time that a packet, or data, should exist on a computer or network before being discarded.

By pinging a target, can use this to ascertain whether a it's running Windows, Linux or is a piece of networking hardware.

```bash:
┌──(kali㉿kali)-[~]
└─$ ping 10.10.10.10
```

### Windows
In output, if ttl=64 to ttl=127 - this is a windows machine.
```bash:
┌──(kali㉿kali)-[~]
└─$ ping 10.10.10.10
  PING 10.10.10.10 (10.10.10.10) 56(84) bytes of data.
  64 bytes from 10.10.10.10: icmp_seq=1 ttl=127 time=11.3 ms
  64 bytes from 10.10.10.10: icmp_seq=2 ttl=127 time=10.4 ms
  64 bytes from 10.10.10.10: icmp_seq=3 ttl=127 time=14.5 ms
  64 bytes from 10.10.10.10: icmp_seq=4 ttl=127 time=10.3 ms
  64 bytes from 10.10.10.10: icmp_seq=5 ttl=127 time=11.4 ms
```
As one can see in the above.

Else, if ttl=128 or greater, it's likely networking hardware such as a switch.
And if ttl=63 or less, it's likely a linux machine.
