https://releases.hashicorp.com/vault/1.5.3/

https://phoenixnap.com/kb/how-to-install-vault-ubuntu

1. arch
> x86_64

2. yum install wget unzip/ apt-get install wget unzip

3. Using the wget command, download the package by pasting the link location copied in the previous step:
>  wget https://releases.hashicorp.com/vault/1.5.3/vault_1.5.3_linux_amd64.zip

4. Next, unzip the package using the following command:
>unzip vault_1.2.3_linux_amd64.zip

5. Then, move the package to the /usr/bin directory:
> mv vault /usr/bin

6. Check the installation using the following command:
> vault

7. Move binary to right path:
> echo $PATH
> /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin
> mv vault /usr/local/bin
