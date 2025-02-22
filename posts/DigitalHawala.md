---
title: Half-Baked Ideas - Digital Hawala
date: 2025-02-16
---

[Hawala](https://en.wikipedia.org/wiki/Hawala) is an informal money transmission system popular in the Middle East, Africa, and India. At its most basic, it relies on two reputable brokers establishing ties with each other, and agreeing to deliver their own money to recipients upon request. A sender can then ask one broker to send money to somebody far away by depositing money, getting the broker to ask their counterparty broker to discharge their own funds, and then adding the deposited funds to the counterparty broker's "balance". All for a fee.

I propose **digital hawala** - a distributed reputation sharing and telegraphic balance transfer system. Unlike cryptocurrency, this system is **built around trust**, rather than trying to **eliminate all trust**. At the end of the day, all money is given value by people **choosing** to value it. People choose to value certain kinds of money and transact with it based on faith that they will be able to successfully obtain goods and services. The financial system relies on centralization because trust is the bedrock of any successful transaction, and trusted brokers attract more people willing to transact with them. Eliminating all trust and implementing a completely adversarial system defeats the whole point of finance. This is seen in the development of centralized crypto exchanges, and the hard consequences of not perfectly securing crypto / smart contracts. However, this does not mean the financial system can't take advantage of decentralization or web technologies.

Here is one example of how digital hawala can work:
- Digital hawala operates as a distributed trust network [0], where every node has:
    - Public/private key pair
    - A ledger of trust scores on other nodes ranging from 0 to 1
        - 0 - cannot be trusted
        - 1 - completes all network actions/transactions faithfully (even if they are illegal)
    - "Balances" open with other nodes
- The less other nodes judge your trust score to be, the less inclined they will be to increase your balances with them / deliver cash on your behalf
- To transfer some *part of a balance*, a node contacts a counterparty node that it mutually trusts and has a balance with, and requests *part of it* to be delivered to the destination in cash
- These transactions can be chained trusted node to trusted node if the source and destination nodes don't directly trust each other, which is more likely as geographic distance increases
- Every node starts with a trust score of 0 and infinitely low spend limits, limiting it to increasing its balances / trust score with other nodes by:
    - Sending the counterparty nodes real dollars
    - Sending real dollars to recipients on behalf of the counterparty nodes to build up balances with them
- Nodes earn trust by
    - Completing successful transactions
    - Honestly reporting trust scores
- This incentivizes other nodes to "vouch" for them. Trust is calculated by asking other trusted nodes for their opinions of the target node
- System is built in a way to incentivize:
    - Completing honest transactions (double spending, failing to complete transactions, disputes, etc. lowers trust score)
    - Honestly reporting trust score (if a node lies about another node's trust score, this discrepancy w/ other reports causes requesting nodes to penalize it)

The decentralized nature of this system, as well as incentives that drive nodes to honestly play by the rules / complete transactions, makes it efficient and resilient.

[0] https://en.wikipedia.org/wiki/Web_of_trust
