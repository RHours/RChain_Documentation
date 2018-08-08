# Overview
Most technical platforms have an authoritative resource which people building on the platform can use to get accurate, up to date, technical documentation. This proposal describes a documentation system for RChain built in Rholang and served from a RChain namespace. 

## Who usually pays for documentation?
In my career I've worked on the documentation teams of two technical platforms; one at Microsoft, one at Amazon AWS. In both cases the documentation was provided free of charge. Well, that is, the cost of documentation was not itemized on any customer's bill. It was rolled into the cost of the software or service.

## Who will pay for *RChain* documentation?
No one? The co-op? Pyrofex? Reflective? Pithia? I've spoken with each of these groups (except the 'no one' group, come on) and each recognizes the need for documentation and each have made a contribution towards it. In the case of Pyrofex, there is documentation in the development wiki, in the tutorial, in example and test programs, in technical specifications, and also through Discord discussions. The co-op runs the website, publishes hours of recorded video and has funded technically oriented marketing content. Reflective and Pitia have both reached out to me and others to find a way to support what's generally termed "on-boarding", though that term encompasses broader needs than what technical documentation strictly provides. 

While there are efforts underway, there still remains a need for an authoritative source of accurate technical documentation for RChain and Rholang, and that none of the existing stakeholders feel that funding this effort independently is their sole responsibility.

## Creative Commons?
Perhaps an open source commons project will provide the answer. That might happen, but I, personally, wonder about the economics of that approach. The contributors to an RChain open source documentation project can be in two possible categories: they can hold RHOC, or not hold RHOC. If they do not hold RHOC, well, then they are being very kind to provide their work for free to the ultimate benefit of the RHOC price and its holders. If the contributors do hold RHOC, then they can recalculate their purchase price as (market price + labor creating documentation). 

While I'm not an expert in game theory, does it seem that the best action is to let others write the documentation, for free if possible? That's great if it happens, but if not, it seems like a long-term losing approach. Adopting RChain requires significant learning (or unlearning and relearning). That's tough if you're guessing at simple things like syntax and discovering features by spelunking in the code.

## My proposal in more detail
I propose we create a documentation namespace and a documentation Rholang contract, perhaps simply "documentation". This contract receives requests for documentation that are structured in such a way that only the documentation requested is returned. Its similar to the query string of a URL. The content returned is encoded in Rholang terms but a client side viewer transforms this content into something viewable, probably HTML.

My understanding of namespaces tells me that economic decisions can be made as to the gas price of calling contracts within it. I propose that we use the gas fees to pay not just for operating the physical hardware of the namespace but also for the creation of the documentation content. That is, we pay the writers, editors, translators, and developers who created the content and the namespace contracts from the fees.

I can see a fatal flaw, though. One person can pay the gas fee, copy the content and post it to a free server off chain. 

To thwart this, maybe we could intentionally post thousands or millions of fake copies of the content with little annoying errors mixed in so people can't tell if they're getting the correct content or faked content. But, that seems hostile at worst and counterproductive at best. Still, I can't think of a way to physically stop people from copying the content and accessing it without paying the fee. 

Maybe we shouldn't try to stop people from using the documentation for free, but instead be transparent about our efforts to create it and fair in how we price it. Maybe reason and fairness would win over and people would pay? Especially if it's easier to do so? I really don't know, but that is what I propose we do.

## Compensated Open Source
I've been working on an idea I call [compensated open source](https://github.com/RHours/RHours/blob/master/CompensatedOpenSource.md) and a new corporate business structure called [RHours](https://github.com/RHours/RHours). Contributors establish a price for their contributions with the project under its governance procedures at the time the contribution is accepted. While the contributor's personal information remains private, the fact that a contribution was accepted and at what price is public and transparent. Consumers of the content are asked to pay a fee to access the content but can verify their fees went directly to compensate its creators. Once a contribution becomes fully compensated it is released, free of charge, under regular open source terms. 

Certainly, it is fairly inexpensive to copy the content and serve it someplace on or off-chain for free, undercutting the content creators. I, personally, have no magic answer to denying the possibility of this action. It's an act of faith that a transparent justification of the effort of creating the work is a viable argument for paying for it. We can also make the path of consuming and paying very low cost by integrating the for-fee content into Rholang development tools.

## Reaching sustainability
I hope the compensated model will work and achieve a sustained state where older documentation that hasn't changed and doesn't need to gets paid for and then made available for free, and that new developments are paid for through the compensated open source model. But, this model is new and unproven. It is unlikely that developers will join such a project in enough numbers to create the documentation we need without a promise of payment.

I request that the co-op(s), Pyrofex, and the two investment arms, pool their resources to fund a documentation effort under this proposal. If the compensated open source model doesn't work and this investment isn't directly recouped, then it falls back to the same model as regular platform companies. The documentation cost is absorbed into the cost of the platform and would be captured indirectly in its fees.

## More details on the plan
The following plan is described in three, six-month phases. The first phase focuses on getting documentation written and delivered over regular, free (i.e. web) delivery channels while beginning the development of a Rholang documentation publishing tool. The second phase focuses on operating a documentation namespace, integrating the documentation into development tools, and refining the documentation namespace implementation. The final phase transitions to a sustainable model where anyone can publish content and receive compensation without the need for angel investors paying the upfront costs.


## Phase 1 - Now to Main Net launch:
(Note: The term 'fork' is used  below and it means a git fork, not a blockchain fork.)


* Establish a pooled budget from the co-op(s), Pyrofex, Reflective, and Pithia. 
* Create an LLC using the RHours model. This is a ZERO MARGIN company. It makes no profit. The contributions are recorded and then compensated from fees (or purchased from investors) but once paid, the intellectual property is free of charge and open sourced. 
* From the pooled budget, establish SOW contracts with technical writers, editors and translators to work full time in a documentation effort. Size of team governed by budget and scope. Minimum scope is a reference of all Rholang features; its core, system contracts; conceptual topics on the mathematical foundations of Rholang; and an operators guide for node/validator operations. 
* Use github issues and Discord to gather and act on member feedback on documentation prioritization. 
* Write relevant documentation today, published off-chain like any other documentation effort. That is, take no technical dependency on Rholang for authoring or delivering the content in phase 1. 
* From the pooled budget, and from the marketing budget for proofs of concept, sign SOWs with one or two developers to push the content into Rholang, write the documentation contract(s), stand up a documentation namespace, and build a viewer application. 

## Phase 2 - After Main Net launch plus 6 months:
* Establish budget for operating the documentation namespace
* Establish budget for addition development of the documentation system
* Integration with development tools
* Develop a documentation generator (like Javadoc) for Rholang contracts.
* Create syndication model through forking agreements, and child namespaces
* Establish versioning and packaging policies
* Publish economic results of fees collected and compensation paid
* Establish market for buying and selling revenue contracts

## Phase 3 - Main Net + 6 mo to Self Sustaining
* Fee history provides indication of payoff rates for contributions, setting expectations for compensation
* Create a documentation fork tied to the co-op (other forks can do as they wish based on compensated fork agreement)
* Use co-op built governance for co-op documentation fork.
* Continue to develop new documentation as needed (if needed) or simply maintain documentation namespace at likely very low cost making documentation nearly free.
* Support compensation for contributions of any size (from a bug fix to months of effort) with automated SOWs.
