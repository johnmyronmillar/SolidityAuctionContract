# MarsNeedsYou
Create Solidity Auction Contracts to sell land on Mars

## Required updates to basic contracts
The basic MartianAuction.sol contract was updated with the following changes:
* Removed 'biddingTime'
* Added an 'ended' variable
* Added 'address payable sender' to bid()
* Added 'require(msg.sender == beneficiary, "Not allowed to end auction");' to ensure beneficiary

The basic MartianMarket.sol contract was updated with the following changes:
* Added 'safeTransferFrom(owner(), auction.highestBidder(), token_id);' to endAuction to prevent fraud
* Added code to 'getAuction' to get the highest bid
* Added code to 'auctionEnded' to end the auction and emit event
* Added code to 'highestBid' to update auction with new highest bid
* Added code to 'pendingReturn' to capture the bids that need to be returned since they weren't the winners
* Added code to 'bid' to caputre the bid information

## Integration setup
Create infura.io account and new project endpoints:
* Kovan https://kovan.infura.io/v3/88fb8bf676674cb0af5e2ad22b2d9d95
* Ropsten https://ropsten.infura.io/v3/88fb8bf676674cb0af5e2ad22b2d9d95

## erroring out
Recieved the following error messages:
* Unable to import "@openzeppelin/contracts/access/Ownable.sol": File not found
* Unable to import "@openzeppelin/contracts/token/ERC721/ERC721.sol": File not found
