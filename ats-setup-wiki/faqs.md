This site provides an overview of the most frequently asked questions and their solutions, concerning ATS.

# Table of Contents

* [Internet Explorer 11 ignores proxy settings for http://localhost/](FAQ#internet-explorer-11-ignores-proxy-settings-for-httplocalhost)

## Internet Explorer 11 ignores proxy settings for http://localhost/. How can I fix this?

**Answer:** Internet Explorer will _always ignore_ your proxy settings for **localhost**. Whoever you can add another hostname to the `hosts` file, which leads to **127.0.0.1** (or ::1 for IPv6). Assuming you're using a Microsoft Windows machine, navigate to  `C:\windows\system32\drivers\etc` and edit the 'hosts' file with administrator privileges.
Add the following line to the end of the file, replace <hostname> with the desired hostname: 
```
127.0.0.1 <hostname> 
```
Now you can reach your local machine by entering `<hostname>` as new url. Internet Explorer won't ignore your proxy settings, for this url.