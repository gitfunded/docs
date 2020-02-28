---
id: governance
title: Governance
sidebar_label: Governance
---

You can read more about the governance from Moloch DAO [white paper](https://github.com/MolochVentures/Whitepaper/blob/master/Whitepaper.pdf).

Here are some of the Jargons used in the governance system:

## Guild Bank

A bank where all the funds are pooled. All the proposals are funded by this bank 
after the election among the members.
```
voting power = contribution/ total value of the Guild Banks 
```

## Rage quit

The member unhappy with the outcome of the proposal can rage quit the 
project. This means that the member who had voted against (NO) the proposal which had passed
may decide to quit the project and withdraw their funds.

## Shares

Shares are issued to the member proportional to their contribution.
Share can be used to vote on the project activities (tasks and expenses)   
```

    each share value = total value of bank / total shares
```
```  
    redeemable funds = each share value * your shares 

```

To make sure that the shares shouldn't be bought and sold on the open market, they are marked 
not transferable. 

---

## Proposals

Proposals are created when a new member wants to join the project or a project related activity (task, expense) 
needs to be funded. When a proposal is accepted, bank mints new shares and sends to the recipient. 5 proposals can be submitted per day for MVP.

The proposal will be processed by any of the members by invoking processProposal function.
 
## Voting

Once the proposal is submitted there will be a fixed voting period (currently 7 days). Election is simply won by simple majority.
There will be a grace period (currently 7 days) where a member voted against the proposal may rage quit.

Refer Moloch white paper for all the edge cases during the rage quitting and how it affects the active proposals.  
 
## Highlights

* Absolute minimum set of governance functionality to secure the funds from any unaccounted attacks
* Proposals are passed with a simple majority voting process


---
