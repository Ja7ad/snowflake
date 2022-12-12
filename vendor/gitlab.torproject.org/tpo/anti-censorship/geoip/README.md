# geoip go library

Get the country code for an IP address using the tor's geoip database.

### example

Needs the path of the geoip database in the initialization. For example in
debian it is provided by `tor-geoipdb` and the path is `/usr/share/tor/geoip`
and `/usr/share/tor/geoip6`.

```go
geo, err := geoip.New("/usr/share/tor/geoip", "/usr/share/tor/geoip6")
if err != nil {
	// Handle error
}

ip := net.ParseIP("12.13.14.15")
country, ok := geo.GetCountryByAddr(ip)
if !ok {
	fmt.Println("Not found any country for the IP")
} else {
	fmt.Println("The ip corresponds to the country:", country)
}
```
