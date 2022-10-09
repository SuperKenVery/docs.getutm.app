---
layout: default
title: Rosetta
parent: Advanced
---
{: .label .label-yellow }
**WIP**

Rosetta feature will be documented here.

To install `rosetta`, 
```shell
% mkdir /tmp/mountpoint
% sudo mount -t virtiofs rosetta /tmp/mountpoint
% ls /tmp/mountpoint rosetta
% sudo /usr/sbin/update-binfmts --install rosetta /tmp/mountpoint/rosetta \
    --magic "\x7fELF\x02\x01\x01\x00\x00\x00\x00\x00\x00\x00\x00\x00\x02\x00\x3e\x00" \
    --mask "\xff\xff\xff\xff\xff\xfe\xfe\x00\xff\xff\xff\xff\xff\xff\xff\xff\xfe\xff\xff\xff" \
    --credentials yes --preserve no --fix-binary yes
```

To enable amd64 in `dpkg`, 
```shell
sudo dpkg --add-architecture amd64
```

Then, 
```shell
sudo apt update
```
