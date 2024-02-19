
1. start local dfx
```
dfx start --clean
```
2. Run NPM server
```
npm start
```
3. Deploy canisters
```
dfx deploy --argument='()'
```
4. Head to localhost
http://localhost:8080/

# Creating NFT for Testing
1. Mint an NFT on the command line to get NFT into mapOfNFTs:
```
dfx canister call opend mint '()'
```
2. List the item into mapOfListings:
```
dfx canister call opend listItem '(principal "<REPLACE WITH NFT CANISTER ID>", 2)'
```
3. Get OpenD canister ID:
```
dfx canister id opend
```
4. Transfer NFT to OpenD:
```
dfx canister call <REPLACE WITH NFT CANISTER ID> transferOwnership '(principal "<REPLACE WITH OPEND CANISTER ID>", true)'
```
# Conneting to the Token Canister
1. Copy over the token declarations folder
2. Set the token canister id into the <REPLACE WITH TOKEN CANISTER ID>
```
const daasPrincipal = Principal.fromText("<REPLACE WITH TOKEN CANISTER ID>");
```
