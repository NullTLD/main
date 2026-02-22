# How to start with .null domain?

You need to install the Certificate Authority file for the **.null** domain in your browser.

## Download Certificate Authority file

https://raw.githubusercontent.com/NullTLD/main/refs/heads/main/null.ca.crt
   
## Import the certificate to your browser

### Chrome 

![Chrome Certificte Manager](https://raw.githubusercontent.com/NullTLD/main/refs/heads/main/images/screenshots/certificate-manager.png)

1. Go to  User Certificates `chrome://certificate-manager/localcerts/usercerts`
2. In "Trusted Certificates" click "Import"
3. Upload `null.ca.crt` file 

### Firefox

1. Go to Privacy Settings `about:preferences#privacy`
2. In **Security** section and **Certificates** subsection click on "Show certificates..."
3. Click "Import..." button
4. Upload `null.ca.crt` file 
   
## Add a new DNS server for the **.null** domain in your Network Settings

### macOS

Add file `/etc/resolver/null` with the following content:

```text
nameserver 172.238.112.142
port 53
```

### Verify the imported Certificate Authority and Network Settings by going to https://gov.null

This should open up the website correctly.
