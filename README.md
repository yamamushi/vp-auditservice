Auditor
=======

Withdrawals
=======

Each participant in the voting pool will operate three physically distinct servers -

* Transaction Server
* Auditing Server
* Key Server

The auditing server audits the OT receipts in real time of all the other participants, particularly looking 
for transactions indicating that a customer wishes to withdraw bitcoins from the pool. The act of sending an 
OT receipt for BTC back to the issuer should include a method of indicating the blockchain address to 
which the withdrawals should be sent.

When the auditing server detects a valid withdrawal request on its own transaction server it creates the 
appropriate bitcoin transaction and passes it around to the other auditing servers for signing. When it 
detects a valid withdrawal request on another transaction server, it stands by to sign the withdrawal transaction.

Withdrawal requests are processed using unspent outputs in the hot series without regard for which server 
originally accepted a particular deposit and which server’s user is requesting a withdrawal.


Deposits
=======



Bootstrapping
=======

Phases of Development
=======

1) Communications
	
	Audit Servers should be able to communicate to eachother through BitMessage, 
	and should also be able to communicate with OT Servers.	

2) Funds
	
	Audit Servers should be able to process test funds, Deposits/Withdrawals. 
	They should be able to communicate the status of these funds to other 
	Audit servers in the pool.

3) Pool Integrity

	The integrity of the pool should be able to be tested by removing Audit 
	servers and OT servers at-will.

4) Bitcoin Integration

	Communication with the Bitcoin Blockchain.



Altering Pool Members
=======

Altering the pool (adding, removing, or replacing members).



Actions
=======

* Adding Funds to Pool
* Removing Funds from Pool
* Check for Inflation
* Adding Members
* Removing Members
* Replacing Members


Known Issues
=======


Definitions
=======

* Funds - 

* Pool - a group of independent Open-Transactions (OT) transaction servers who cooperate to store outputs 
	on the Bitcoin blockchain in order to provide full backing for bitcoin-denominated receipts.

* Multisig - A type of bitcoin output script which uses OP_CHECKMULTISIG as described in BIP11.

* Inflation - 


Related Projects
=======

* ServerCore - https://github.com/monetas/ServerCore
* Verifier - https://github.com/monetas/verifier


References
=======

* Voting Pools Whitepaper - https://docs.google.com/a/monetas.net/document/d/1aS4v4SlvwthYKo2xrAohlqZ9CqcA-9AL4atqq8P_O4c/edit?pli=1

