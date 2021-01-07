1. Create a configuration file:
> Outside of Dev mode, Vault server are configured using a file:
> The Format of the file is either in HCL or JSON:

***************************************************************************************************************
                                         Vault Configuration
***************************************************************************************************************
# Link: https://www.vaultproject.io/docs/configuration
# VSCode: HCL marketplace

1. Start by creating a configuration directory and a file within it:
> vim/nano /etc/vault/config.hcl

2. Then, type or paste the following content in the file:

# Note: storage can be file, s3, consul etc.

storage “consul” {
address = “127.0.0.1:8500”
path = “vault/” 
} # where exactly i want to store data(S3, consul, sql, file etc)

listener “tcp” {
address = ”IP.ADDRESS.OF.SERVER” [or “0.0.0.0” to listen to everything]
tls_disable = 1 # for prod this is not required
}
ui = true


vault server --config prod.hcl

vault status

export VAULT_ADDR='http://127.0.0.1:8200' 


vault operator init
Unseal Key 1: fmlGu2X6S21XW0mtAxKBvWBEebiAl8tq3nkvaayWRpot
Unseal Key 2: W2CnQLnGOEn3TQgnhFZWRBzgOHmk9FpvvDlaetRqSja8
Unseal Key 3: AAJWXdmzr2zlRAbyWIQGMtJ5r7yhA2VHoqy4nyzn7tbH
Unseal Key 4: Uu4vhkhfr9gA4Sor4tolgPf/dfCOmu4pY7YUEzeYyNBR
Unseal Key 5: B5XGc/0DUTyY1czAX+sDtSXV+f6JtBSiRQiz7+F9dHhJ

Initial Root Token: s.f7VzuiQnHbaL09J0F9eVwzCL

vault operator unseal

vault login 
