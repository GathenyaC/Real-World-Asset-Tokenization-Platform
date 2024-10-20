1. AssetToken Contract
Function: Represents each tokenized real-world asset (e.g., real estate, artwork) as an ERC-721 (NFT) or ERC-1155 (multi-token).
Key Features:
Minting of tokens representing real-world assets.
Fractional ownership (integrated or through a separate contract).
Transfer, sale, and ownership management.
Connection: Linked to the AssetRegistry contract for verifying asset data.


2. AssetRegistry Contract
Function: A registry of all tokenized assets, storing metadata and legal proof of ownership (e.g., documents, certificates) using decentralized storage (e.g., IPFS).
Key Features:
Register assets before tokenization.
Store asset information such as value, location, or legal documents.
Connection: Connected to the AssetToken contract for verifying and minting tokens only for registered assets.


3. FractionalOwnership Contract (Optional)
Function: Allows fractional ownership by dividing a single asset token (ERC-721) into multiple ERC-20 tokens representing fractions.
Key Features:
Creation of ERC-20 tokens linked to each NFT.
Enables fractional sale, voting on asset decisions, and dividend distribution.
Connection: Works alongside the AssetToken contract to issue and manage fractions.


4. Marketplace Contract
Function: Facilitates buying, selling, and transferring ownership of tokenized assets.
Key Features:
List tokenized assets for sale.
Auction or fixed-price mechanisms for asset sales.
Handles payments and escrows (in native token or stablecoins).
Connection: Interacts with the AssetToken and FractionalOwnership contracts to transfer asset ownership upon purchase.


5. Governance Contract
Function: Allows token holders (owners or fractional owners) to vote on decisions related to the asset, such as selling or modifying the asset.
Key Features:
Voting mechanisms for governance actions.
Proposals for asset management decisions (e.g., upgrades, sales).
Connection: Works with the FractionalOwnership contract for governance over fractionalized assets.


6. Oracle Contract
Function: Ensures real-world events (e.g., asset sale, value updates, or legal status) are reflected on-chain through external data feeds.
Key Features:
Fetch and validate off-chain data (e.g., asset price, legal status).
Update relevant contracts with verified data.
