#### Description

Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

Additional details will be available after launching your challenge instance.

````
lesly@Lesly:~/anterior$ gzip -d disk.img.gz
lesly@Lesly:~/anterior$ mls disk.img
Command 'mls' not found, but there are 16 similar ones.
lesly@Lesly:~/anterior$ mmls disk.img
DOS Partition Table

lesly@Lesly:~/anterior$ fls disk.img -o 206848
lesly@Lesly:~/anterior$ fls disk.img -o 206848 -r 1 grep ssh
Error stat(ing) image file (raw_open: image "1" - No such file or directory)
lesly@Lesly:~/anterior$ fls disk.img -o 206848 -r | grep ssh
lesly@Lesly:~/anterior$ fls disk.img -o 206848 3916 -r
r/r 2345:       id_ed25519
r/r 2346:       id_ed25519.pub
lesly@Lesly:~/anterior$ icat disk.img -o 206848 2345
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLAAAAJgxpYKDMaWC
gwAAAAtzc2gtZWQyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLA
AAAECItu0F8DIjWxTp+KeMDvX1lQwYtUvP2SfSVOfMOChxYGCtd7hso2E7OQItY6aTjMMy
KZb1FVmeBfnVjyHcGYosAAAADnJvb3RAbG9jYWxob3N0AQIDBAUGBw==
-----END OPENSSH PRIVATE KEY-----
lesly@Lesly:~/anterior$ icat disk.img -o 206848 2345 > key_file
lesly@Lesly:~/anterior$ chmod og-r key_file
lesly@Lesly:~/anterior$ ssh -i key_file -p 52223 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:52223 ([13.59.203.175]:52223)' can't be established.
ED25519 key fingerprint is SHA256:XBSvB1lk28EctsAVdKJtsl0A7C5bonqPrvHCYH8aEy4.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:9: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:52223' (ED25519) to the list of known hosts.
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ cat flag.txt
picoCTF{k3y_5l3u7h_b5066e83}ctf-player@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
lesly@Lesly:~/anterior$
```