---
description: Devopsdao process description
---

# Devopsdao processes

## Roles
Customer - When you create a task, you are in a Customer role.
Performer - When you take a task, you are in a Performer role.
Auditor - When who Audit a task, you are in a Auditor role.

## Wallet connection:

When you open Devopsdao app, it will show you publicly viewable Tasks. In order to create a new Task, take or Audit an existing Task you must connect your wallet.
Currently to options are supported: Metamask and WalletConnect.
1. Metamask is supported on Desktop and Mobile. To connect with Metamask on Desktop, please install Metamask browser plugin. To connect with Metamask on Mobile, please install Metamask App for Android or IOS and open Devopsdao in Metamask in-app browser.
2. Wallet connect is supported on Desktop and Mobile. To connect with WalletConnect on Desktop, please install WalletConnect compatible wallet on your mobile device and scan the QR code. Connection via the WalletConnect on Mobile devices is available both from Devopsdao native app and Devopsdao web app. To connect via the WalletConnect on Mobile, please press connect, and the WalletConnect compatible wallet will be opened. If it is not installed, we suggest to install Metamask, Trustwallet or Alphawallet.

After connecting, you will see the "Wallet connected" message.

Below are the Devopsdao process descriptions, with a user (role) and a task [state].

## Task creation (Customer) [New State]

To create a Task, press create Task button, then the Task creation dialog will appear. You should put a Task Title which shortly describes the nature of the task and a full Description of it, you can checkout Task creation best practices for Task creation recommendations.
Currently you can fund the Task with DEV and aUSDC tokens. After you are done, press create button and then your wallet will prompt you to confirm the transaction, in the case when you fund with aUSDC you will first have to approve aUSDC token spend by Devopsdao smart contract. After the transaction is minted, the task will appear in the Customer tab for you, and in Tasks for other Devopsdao users.

## Task participation (Performer) [New State]

To take the task as a Performer, navigate to the Tasks page and pick the Task you like, read its Description and if you are convinced you can make it fill-in the Task appication text box and click Participate. Your wallet will ask for transaction confirmation. After the transaction is minted, Task will move to the Applied tab on the Perfomer page, and the Customer will see that a Performer has applied for a task.

## Performer selection (Customer) [Agreed State]

When someone has applied to work on the Task, Customer will see it on the Selection tab of the Customer page.
Customer can select one of the Performers who have applied for a Task. When a Performer is selected he will see a Task in the Working tab of the Performer page, other Performers will see lost Tasks in the Lost tab.

## Working on a Task (Performer) [Progress State]

When you are selected to work on the Task as a Performer, you will see it on the Working tab, you should then write your short plans for implementing the Task and press Start the task button. Your wallet will ask for transaction confirmation. After the transaction is minted, the Task will change its color to indicate that the Task is in the Progress state..

## Submitting a Task for the Review (Performer) [Review State]

After finishing your work on the Task, you should submit it for the Review, you should then write your notes for the Customer, probably include a link to your work, or pass it via the agreed with the Customer method offchain and press Review button. Your wallet will ask for transaction confirmation. After the transaction is minted, the Task will change its color to indicate that the Task is in the Review state.

## Reviewing a Task (Customer) [Review State]

When a Performer has sent his work for a Review, you will see your task in the Review state on the Progress tab of the Customer page. You should then carefully review the received work from the Performer and if you are convinced that the Task is implemented, press Sign review button. Your wallet will ask for transaction confirmation. After the transaction is minted, the Task will move to the Completed tab of the Customer page, the Performer will also see it on the Completed tab of the Performer page.

## Withdrawing funds (Performer) [Complete State]

When a Customer has signed the Review, you can withdraw your earned funds to a preferred chain(Moonbase or one which is supported by Axelar). Select the preferred chain and press Withdraw button. Your wallet will ask for transaction confirmation. After the transaction is minted, you will receive funds to your wallet.

## Audit process [Audit State]

When a task is in Agreed, Progress, Review stage Customer can apply for an Audit. When a task is in a Review stage a Performer can apply for an Audit. A 10% audit fee is paid by topping up the task contract during the application.

When a task is sent to Audit, it is available for Auditors to apply for it, then the Initiator of the audit can select the Auditor(note: maybe we will make it random). When an Auditor is selected he carefully reviews the task and asks the Performer to send him his work, the Auditor must analyze if the work matches the tasks requirements and within 48 hours make his decision either to: set the task to a Completed stage, or return it back to the New stage for a new Performer selection. When the work does not match the task requirements, Auditor based on on his professional expertise has a right to ask the Performer to send his corrections if he believes that it is minor and the work can be improved within the Audit period. Auditor role is to effectively and economically resolve the issue raised between the Customer and Performer, for which he gets 10% Audit fee.

