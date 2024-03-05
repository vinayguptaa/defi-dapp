#1. Creation of new coins

For the running of our application, we needed basically two cryptocurrencies which would allow the user to make transactions on the network. So in our app there were two main parties :-
The bank itself (or the deployer)
The other users which interact with the bank.
To make the process of finance possible, we made the cryptocurrencies mDAI (mockDAI) and DAPP.

MDAI CREATION

![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/da56f2f3-76a3-4280-940c-f0e1fab8d6a5)
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/346cd2b2-b759-41da-afaa-f12b59d390bb)

DAPP CREATION
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/d83cca1d-b796-4f1f-8875-143e6e9c1760)
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/5b88ae0f-d6cd-412a-b9ab-6780ca7f87ba)

#2. Configuring the data
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/c2322ceb-23ee-49a3-b93f-d99e091a0e9e)
Here we import all the modules (or simply solidity contracts) into a file and deploy them. Then we liquidate all the 1 million DAPP coins created to the deployer of the contract (or simply the bank). Also, to the first address of the users, we transfer 100 mDAI. According to the rules of our application, a user will stake some of his mDAI coins and will get reward from the bank in form of DAPP coins.

#3. Making migrations
Now we need to run the command for the deletion of any of the previously deployed version of the contract and this can be done by the help of :
npx truffle migrate –reset
The results of this command are as follows:
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/74abfb6e-8553-49da-9373-f634325d8089)
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/b587a859-c35a-4d51-9ae6-aad3569dcf77)
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/f2e372d5-fd08-4ee9-9e24-f05b78ab205f)

#4. Starting the server
In order to start the react app on the localhost server, we need to run the following command:
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/af6081f2-eb74-44f0-8cfe-f74d41e6fb19)
which gives the ouput as follows:
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/7a18af4e-d72f-4aef-b6fe-eb6bf022440c)

#5. Setting Up MetaMask with Ganache
Open your metamask and go to the import account section
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/7fd99cf0-cefc-4ad1-b574-9d0de1845841)
Now open Ganache and paste the key on the second index as first one is the deployer

![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/43826507-08e6-4272-9d49-f622b02747a1)

The front page will show:
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/b7cf3afd-bcd1-4fe1-a3b0-e8d192efb132)
Current the user has 0 DAPP and 100 mDAI.

#6. Staking of coins
The user can now stake the coins. Suppose the user stakes 20 mDAI.
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/c4301b99-7237-458b-a7c9-31bc294175ed)

After staking, this function will run:
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/c0c6a465-4b8a-4d3d-9c6f-d660d6972487)

Now we will have to allow the user to take part in transaction by once confirming identity and second for stake for coins :
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/fda90df5-f910-409c-89a5-04861bfc0e2b)
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/a48f34d5-853f-4a6f-bd64-641873fbf6d7)

#7. Issuing of tokens
To issue token in form of DAPP, the deployer can run this script anytime he wants. The user will be given equal number of DAPP according to the amount of mDAI stacked:
<img width="299" alt="image" src="https://github.com/vinayguptaa/defi-dapp/assets/47681912/226d59a5-c5f1-44aa-a6dc-2f262759b37d">

After token will be issued reward will be 20 DAPP:
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/6b04a016-5e52-4e62-87d9-e831610c9b08)

In backend the code is as follows:
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/fb12eecd-c78f-410b-8a72-d1ac9497b2ad)

#8. Unstaking Tokens
The balance will no again be 100 mDAI.
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/a95fb6da-fe65-42e8-96e7-cd7fa813c4f6)
The code in backend is:
![image](https://github.com/vinayguptaa/defi-dapp/assets/47681912/4d7ef532-17af-4038-af09-2ab11f59db3a)
Now once again we need to give permission in Metamask to unstake the tokens:
![Uploading image.png…]()
