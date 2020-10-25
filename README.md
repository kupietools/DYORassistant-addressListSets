# DYORassistant-addressListSets
Repository of external address list sets for use with DYORa address nicknaming

This repo will contain standalone external address list files that can be refferenced in DYORassistant to assign nicknames to sets of ethereum addresses. The thought is, separate files will allow groups of addresses to be labeled for specific purposes, without using a single list that grows unmanageable huge over time. 

The address lists are standard JSON objects in the format {"address1":"nickname1","address2":"nickname2", ... , "addressN":"nicknameN"}. DYORassistant uses them to display human-readable nicknames on ethereum addresses, making long lists of addresses or transactions easier to make sense of at a glance.

DYORassistant is capable of using either an ethereum address, or the SHA1 hash of an ethereum address, as the "address" key. The particular SHA1 function used is from th jkiss/crypto-JS repository, which DYORa loads from Cloudflare's CDN. If errorLog is set to true in DYORassistant, DYORa will dump the current addressNicknames set to the console when it runs, but with the SHA1 has given as keys instead of the unhashed addresses, so you can copy those into the script if you want to refer to hashes instead of unhashed addresses. The reason hashes are allowed is so address nickname lists can be shared publicly without revealing all the addresses that may be under scrutiny for an investigation. 
