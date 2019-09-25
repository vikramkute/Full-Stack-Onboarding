## Setup PROXY

A proxy server, also known as a "proxy" or "application-level gateway", is a computer that acts as a gateway between a local network (for example, all the computers at one company or in one building) and a larger-scale network such as the internet. Proxy servers provide increased performance and security. In some cases, they monitor employees' use of outside resources.

A proxy server works by intercepting connections between sender and receiver. All incoming data enters through one port and is forwarded to the rest of the network via another port. By blocking direct access between two networks, proxy servers make it much more difficult for hackers to get internal addresses and details of a private network.

You browser already has proxy setup for it, therefore you can easily download any secure content like packages and GIT code from internet. but when you tools like npm or git try to download any content from internet then you may get into proxy errors.

To overcome any proxy errors you can setup a proxy for that specific tool or a global proxy in your environment variables.

---

Example of Proxy:

User name: `cag\t4318vk`

Password: `abc@123` (Note that if password has @ then replace it with equivalent url encoding. i.e. `%40`. All special characters has to be replaced with equivalent url encoding)

Reference: https://www.w3schools.com/tags/ref_urlencode.asp

For above username and password, **proxy** would be:
`http://abcxyz:abc%40123@proxy.company.com:8080/`

---


`<USERNAME>` is your windows username.

`<PASSWORD>` is your windows password.


The best way of setup proxy for your system is to create following environment variables for your account because most of the tools and language implementations like python read proxy settings from system's environment variables

1. Got to Start > Environment variables for your account
2. Under `User variables for <USERNAME>` click new

```
    Variable name: HTTP_PROXY
    Variable value: http://<USERNAME>:<PASSWORD>@proxy.company.com:<PORT>/
```

3. Click `OK`
4. Again click new 

```
    Variable name: HTTPS_PROXY
    Variable value: http://<USERNAME>:<PASSWORD>@proxy.company.com:<PORT>/
```

5. Click `OK`

If still your tool like npm, git is unable to download any content from internet then you can set up a proxy for that particular account.

Run following commands through command line to set proxy for GIT:
```
git config --global http.proxy http://<USERNAME>:<PASSWORD>@proxy.company.com:<PORT>/
git config --global https.proxy http://<USERNAME>:<PASSWORD>@proxy.company.com:<PORT>/
```

Run following commands through command line to set proxy for NPM:
```
npm config set http-proxy http://<USERNAME>:<PASSWORD>@proxy.company.com:<PORT>/
npm config set https-proxy http://<USERNAME>:<PASSWORD>@proxy.company.com:<PORT>/
```

You can use following link to bypass proxy for any other tool which uses internet to download any packages.

```
http://<USERNAME>:<PASSWORD>@proxy.company.com:<PORT>/
```

