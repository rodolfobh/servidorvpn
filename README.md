# servidorvpn
Instruções para criar um servidor OpenVPN

A) Construtor de CA – Certificado de Autoridade  

Passo 1- Instalar openvpn

$ sudo apt update
$ sudo apt install openvpn

wget - ira trazer a última versão da EasyRSA
$ wget -P ~/ https://github.com/OpenVPN/easy-rsa/releases/download/v3.0.4/EasyRSA-3.0.4.tgz

Desempacote
$ cd ~
$ tar xvf EasyRSA-3.0.4.tgz

Passo 2 - 
# Copiar vars 
$ cd ~/EasyRSA-3.0.4/
$ cp vars.example vars

# Editar vars, atualizar os dados abaixo e retirar a marcação de “# -comentário” das linhas abaixo.
$ nano vars 

#set_var EASYRSA_REQ_COUNTRY    "US"
#set_var EASYRSA_REQ_PROVINCE   "California"
#set_var EASYRSA_REQ_CITY       "San Francisco"
#set_var EASYRSA_REQ_ORG        "Copyleft Certificate Co"
#set_var EASYRSA_REQ_EMAIL      "me@example.net"
#set_var EASYRSA_REQ_OU         "My Organizational Unit"
$ ./easyrsa init-pki
