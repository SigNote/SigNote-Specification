# The SigNote Specification (draft-00)

This document outlines *SigNote: Signed Notes for Reserve Currencies*. A SigNote refers to digital data that comes from and is signed in trust by a government's central reserve. SigNotes could be used as the digital equivalent to Reserve Currency Bank Notes if adopted by a government's central reserve. Like paper banknotes, all SigNotes are owned by a government's central reserve and can be thought of as legal tender. Unlike paper banknotes, each SigNote contains cryptographic information to identify each entity that interacted with the note. Whereas most paper bank notes are legal tender for the life of the note, SigNotes are only valid for a set amount of time. This provides incentive for those in possession to return time-spent SigNotes to an agent of a government's central reserve where new SigNotes will be issued and the agent can assess the lifetime of the note. Much akin to paper banknotes, SigNotes can be sent from "hand-to-hand" and as such, network connectivity is not required to make payments with SigNotes. Lastly, Double spend attacks are prevented by means of a legal framework aided by the cryptographic information contained within each note and the time limitation of each note. Any double-spent SigNote would be returned more than once to an agent of a government's central reserve when reclaimed. By comparing the difference between similar notes, the rogue entity who double-spent and forked the note would become immediately apparent. Since cryptographic identities must be signed by a government's central reserve and therefore be accountable to a government's central reserve, any such rouge entity could be criminally sentenced under the current legal framework for banknote fraud by most governments.

Copyright © MMXVIII kristopher tate. All Rights Reserved.

Without permission, anyone may use, reproduce or distribute any material in this document for non-commercial and educational use (i.e., other than for a fee or for commercial purposes) provided that the original source and the applicable copyright notice are cited.

**DISCLAIMER**: This SigNote Specification is for information purposes only. kristopher tate does not guarantee the accuracy of or the conclusions reached in this document and as such, it is provided “as is”. kristopher tate does not make and expressly disclaim all representations and warranties, express, implied, statutory or otherwise, whatsoever, including, but not limited to: (i) warranties of merchantability, fitness for a particular purpose, suitability, usage, title or noninfringement; (ii) that the contents of this document are free from error; and (iii) that such contents will not infringe third-party rights. kristopher tate shall have no liability for damages of any kind arising out of the use, reference to, or reliance on this document or any of the content contained herein, even if advised of the possibility of such damages. In no event will kristopher tate be liable to any person or entity for any damages, losses, liabilities, costs or expenses of any kind, whether direct or indirect, consequential, compensatory, incidental, actual, exemplary, punitive or special for the use of, reference to, or reliance on this document or any of the content contained herein, including, without limitation, any loss of business, revenues, profits, data, use, goodwill or other intangible losses.

## Background

Members of the U.S. Congress and the Federal Reserve are said to be in talks as of May 2018 about the possibility of a Federal Reserve Blockchain nicknamed "FedCoin" [[1]]. With the rise of credit cards and subsequently debit cards, the benefits of electronic money transfer are well known and practiced. That said, the boundary between money transfer and unit of reserve currency is also well apparent: today, we continue use paper money in daily commerce that is prone to counterfeiting and damage. Such paper reserve currency cannot be sent long distances or spent online without the help of third-parties.

In his seminal paper, *Bitcoin: A Peer-to-Peer Electronic Cash System* [[2]], Satoshi Nakamoto outlines a money transfer network that would *"allow payments to be sent directly from one party to another without going through a financial institution."* As of May 2018, the current implementation of the bitcoin network consumes a great deal of energy by means of requiring computers to calculate cryptographic proofs of all transactions at great cost [[3]].

## Problems with Bitcoin and related systems
### Economic Problems
Since BitCoin and related systems are built on the principle of a network of computers calculating cryptographic proofs, such systems suffer from the following problems:

* Proofs require massive commitment from our environment [[3]].
* Transactions are costly and slow [[4]].
* Transactions cannot travel from "hand-to-hand".
* Those who can afford the fastest computers serve to get richer than others [[5]].

Bitcoin in particular has a limited number of "coins" that amounts to 21 million in total when all the coins are found. Before such an event, it is said that "mining [coins] will not be profitable due to the high energy cost and expensive hardware needed for mining." [[6]]

### Social Integrity Problems
Our current society and financial system is built on the reserve currency banking model, a model of trust. BitCoin and related systems seemingly aim to replace government backed reserve currency with their own model of a trustless system with no controls or legal oversight. From Nakamoto's paper: "We have proposed a system for electronic transactions without relying on trust." [[2]]

The Federal Reserve's Randal Quarles Says Bitcoin Could Be Dangerous for the Financial System [[7]]
> “Without the backing of a central bank asset and institutional support, it is not clear how a private digital currency at the center of a large-scale payment system would behave, or whether the payment system would be able to function, in times of stress,” Quarles, the Fed’s newly minted vice chairman for supervision, said in remarks prepared for a Thursday conference at the U.S. Treasury Department.

> “Digital currencies are a niche product that sometimes garners large headlines," he said. “But from the standpoint of analysis, the ‘currency’ or asset at the center of some of these systems is not backed by other secure assets, has no intrinsic value, is not the liability of a regulated banking institution, and in leading cases, is not the liability of any institution at all.”

### Zero Accountability: an Agent of Corruption

Bitcoin and related systems are built on anonymous cryptographic primitives that make it easy to subvert international anti-laundering treaties leading to increased drug trafficking.

According to the U.S. DEA [[8]]:
> Emerging as a money laundering threat, virtual currencies, such as Bitcoin, enable [Transnational Criminal Organizations] to easily transfer illicit proceeds internationally.

A joint report published by The Foundation for Defense of Democracies' Center on Sanctions and Illicit Finance [[9]] has indicated that Bitcoin laundering for illicit drug activity is a highly centralized process.

Authors Yaya Fanusi and Tom Robinson [[10]]:
> Mixers have consistently processed about a quarter of incoming illicit Bitcoins per year. The proportion laundered through exchanges and gambling combined has been roughly constant (66 to 72 percent). Of note, Bitcoin exchanges processed 45 percent of laundered Bitcoins, but, as they received much higher volumes, a much lower proportion of their activity is illicit.

These problems are not just limited to Bitcoin: the Federal Bureau of Investigation (FBI) expressed concerns over digital currency *Monero* and its use among criminals. Joseph Battaglia, a special agent working at the FBI's Cyber Division in New York City, had this to say at a joint event with New York's Fordham University [[11]]:

> There are obviously going to be issues if some of the more difficult to work with cryptocurrencies become popular. Monero is one that comes to mind, where its not very obvious what the transaction path is or what the actual value of the transaction is except to the end users. *-- Joseph Battaglia, FBI Special Agent at the NYC Cyber Division*

## Solutions in SigNote
### Signed Banknotes, not Signed Balances
SigNote defines a set of rules for encoding, validating and sending banknote denominations from entity to entity, much like sending files directly from computer to computer. Compare this to BitCoin and related systems where each address in the system stores a balance much like a bank and requires a network of computers to calculate a shared balance.

### Works like a Banknote: No Fees Required
Just like paper banknotes, no fees are required to settle debts. Unlike paper banknotes, SigNotes are digital data that can be securely stored inside a smartphone or physical cryptographic wallet. Settling debts only requires a means of directly connecting to another secure wallet either physically or over the Internet.

![Sending Funds between digital wallets](https://github.com/SigNote/SigNote-Specification/raw/master/images/anime_transfer_currency.gif)

### Transaction Accountability Built-in

* **Cryptographically Signed Identities:** All cryptographic identities used in SigNote are required to be co-signed by a government's central reserve and therefore are accountable to a government's central reserve. In the event of a double-spend, illicit transaction or fraudulent activity, any such rouge entity could be identified and subsequently sentenced if required under the current legal framework for wire fraud by most governments.
* **Privacy Amongst Peers:** Names, phone numbers and addresses are not stored in SigNote as a policy and therefore contribute to the strength of privacy amongst peers.
* **Support for ISIC Codes:** SigNote records a ISIC (International Standard Industrial Classification) code for each transaction that is verified by both sender and recipient so that economic activity can recorded for easy accounting and to protect against money laundering and fraudulent transactions.

## Technical Specification

### The Lifecycle of a SigNote

```
+------------------------------------------------------+
| A SigNote is signed into existence at an authorized  |
|mint using the mint's public/private keypair which is |
|     co-signed by a government's central reserve.     |
+---------------------------+--------------------------+
                            |                           
+---------------------------v--------------------------+
| SigNote sent to a government's central reserve bank. |
+---------------------------+--------------------------+
                            |                           
+---------------------------v--------------------------+
| The Central Reserve or one of its co-signing agents  |
|   signs away the SigNote to a reputable financial    |
|institution (FI). The SigNote is now in the possession|
|of the FI. SigNotes require the signature of the last |
|    and current possessor to start a new transfer.    |
+---------------------------+--------------------------+
                            |                           
                +-----------v----------+                
      +-[SIGN]-->Financial Institutions<--[SIGN]-+      
      |         +----------------------+         |      
      |   SigNotes can be transferred between    |      
      |  Financial Institutions, Retailers and   |      
      | Consumers endlessly until either (i) the |      
      |file size grows too large or (ii) the bill|      
[SIGN]|  reaches its Spent at Time (ST) Limit.   |[SIGN]
+-----v-----+               |              +-----v-----+
| Retailers <----[SIGN]-----+----[SIGN]----> Consumers |
+-----------+               |              +-----------+
                            |                           
+---------------------------v--------------------------+
| Once a SigNote cannot be transferred anymore due to  |
|file size or Spent at Time Limitation, the file can be|
| sent back to an agent of the central reserve system  |
|  where a new SigNote of exact denomination will be   |
|    exchanged for the old SigNote. This provides a    |
|  government's central reserve or treasury with data  |
| that can be used to better the economy and check for |
|            rouge entities in the system.             |
+------------------------------------------------------+
```

### The SigNote File Format

SigNotes are represented and stored on computers as binary files.

All SigNotes contain the following information when first signed into existence:

* Creation Time (TAI64N, 12-bytes)
* Spent at Time (TAI64N, 12-bytes)
* 3-letter Currency Code (ISO 4217, 3-bytes, Ex: JPY, USD)
* Currency Denomination (UINT16, Non-Zero)
* Sequential Identifier (13-bytes, all uppercase, a-z 0-9, asterisk `0x2A` padded)
* Decimal place / subunit indicator position (UINT8, number of places from start of number, Ex: USD is 2, JPY is 0)
* Public key of Authorized Agent of a government's central reserve (Ed25519 key, 32-bytes)
* Signature data from currency code trust root (government central reserve) authorizing Agent's public key (Ed25519 signature, 64-bytes)
* Nonce (UINT32)
* SigNote Hash Key String (64-Bytes) (Ex: *"In God We Trust. Copyright The United States Federal Reserve"*)
* The SigNote's Serial Number (BLAKE2b 64-byte Hash of Initial Data)

Filenames start with the hyphenated concatenation of the ISO 4217 3-letter currency code, followed by the denomination in integer multiples of its least subunit, followed by the serial number and end with the `.snote` file extension. For example, a SigNote representing the denomination of ¥10,000 Japanese Yen would be the following:

`JPY-10000-5891b5b522d5df086d0ff0b110fbd9d21bb4fc7163af34d08286a2e846f6be03.snote`

Likewise, a SigNote representing the denomination of $100.00 United States Dollars would be the following:

`USD-10000-48ae15fd45c3ae607e41a72d153d6c051f267c42f5ea11f26e1b33b183eaf0e8.snote`

Notice again that SigNotes of USD denomination are represented in integer multiples of its least subunit and not a fraction of the main unit.

#### SigNote File Version Header

SigNotes start with the following 4-byte version header:

```
------------- 4-bytes / 32 bits -------------
+--------------------+ +--------------------+
|     MAGIC:"SN"     | |      VERSION       |
|      (0x534E)      | |      (0x0001)      |
+--------------------+ +--------------------+
```

#### SigNote File Sections

After the file version header, a SigNote is a constructed of sections and signed checkpoints.

Each section is represented by the following data structure:

```
------------- 4-bytes / 32 bits -------------
+------------++-------------++--------------+
|SECTION TYPE||SECTION FLAGS||SECTION LENGTH|
|  (UINT8)   ||   (UINT8)   ||   (UINT16)   |
+------------++-------------++--------------+
---- Section Length (MAXIMUM 16383 BYTES) ---
+-------------------------------------------+
|           SECTION SPECIFIC DATA           |
|           (MAXIMUM 16383 BYTES)           |
+-------------------------------------------+
```

#### SigNote Signed Checkpoints

SigNotes are append-only logs of transaction data that MUST be signed after each transaction.

Unless the following requirements are met, any signed checkpoint data will be discarded:

* All checkpoint public keys must be linked to a valid chain of the SigNote's currency trust root. This is accomplished via file sections with type `0x01` hexadecimal.
* The timestamp must be more recent than any other timestamp within the SigNote.
* The timestamp must be within the Spent at Time (ST) Limit of the SigNote.
* The timestamp must be a time earlier than current time of the verification engine.

If the checkpoint is the last checkpoint in the SigNote and is signed by an entity other the verification engine:

* The timestamp must be within 172800 seconds difference of the current time of the verification engine.

A signed checkpoint is designated inside of the file as a section with the registered type `0xFF` hexadecimal and has the following data structure:

```
------------- 4-bytes / 32 bits -------------
+------------++-------------++--------------+
|SECTION TYPE||SECTION FLAGS||SECTION LENGTH|
|(UINT8=0xFF)||   (UINT8)   ||   (UINT16)   |
+------------++-------------++--------------+
------------ 16-bytes / 128 bits ------------
+------------------++-----------------------+
| TAI64N Timestamp ||     Random Nonce      |
|    (12 bytes)    ||       (UINT32)        |
+------------------++-----------------------+
------------ 32-bytes / 256-bits ------------
+-------------------------------------------+
|             SIGNER PUBLIC KEY             |
|             Ed25519(256-bits)             |
+-------------------------------------------+
------------ 64-bytes / 512-bits ------------
+-------------------------------------------+
|    Signature of file up to this point     |
|             Ed25519(512-bits)             |
+-------------------------------------------+
```

#### SigNote Section Listing

This area is reserved for information about each SigNote Section Type.

* `0x00` -- Initialization
* `0x01` -- Signature Trust Authorization <br /> *Connects a public key to a currency's trust root.*
* `0x10` -- Offer <br /> *Offer SigNote to a known public key*
* `0x11` -- Accept <br /> *Accept SigNote under new public key (must match most recent offer section.*
* `0xFE` -- Used to VOID a SigNote before its Spent at Time (ST) Limit. <br /> *Next immediate checkpoint must be signed by an agent of a government's central reserve.*
* `0xFF` -- Signed Checkpoint

### Working with SigNotes

#### Verifying a SigNote

This area is reserved for information about how to Verify a SigNote.

#### Transferring a SigNote

This area is reserved for information about how to Transfer a SigNote.



[1]: https://www.nytimes.com/2018/05/04/upshot/should-the-fed-create-fedcoin-to-rival-bitcoin-a-former-top-official-says-maybe.html
[2]: http://bitcoin.org/bitcoin.pdf
[3]: https://arstechnica.com/tech-policy/2017/12/bitcoins-insane-energy-consumption-explained/
[4]: https://www.cnbc.com/2017/12/19/big-transactions-fees-are-a-problem-for-bitcoin.html
[5]: https://www.theguardian.com/technology/2018/jan/29/cryptocurrencies-bitcoin-blockchain-what-they-really-mean-for-our-future
[6]: https://www.forbes.com/sites/forbestechcouncil/2018/03/29/the-problems-with-bitcoin-and-the-future-of-blockchain/#497e3c9b68dc
[7]: https://www.bloomberg.com/news/articles/2017-11-30/guess-who-s-not-joining-bitcoin-revolution-fed-s-bank-watchdog
[8]: https://www.dea.gov/docs/DIR-040-17_2017-NDTA.pdf
[9]: http://www.defenddemocracy.org/csif
[10]: https://info.elliptic.co/whitepaper-fdd-bitcoin-laundering
[11]: https://www.deepdotweb.com/2017/02/17/fbi-concerned-criminals-use-monero/