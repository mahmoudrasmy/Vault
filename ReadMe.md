# Vault

## Installation Steps
- $curl -O https://releases.hashicorp.com/vault/0.6.2/vault_0.6.2_linux_amd64.zip
- $sudo apt-get install unzip
- $apt-get install unzip
- $unzip vault_0.6.2_linux_amd64.zip
- $mv vault /usr/local/bin

## Working with Vault
- $export VAULT_DEV_LISTEN_ADDRESS='0.0.0.0:8200'   ==> to customize the server address 
- $vault server -dev    ==> to start the server address

## Starting the server with specific config
- $vault server -dev -config='config.json'
- in the config 
```
listener "tcp" {
  address     = "0.0.0.0:8200"
  tls_disable = 1
}
```
-To start the server using specific config
  $vault server -dev -dev-listen-address="0.0.0.0:8200"
- $vault init
- $vault write secret/hello foo=world
