# VR Access Token
VR Access Token Project for the Open Web Community Hackathon

## Our Project
This solution demonstrates how an NFT published on Mintbase.io can be used as a ticket to a browser-based VR experience. 

Artists Liminallogic and Renderedflesh collaborated to create an immersive artwork inspired by the NEAR protocol. Using a mechanism devloped by the MintGate platform, we created a URL of their VR experience that is gated by a NEAR NFT.

## Links to Project Presentation and Proposal:

Link to the Proposal: https://gov.near.org/t/ideation-for-vr-dao-hackathon-tickets-to-the-metaverse/1749

Link to Presentation: https://prezi.com/view/PdNMocaJtrqAlvmaPHW0/

## How It Was Built
### NFT
The VR Access Token NFT was minted on MintBase. First, we deployed a store. Once the store deployed, we updated the store settings and added Liminallogic and Renderedflesh as minters. 

Then, we provided the following information:
- uploaded the thumbnail image
- set the number of NFTs to be minted
- filled out the description and added tag
- added royalty splits
- added revenue splits
- uploaded media

Then we minted the NFT which resulted in: https://testnet.mintbase.io/thing/UNgM3-n3wZMgRra12x9FrOOKNzaWQOFXSeUuM09K_gs:testing.mintspace2.testnet


### VR Experience
The HTML site was built using A-Frame for webXR. 

### Token Gating Mechanism
MintGate is a platform that allows creators and communities to gate web content using blockchain tokens on Ethereum and 60+ EVM compatible blockchains. Their solution uses React on the frontend and proxy server on the backend. 

A creator inputs the URL of web content, sets the token parameters required for an end-user to hold to access the link, and the MintGate site provides a new, URL-shortened token gated link. Once a user clicks on the link and connects their wallet, MintGate's blockchain-aware CDN confirms that the user has the amount of NFTs or tokens that the creator specified when setting up the link. 

As part of the hackathon, they integrated with NEAR testnet. They updated their CDN to accept and read a NEAR contract addresses and token IDs. They also incorporated the NEAR testnet wallet and enabled it to check data inputted from proxy.
