# transaction-lists
This package includes a JSON schema and will soon include example Python utilities for working with transaction lists.

This JSON schema is intended as a testing ground to design specifications for a transaction list which can be used in a dApp interface, such as the Privacy Pools interface.

# What are Transaction Lists?
Transaction lists are a specification for lists of transaction metadata (hash, sender, receiver, label, ...) that can be used by any dApp interface to label transactions of interest. 

Anyone can create, curate and maintain their own transaction list as long as they follow the specification.

Specifically, an instance of a transaction list is a [JSON](https://www.json.org/json-en.html) blob that contains a list of transaction metadata for use in dApp user interfaces. 

This specification is designed with the Privacy Pools use-case in mind. When withdrawing funds from a privacy pool, a user may choose to exclude some deposits from the anonymity set related to their withdrawal, thus proving that the funds they are withdrawing did *not* originate from that deposit. Transaction lists allow users to share information about transactions they find interesting in as transparent a manner as possible. 

# Deploying your list
Once you have authored the list, you can make it available at any URI. Prefer pinning your list to IPFS (e.g. via pinata.cloud) and referencing the list by an ENS name that resolves to the contenthash. An example list is pinned at santaslist.eth. However, it is large and may take a while to download via a public IPFS gateway.
