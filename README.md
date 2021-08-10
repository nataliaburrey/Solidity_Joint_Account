
# Creating Joint Account with Solidity


<img width="1100" alt="Screen Shot 2021-08-06 at 5 04 23 PM" src="https://user-images.githubusercontent.com/80833988/128581200-d2fe9302-9ca8-4b4b-a184-58e919c692f2.png">



📌 Challenge 20

> "Smart contract created with Solidity, that accepts two user addresses linked to a joint savings account. Implementing a financial institution’s requirements for provide the ability to deposit and withdraw funds from the account.
"


## Table of content
- [Overview of the project](https://github.com/nataliaburrey/Solidity_Joint_Account#overview-of-the-project) 
- [Project goals](https://github.com/nataliaburrey/Solidity_Joint_Account#project-goals)
- [Project steps](https://github.com/nataliaburrey/Solidity_Joint_Account#project-steps)
- [Software version control](https://github.com/nataliaburrey/Solidity_Joint_Account#software-version-control)
    - [Work with GitHub](https://github.com/nataliaburrey/Solidity_Joint_Account#work-with-github)
    - [How to install](https://github.com/nataliaburrey/Solidity_Joint_Account#how-to-install)
- [Helps recruiters](https://github.com/nataliaburrey/Solidity_Joint_Account#helps-recruiters)
- [License](https://github.com/nataliaburrey/Solidity_Joint_Account#license)



## Overview of the project 

To automate the creation of joint savings accounts, I am creating Solidity smart contract that accepts two user addresses. These addresses will be able to control a joint savings account. Smart contract uses ether management functions to implement a financial institution’s requirements for providing the features of the joint savings account. These features consist of the ability to deposit and withdraw funds from the account.

## Project goals




## Project steps 

    ###Step 1: Create a Joint Savings Account Contract in Solidity
   

* From the provided starter code, open the Solidity file named joint_savings.sol in the Remix IDE.

* Define a new contract named JointSavings.

 <img width="321" alt="Screen Shot 2021-08-09 at 5 08 50 PM" src="https://user-images.githubusercontent.com/80833988/128789398-e5640b51-d786-479e-9b8c-d30435929a04.png">

* Define the following variables in the new contract:


<img width="697" alt="Screen Shot 2021-08-09 at 5 12 14 PM" src="https://user-images.githubusercontent.com/80833988/128789599-c14f0192-e54c-4549-9af3-0dffd1e6109a.png">


* Define a function named withdraw that accepts two arguments: amount of type uint and recipient of type payable address. In this function, code the following:

<img width="563" alt="Screen Shot 2021-08-09 at 5 12 43 PM" src="https://user-images.githubusercontent.com/80833988/128789630-27c9be2e-475e-4303-8690-68d9505ea341.png">


* Define a require statements

<img width="856" alt="Screen Shot 2021-08-09 at 5 15 26 PM" src="https://user-images.githubusercontent.com/80833988/128789777-ed407e83-42b8-4ac5-b844-a7b5bc22e548.png">


* Add an if statement to check if lastToWithdraw is not equal (!=) to recipient. If it’s not equal, set it to the current value of recipient.

<img width="955" alt="Screen Shot 2021-08-09 at 5 15 44 PM" src="https://user-images.githubusercontent.com/80833988/128789795-ad459adc-0eb1-4cb7-9594-363e3fbdab6a.png">


* Call the transfer function of the recipient, and pass it the amount to transfer as an argument. Set lastWithdrawAmount equal to amount. Set the contractBalance variable 

<img width="869" alt="Screen Shot 2021-08-09 at 5 17 08 PM" src="https://user-images.githubusercontent.com/80833988/128789919-ad332dd0-dac8-4542-bfe0-ce92bd65e85e.png">


* Define a public payable function named deposit. In this function, code the following: Set the contractBalance variable, Define a public function, set the values of accountOne and accountTwo 

<img width="953" alt="Screen Shot 2021-08-09 at 5 18 32 PM" src="https://user-images.githubusercontent.com/80833988/128789984-87a53817-6da2-4737-b32b-c782e249f7cd.png">


* Add a fallback function so that your contract can store ether that’s sent from outside the deposit function.

<img width="612" alt="Screen Shot 2021-08-09 at 5 19 04 PM" src="https://user-images.githubusercontent.com/80833988/128790011-ec33d3c4-0417-4897-aa15-a8342247da1f.png">


    Step 2: Compile and Deploy Your Contract in the JavaScript VM
    
<img width="597" alt="Screen Shot 2021-08-09 at 5 22 58 PM" src="https://user-images.githubusercontent.com/80833988/128790262-e18c08a1-9bfc-43ce-b20e-dd377644a611.png">


    Step 3: Interact with Your Deployed Smart Contract

To interact with your deployed smart contract, complete the following steps:

* Use the setAccounts function to define the authorized Ethereum address that will be able to withdraw funds from your contract.

<img width="286" alt="Screen Shot 2021-08-06 at 3 37 32 PM" src="https://user-images.githubusercontent.com/80833988/128790338-b2e2d118-4100-402d-becf-e9e73a12400c.png">


* Test the deposit functionality of your smart contract by sending the following amounts of ether. After each transaction, use the contractBalance function to verify that the funds were added to your contract:

<img width="301" alt="Screen Shot 2021-08-06 at 3 37 20 PM" src="https://user-images.githubusercontent.com/80833988/128790653-5ed92cc0-b570-4b9b-813d-b31dd9c4375a.png">


##### Transaction 1: Send 1 ether as wei.
<img width="282" alt="Screen Shot 2021-08-06 at 3 42 43 PM" src="https://user-images.githubusercontent.com/80833988/128791068-d56e7d57-7ee2-4fa4-908f-80ef772a8d16.png">


##### Transaction 2: Send 10 ether as wei.

<img width="304" alt="Screen Shot 2021-08-06 at 3 38 26 PM" src="https://user-images.githubusercontent.com/80833988/128791041-df3f299c-a551-4507-9b10-abae8016b2cb.png">


##### Transaction 3: Send 5 ether.

<img width="304" alt="Screen Shot 2021-08-06 at 3 38 58 PM" src="https://user-images.githubusercontent.com/80833988/128791163-0aca95b6-69b6-4d7d-a805-0b44c50e1303.png">



##### Once you’ve successfully deposited funds into your contract, test the contract’s withdrawal functionality by withdrawing 5 ether into accountOne and 10 ether into accountTwo. After each transaction, use the contractBalance function to verify that the funds were withdrawn from your contract. 

<img width="304" alt="Screen Shot 2021-08-06 at 3 38 26 PM" src="https://user-images.githubusercontent.com/80833988/128790747-c7329975-1371-4548-b620-7c42b8e63252.png">

<img width="286" alt="Screen Shot 2021-08-06 at 3 43 14 PM" src="https://user-images.githubusercontent.com/80833988/128791090-e7ed5fb9-3c76-44c3-ad7e-2232acfb760f.png">


##### Use the lastToWithdraw and lastWithdrawAmount functions to verify that the address and amount were correct.


<img width="528" alt="Screen Shot 2021-08-06 at 3 43 57 PM" src="https://user-images.githubusercontent.com/80833988/128790588-e28232e2-dc19-40ec-9c48-a218b6f46c75.png">




## Software version control

[Remix IDE](https://remix.ethereum.org) used to interact with Etherium blockchain.

Remix - Ethereum IDE is an open source web and desktop application. It fosters a fast development cycle and has a rich set of plugins with intuitive GUIs. Remix is used for the entire journey of contract development as well as being a playground for learning and teaching Ethereum.

### Work with GitHub
* Repository created on GitHub
* Files were  committed using command line
* Our repository is organized, and includes Resources folder with CSV  project files, 
* Jupyter Notebook with code runs without errors.
* Answers on nesassary questions are included

### How to install

* Save remote repo from GitHub to your computer (Desktop): in Terninal type:

```
cd desktop

git clone https://github.com/nataliaburrey/Solidity_Joint_Account.git
```

now you can find the folder Solidity_Joint_Account on your desktop




## Helps recruiters

The project was created in collaboration with Berkeley Fintech Bootcamp team


## License

[MIT](https://github.com/nataliaburrey/Solidity_Joint_Account/blob/main/LICENSE)



📔 Contact me: 
📩 nataliaburrey@gmail.com
