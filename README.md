<h2>SeedSigner Independent Custody Guide</h2>

<img src="https://github.com/SeedSigner/independent_custody_guide/blob/main/images/seedsigner_logo.png" width="450">

## Quick Links (if you want to skip ahead):

* [Introduction](#introduction)
* [Why Multi-signature Wallets?](#why-multi-signature-wallets)
* [What's the story with this SeedSigner thing anyway? (Ideation / Evolution)](#whats-the-story-with-this-seedsigner-thing-anyway)
* [Alright, but there's got to be a catch, right? (Concerns / Considerations)](#alright-but-theres-got-to-be-a-catch-right)
* [So what does this SeedSigner thing actually do? (Core Functionality)](#so-what-does-this-seedsigner-thing-actually-do)
* [How can I get my hands on a SeedSigner to try it out? (Sourcing / Building)](#alright-alright-this-all-sounds-pretty-cool-how-can-i-get-my-hands-on-a-seedsigner-to-try-it-out)
* [Testnet is the best way to, well, test...](#testnet-is-the-best-way-to-well-test)
* [Wallet Set-up and Spend Walkthrough!](#can-we-get-started-with-the-actual-guide-already)
* [Final Variables to Consider](#variables-to-consider)


## Introduction

Most bitcoiners understand the importance of self-custody within the the larger bitcoin ecosystem -- as a digital bearer asset, being able to have personal custody of your coins is a huge part of the ethos of bitcoin (not your keys...not your coins). And holding one's own private keys is not merely some kind of bitcoiner virtue signaling exercise, but actually serves several important functions:

- Protects bitcoin owners from loss of funds due to custodial service thefts or rugpulls
- Allows users to send bitcoin to any recipient without the need for permission **from anyone**
- Foundational to privacy-conscious bitcoin usage
- Protects bitcoin as a financial asset from rehypothication & other forms of value dilution
- Helps bitcoin users understand the network's technical fundamentals (when done properly)


<h2 id="why-multi-signature-wallets">Why Multi-signature Wallets?</h2>

Multi-signature wallets have gotten a bad reputation. Several years ago when the core concept of "multi-signature" storage started to gain traction in the bitcoin ecosystem, the hype and value proposition were real but it it took a fair amount of time for proper tools to be developed. And like most tools, the earliest versions necessarily targeted a more-technical audience, and by the time those tools had emerged the larger hype around multi-signature wallets had died down. This progression of events has seemingly resulted in multi-signature bitcoin storage being perceived as a more niche self-custody option only suited to sufficiently-technical individuals.

One of the primary goals of this guide is to shatter and discard the notion that multi-signature wallets are too complex for most, if not all, bitcoiners -- full stop. If a given multi-signature wallet seems too complex and is practically too difficult for most bitcoiners to use, that is the fault of the wallet's creators, who need to proverbially "return to the drawing board".

The most approachable way I've found for many people to think about multi-signature storage is to consider a multi-signature wallet as a kind of corporate board (sometimes referred to in technical-speak as a "quorum"). Your funds are the board's treasury, and those funds can only be accessed or moved with the approval of a certain number of board members (sometimes referred to as "co-signers"). Usually the number of co-signers required to access funds constitutes a majority of the total signers (think 3-of-5) but the chartering documents that are laid out when the board was created (sometimes referred to as the "multisig policy") dictate how many votes are needed to access funds. (Note that a board that only required one member to be able to approve the movement of funds wouldn't make a lot of sense, and in most scenarios a board that required every member to approve transactions would be difficult to manage.)

Like most analogies, this one breaks down as you get deeper into the technical details, but it still serves as a good starting point for most people. But now with a general idea of how multi-signature wallets work, what are the advantages & disadvantages?

<h2 id="why-multi-signature-wallets">Alright, But There's Got to Be a Catch, Right?</h2>

No technology, especially security-related technologies, are **ALL** positive, there have to be trade-offs or vulnerabilities. What follows is a list of the criticisms/vulnerabilities of SeedSigner of which I am aware; I will also briefly provide my perspective on each of them

<h2 id="why-multi-signature-wallets">So What Does This SeedSigner Thing Actually Do?</h2>

Generally speaking, SeedSigner helps bitcoiners accomplish three important independent custody tasks:

- Creating secure private keys in a trust-minimized way
- Generating extended public keys used during initial wallet configuration
- Securely signing transactions via animated QR code sets

Each one of these tasks deserves some elaboration, so here we go...
