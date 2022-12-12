# Snowflake Module

Snowflake is tor client module

## How to use?

- download snowflake from [Release Page](https://githu.com/Ja7ad/snowflake/releases)
- create directory snowflake in opt `mkdir -p /opt/snowflake/client`
- copy snowflake file into /opt/snowflake `cp snowflake /opt/snowflake/client`
- edit `torrc` file and bridge :

```editorconfig
UseBridges 1

ClientTransportPlugin snowflake exec /opt/snowflake/client/snowflake

Bridge snowflake 192.0.2.3:1 url=https://snowflake-broker.torproject.net.global.prod.fastly.net/ front=cdn.sstatic.net ice=stun:stun.voip.blackberry.com:3478,stun:stun.altar.com.pl:3478,stun:stun.antisip.com:3478,stun:stun.bluesip.net:3478,stun:stun.dus.net:3478,stun:stun.epygi.com:3478,stun:stun.sonetel.com:3478,stun:stun.sonetel.net:3478,stun:stun.stunprotocol.org:3478,stun:stun.uls.co.za:3478,stun:stun.voipgate.com:3478,stun:stun.voys.nl:3478
```