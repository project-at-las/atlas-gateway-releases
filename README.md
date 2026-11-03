# Atlas gateway releases

Signed release statements for the Atlas inference gateway.

`current.json` is the release in force. `history/<securityEpoch>.json` keeps every release ever published, in order.

Each file is a security snapshot naming the gateway builds Atlas has authorized: the app, its allowed compose hashes, OS and boot measurements, and a validity window. It is signed with an Atlas release key. Atlas clients and agents hold the release public keys and refuse any snapshot that doesn't verify, so where you fetched the file from doesn't matter.

Release public keys (compressed secp256k1):

- primary `020629dfa3a1bcbdae4adc17314e5eb83a56527af319afbe9e766862df1fe81901`
- backup `02a29310384d2f2ccc044948cc26a2117a1a95066c5dfb883cb7a17a4e704c3907`

These are staging keys, to be replaced before production.

To check a reply's proof yourself, see the gateway's verifier, `atlas-proof-verify`, and the attestation library at https://github.com/b1narydt/binary-attestation.
