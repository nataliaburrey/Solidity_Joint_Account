# Solidity_Joint_Account

📌 Challenge 20

> "Smart contract created with Solidity, that accepts two user addresses linked to a joint savings account. Implementing a financial institution’s requirements for provide the ability to deposit and withdraw funds from the account.
"


## Table of content
- [Overview of the project](https://github.com/nataliaburrey/Paying_Salary_With_Crypto#overview-of-the-project) 
- [Project goals](https://github.com/nataliaburrey/Paying_Salary_With_Crypto#project-goals)
- [Project steps](https://github.com/nataliaburrey/Paying_Salary_With_Crypto#project-steps)
- [Software version control](https://github.com/nataliaburrey/Paying_Salary_With_Crypto#software-version-control)
    - [Libraries](https://github.com/nataliaburrey/Paying_Salary_With_Crypto#libraries)
    - [Work with GitHub](https://github.com/nataliaburrey/Paying_Salary_With_Crypto#work-with-github)
    - [How to install](https://github.com/nataliaburrey/Paying_Salary_With_Crypto#how-to-install)
    - [Run Streamlit](https://github.com/nataliaburrey/Paying_Salary_With_Crypto#run-streamlit)
- [Helps recruiters](https://github.com/nataliaburrey/Paying_Salary_With_Crypto#helps-recruiters)
- [License](https://github.com/nataliaburrey/blockchain_based_ledger#license)



## Overview of the project 

In this Challenge, I was task to  complete the code that enables customers to send cryptocurrency payments to fintech professionals. To develop the code and test it out, we assume the perspective of a Fintech Finder customer who is using the application to find a fintech professional and pay them for their work.

To complete this Challenge, I am using two Python files:
1. [fintech_finder.py]()  contains the code associated with the web interface of the application. The code included in this file is compatible with the Streamlit library. 

2. [crypto_wallet.py]() contains the Ethereum transaction functions. By using import statements, I integrate the crypto_wallet.py Python script into the Fintech Finder interface program that is found in the fintech_finder.py file. 


Integrating these two files allow the user to automate the tasks associated with generating a digital wallet, accessing Ethereum account balances, and signing and sending transactions via Ethereum’s Kovan testnet.

## Project goals

1. Generate a new Ethereum account instance by using your mnemonic seed phrase (which you created earlier in the module).

2. Fetch and display the account balance associated with your Ethereum account address.

3. Calculate the total value of an Ethereum transaction, including the gas estimate, that pays a Fintech Finder candidate for their work.

4. Digitally sign a transaction that pays a Fintech Finder candidate, and send this transaction to the Kovan testnet.

5. Review the transaction hash code associated with the validated blockchain transaction.

6. Once you receive the transaction’s hash code, you will navigate to Kovan’s Etherscan (Links to an external site.) website to review the blockchain transaction details 


## Project steps

The steps for this Challenge are divided into the following sections:

### Step 1: Import Ethereum Transaction Functions into the Fintech Finder Application

##### Import generate_account, get_balance, and send_transaction from the crypto_wallet.py file. 

<img width="638" alt="Screen Shot 2021-08-04 at 4 03 03 PM" src="https://user-images.githubusercontent.com/80833988/128266368-976d1237-2400-4e85-9940-b7f7ab2aed21.png">


##### Call the generate_account function and store the account object. 

<img width="641" alt="Screen Shot 2021-08-04 at 4 03 48 PM" src="https://user-images.githubusercontent.com/80833988/128266414-580b51f1-edf8-4ad8-856e-900a1aae9731.png">

##### Call the get_balance function and pass it the Ethereum account.address. 

<img width="540" alt="Screen Shot 2021-08-04 at 4 05 12 PM" src="https://user-images.githubusercontent.com/80833988/128266512-98987639-4727-4d10-88c9-afbb3e35a7ba.png">





### Step 2: Sign and Execute a Payment Transaction

##### Calculate the transaction’s total wage. 

<img width="649" alt="Screen Shot 2021-08-04 at 4 08 53 PM" src="https://user-images.githubusercontent.com/80833988/128266856-bc69f876-0114-4fa6-8d83-2f259d90ea49.png">


##### Call the send_transaction function and pass it the account, candidate_address, and wage parameters. 
<img width="620" alt="Screen Shot 2021-08-04 at 4 07 07 PM" src="https://user-images.githubusercontent.com/80833988/128266681-032720a8-1dbe-41c8-a11b-fb3fc2a4a9ed.png">


##### Return the transaction hash from the send_transaction and display it on the application’s web interface. 

<img width="327" alt="Screen Shot 2021-08-04 at 4 23 43 PM" src="https://user-images.githubusercontent.com/80833988/128267978-dbeb83fb-1dcf-4a1b-9afa-95736b6b9d50.png">



### Step 3: Inspect the Transaction on Etherscan

##### Send a transaction using the Fintech Finder app


https://user-images.githubusercontent.com/80833988/128267117-7269b2d5-7874-43db-8938-e904530ff639.mov



##### Use the returned transaction hash to verify the transaction on Etherscan. 

<img width="1299" alt="Screen Shot 2021-08-04 at 3 59 28 PM" src="https://user-images.githubusercontent.com/80833988/128267224-a12df8fc-f472-4a6c-bd8c-c09426d17dd3.png">

##### Include a screenshot of the provided transaction details. 


<img width="848" alt="Screen Shot 2021-08-04 at 4 14 36 PM" src="https://user-images.githubusercontent.com/80833988/128267348-ed4419ef-5732-476e-a935-bc51418117fd.png">


##### Provide screenshots from Etherscan that show the sender’s address balance and history, and the recipient's address balance and history. 

            ##### Sender
            
<img width="623" alt="Screen Shot 2021-08-04 at 4 20 53 PM" src="https://user-images.githubusercontent.com/80833988/128267805-de754db2-efd2-4a0b-8bbd-3a3a299d2bb2.png">


            ##### Recipient

<img width="1299" alt="Screen Shot 2021-08-04 at 4 17 51 PM" src="https://user-images.githubusercontent.com/80833988/128268108-690be4b9-f04e-4c2c-a084-bb8d13dcace1.png">



## Software version control


### Libraries 

##### Following libraries were imported

* crypto_wallet.py

[
<img width="658" alt="Screen Shot 2021-08-02 at 1 05 59 PM" src="https://user-images.githubusercontent.com/80833988/127917395-947eaeaf-7ade-471f-84ec-e96e3c8eafa4.png">
](url)

* fintech_finder.py

```
# Import the required libraries and dependencies


import streamlit as st
from dataclasses import dataclass
from typing import Any, List

```

* Streamlit- is an open-source app framework for Machine Learning and Data Science teams.
* Dataclasses-a utility tool to make structured classes specially for storing data. These classes hold certain properties and functions to deal specifically with the data and its representation.
* Typing-provides runtime support for type hints. The most fundamental support consists of the types Any, Union, Tuple, Callable, TypeVar, and Generic.



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

git clone https://github.com/nataliaburrey/Paying_Salary_With_Crypto.git
```

now you can find the repo Paying_Salary_With_Crypto on your desktop




### Run streamlit

1. In the terminal, navigate to the repository folder

2. In the terminal, run the Streamlit application by running the command

```
streamlit run fintech_finder.py

```



## Helps recruiters

The project was created in collaboration with Berkeley Fintech Bootcamp team


## License

[MIT](https://github.com/nataliaburrey/Paying_Salary_With_Crypto/blob/main/LICENSE)



📔 Contact me: 
📩 nataliaburrey@gmail.com
