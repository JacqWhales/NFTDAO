

# MyNFT

The MyNFT contract is a non-fungible token (NFT) contract that extends the ERC721 contract from the OpenZeppelin library. It allows for the minting and management of unique, collectible tokens.

## Properties

*   mintingRate: The maximum number of tokens that can be minted in a single block.
*   lastMintedBlock: The block number of the last time a token was minted.
*   mintsInCurrentBlock: The number of tokens minted in the current block.
*   nftPrice: The price of each token in wei.
*   members: A mapping of addresses to booleans representing whether or not they are members of the DAO.

## Functions

### mint

Mints a new token and assigns it to the specified address.

#### Parameters

*   _to: The address to assign the token to.
*   _tokenId: The unique ID of the token to mint.

### mintNFT

Mints a new token and assigns it to the caller, provided that they have sent the required payment to the contract. Also enforces the minting rate and block restrictions.

#### Parameters

*   _tokenId: The unique ID of the token to mint.

#### Modifiers

*   payable: The function accepts ether payments.

### addMember

Adds the specified address to the list of members of the DAO.

#### Parameters

*   _member: The address to add as a member.

### updateMintingRate

Updates the minting rate of the contract. Can only be called by members of the DAO, and requires a majority vote of the members in favor of the change.

#### Parameters

*   _newRate: The new minting rate to set.

#### Modifiers

*   onlyMembers: The function can only be called by members of the DAO.

</div>
