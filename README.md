# MarsNeedsYou
Create Solidity Auction Contracts to sell land on Mars

## Required updates to basic contracts
The basic MartianAuction.sol contract was updated with the following changes:
* Removed 'biddingTime'
* Added an 'ended' variable
* Added 'address payable sender' to bid()
* Added 'require(msg.sender == beneficiary, "Not allowed to end auction");' to ensure beneficiary

The basic MartianMarket.sol contract was updated with the following changes:
* 
* 
* 
* 

