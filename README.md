# R1,R2,R3 e R4

enable
configure terminal
hostname R1
banner motd "ACESSO APENAS PARA PESSOAS AUTORIZADAS"
enable secret SenhaEnable
ip domain-name peachanddaisy.local
crypto key generate rsa general-keys modulus 1024
line vty 0 15
password SenhadaVTY
login
transport input ssh
exec-timeout 10
exit
username ruthbraga privilege 15 secret Batata
username estagiario privilege 1 secret senha
line console 0
password SenhadaConsole
login
exit
service password-encryption
interface serial 0/0/1
ip address 201.187.89.4 255.255.255.252
no shutdown
exit
interface serial 0/1/1
ip address 201.187.89.0 255.255.255.252
no shutdown
interface serial 0/0/0
ip address 201.187.89.20 255.255.255.252
no shutdown
int g0/1
ip address 192.168.0.0 255.255.224.0
no shutdown
ip default-gateway 192.168.0.1
R2
enable
configure terminal
hostname R2
banner motd "ACESSO APENAS PARA PESSOAS AUTORIZADAS"
enable secret SenhaEnable
ip domain-name peachanddaisy.local
crypto key generate rsa general-keys modulus 1024
line vty 0 15
password SenhadaVTY
login
transport input ssh
exec-timeout 10
exit
username ruthbraga privilege 15 secret Batata
username estagiario privilege 1 secret senha
line console 0
password SenhadaConsole
login
exit
service password-encryption
interface serial 0/0/1
ip address 201.187.89.4 255.255.255.252
no shutdown
exit
interface serial 0/0/0
ip address 201.187.89.16 255.255.255.252
no shutdown
exit
interface serial 0/1/1
ip address 201.187.89.8 255.255.255.252
no shutdown
int g0/1
ip address 10.0.0.0 255.0.0.0
no shutdown
ip default-gateway 10.0.0.1

R2
enable
configure terminal
hostname R2
banner motd "ACESSO APENAS PARA PESSOAS AUTORIZADAS"
enable secret SenhaEnable
ip domain-name peachanddaisy.local
crypto key generate rsa general-keys modulus 1024
line vty 0 15
password SenhadaVTY
login
transport input ssh
exec-timeout 10
exit
username ruthbraga privilege 15 secret Batata
username estagiario privilege 1 secret senha
line console 0
password SenhadaConsole
login
exit
service password-encryption
interface serial 0/0/1
ip address 201.187.89.4 255.255.255.252
no shutdown
exit
interface serial 0/0/0
ip address 201.187.89.16 255.255.255.252
no shutdown
exit
interface serial 0/1/1
ip address 201.187.89.8 255.255.255.252
no shutdown
int g0/1
ip address 10.0.0.0 255.0.0.0
no shutdown
ip default-gateway 10.0.0.1

R3
enable
configure terminal
hostname R3
banner motd "ACESSO APENAS PARA PESSOAS AUTORIZADAS"
enable secret SenhaEnable
ip domain-name peachanddaisy.local
crypto key generate rsa general-keys modulus 1024
line vty 0 15
password SenhadaVTY
login
transport input ssh
exec-timeout 10
exit
username ruthbraga privilege 15 secret Batata
username estagiario privilege 1 secret senha
line console 0
password SenhadaConsole
login
exit
service password-encryption
interface serial 0/0/0
ip address 201.187.89.20 255.255.255.252
no shutdown
exit
interface serial 0/1/1
ip address 201.187.89.8 255.255.255.252
no shutdown
exit
interface serial 0/0/1
ip address 201.187.89.12 255.255.255.252
no shutdown
int g0/1
ip address 192.168.32.0 255.255.248.0
no shutdown
ip default-gateway 192.168.32.1

R4
enable
configure terminal
hostname R4
banner motd "ACESSO APENAS PARA PESSOAS AUTORIZADAS"
enable secret SenhaEnable
ip domain-name peachanddaisy.local
crypto key generate rsa general-keys modulus 1024
line vty 0 15
password SenhadaVTY
login
transport input ssh
exec-timeout 10
exit
username ruthbraga privilege 15 secret Batata
username estagiario privilege 1 secret senha
line console 0
password SenhadaConsole
login
exit
service password-encryption
interface serial 0/1/1
ip address 201.187.89.0 255.255.255.252
no shutdown
exit
interface serial 0/0/0
ip address 201.187.89.16 255.255.255.252
no shutdown
exit
interface serial 0/0/1
ip address 201.187.89.12 255.255.255.252
no shutdown
int g0/1
ip address 172.16.0.0 255.240.0.0
no shutdown
ip default-gateway 172.16.0.1
