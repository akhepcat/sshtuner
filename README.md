# sshtuner
overly ugly script to check your ssh client/server support for various encryption algorithms and suggest a 'best practices' configlet

defaults to "modern" practices, but you can add "-legacy" support with a command-line flag.  
(really, any text on the command line forces legacy support right now)

This has not been tested on a wide swath of platforms or ssh versions.  
  7.0 in particular is not represented yet.  
  some "OLD" versions are not well supported, but hardcoded based on manual testing.  Sigh.  
  

    $ ssh-enc-check
    use the '-legacy' flag to include legacy encryption in final configs
    SSH version is 66 (aka 6.6)  
    
    Please wait, testing ciphers...
    Please wait, testing macs...  
    Please wait, testing kexs...
    Please wait, testing hkeys...
    Your ssh(d)_config supports the following more-secure configuration:
    
    Ciphers chacha20-poly1305@openssh.com,aes256-gcm@openssh.com,aes128-gcm@openssh.com,aes256-ctr,aes192-ctr,aes128-ctr
    MACs hmac-sha2-512-etm@openssh.com,hmac-sha2-256-etm@openssh.com,hmac-ripemd160-etm@openssh.com,umac-128-etm@openssh.com,hmac-sha2-512,hmac-sha2-256
    KexAlgorithms curve25519-sha256@libssh.org,diffie-hellman-group-exchange-sha256,diffie-hellman-group-exchange-sha1
    HostKeyAlgorithms ssh-ed25519-cert-v01@openssh.com,ssh-rsa-cert-v01@openssh.com,ssh-rsa-cert-v00@openssh.com,ssh-ed25519
    


