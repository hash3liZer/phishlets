# Phishlets
Phishlets are the configuration files in **YAML** syntax for proxying a legitimate website into a phishing website. They are the building blocks of the tool named `evilginx2`. https://github.com/kgretzky/evilginx2. 

## Blockchain
The phishlet `blockchain.yaml` for blockchain.com is somewhat different from the phishlets as can be seen on the orignal repo of `evilginx2`. Blockchain.com is heavily built on the javascript containing millions of lines of code and instead of maintaining sessions, the data is obfuscated and stored within the **DOM** as long as the user is logged in. So, we can't track cookies yet. Another problem here is the blockchain.com site never sends plain text over the wire. So, i used javascript to keep record the credentials. Hope it will work out. 

There was a small problem in one of the core files of evilginx2, you have to fix before using this phishlet. Edit the line `475` in `evilginx2/core/http_proxy.go`:
```
if (allow_origin == "" || allow_origin != "") {
    ....
}
```
Save the file and rebuild from the source code. Then you can use the blockchain phishlet. 

## Admin Booking
The phishlet `booking.yaml` is just like other commonly used phishlets. Upload it anad use it. However, note that this phishlet is for `admin.booking.com` not `booking.com`

## Contact
Twitter - @hash3liZer<br>
Email   - admin@shellvoide.com
