---
id: moloch-dao
title: DAO Governance and its Integration
author: Aditya Srivastava
author_title: Blockchain Developer, Consenso Labs
author_url: https://github.com/adityasrivastava98
author_image_url: https://avatars2.githubusercontent.com/u/60963825?s=460&v=4
tags: [moloch, gitfunded, dao]
---

In this blog post, We will start by looking on Governance and its specific form Moloch DAO and then we will try it to link it to our main project and use Governance feature with it.

<!--truncate-->

**Governance** determines who has power, who makes decisions, how other players make their voice heard and how account is rendered.

The need for governance exists anytime a group of people come together to accomplish a task. Though the governance literature proposes several definitions, most rest on three dimensions: authority, decision-making and accountability.

5 principles of Governance are:
1. Legitimacy and Voice
2. Direction
3. Performance
4. Accountability
5. Fairness

Read more on [** Governance **](https://iog.ca/what-is-governance/)


What is a **DAO**? It is defined as “a censorship-resistant means to coordinate the deployment of shared resources towards a shared objective”.
A simple example of DAO will be a multisig account where a group of many members can withdraw significant sum of money for a cause.

4 significant Ethereum DAO project are:
1. Aragon
2. DAOstack
3. Colony
4. Moloch

Click here to get a detailed view on these [** DAO project **](http://kronosapiens.github.io/blog/2019/06/16/aragon-daostack-colony-moloch.html)

### Moloch DAO

In this Blog post we will start with looking at Moloch form of Governance and then we will learn to Integrate it to our exsisting project.
Before we dive deep into Moloch DAO lets get familiar with its some of its basic terms and features.

- Member/Contributor: People involved in a Organization or a Project, working towards a common goal.

- Guild Bank: A central place where all the fund contributed through members or sponsors are collected.Only member have the power to spend the funds based on their collective decision of their combined shares.

- Shares: Its like a voting power awarded to each member on the basis of Workdone in the project or money contributed to Guild Bank.

- Proposal: Its a way to deicde things within an organization/project.New members who want to join need to submit proposal along with funds they are contributing and shares that they want.Members can also add proposal to spend fund how they want if it is passed by the members.

- Voting Mechanism: Voting on proposals is not based on number of people towards yes or no but is based on collective sum of shares of people voting yes or no.Suppose a person with 8 shares is voting No ,his 8 shares are added towards no and the final decision is based on collective sum of shares towards yes or no based on whichever is more.

- Voting Period Length: Duration during which members are allowed to cast their vote.

- Grace Period Length: Duration during which members who voted NO are allowed to RageQuit.We will explain RageQuit next.

- RageQuit: We allow participants to exit with their funds if they did not agree with the result of a vote. This is done by allowing members to
“Ragequit” the guild within a “grace period” after voting on a proposal completes but before those members’ ownership is affected by that
proposal.To prevent contentious vote where a large minority exits , it is only allowed for members who voted "NO".

### Mechanism

Any member who has shares have voting power and the  members are not allowed to transfer shares to any one.To become a member the new member must convince an existing member to submit a proposal on his behalf.Existing member evaluate the proposal based on the tribute offered by the new members.A proposal is not only to add members but also to add different functionality or anything that requires to spend tokens from guild bank.Members can propose a proposal to add a functionality and get shares or token from guild bank in return.

A proposal needs a simple majority to pass with no quorum requirement.The voting period is generally 7 days which can be set as our need.Once the proposal is processed concerned smart contract is executed.

After the proposal is processed and the members who voted "NO" are not happy with the outcome, they have the option to "Rage Quit" which means members can cash out their shares instead of spending money they disagree with.After RageQuit members loose thier entire voting power and the voting shares are also diluted.This is helpful if suppose 51% members decide to take shares of the rest 49% members and many other.

In the newer version of Moloch members can also Rage Kick other members and concept of loot, jailing members and bail out member are also incorporated.Though these are important concepts they were not relevant to our project and its need so were left out from the code.

![Moloch Working](/img/moloch.jpeg)

### Integration

After the standalone Moloch Dao code is ready for use, its time to integrate it to our existing project.

Start with importing the code to your main project and create instance variable of same type

```
import './dao/Governance.sol';

Governance dao;
```
Deploy the contract and pass the address to your main project and assign it to your variable as:

```
dao = Governance(daoAddress);
```
Now call the DAO Governance function's such as submit proposal as:

```
dao.submitProposal(applicant,sharesRequested,lootRequested,tributeOffered,tributeToken,paymentRequested,paymentToken,details);
```
You can call any other function as told above which means your Governance code is now integrated with main project.

You can find the entire code [**here**](https://github.com/gitfunded/contracts/tree/master/truffle-contracts/contracts)
