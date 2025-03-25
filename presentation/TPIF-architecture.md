```mermaid
graph TD
    User("User")
    Client("User Client")
    RP("Relying Parties\n(Websites/Apps)")
    MN("Mix Network\n(Onion Routing)")
    VO("Verification Oracles")
    BC("TPIF Blockchain")
    CA("Certificate Authorities")
    IPFS("IPFS\n(Encrypted Storage)")
    
    User -->|uses| Client
    Client -->|communicates via| MN
    MN -->|routes to| RP
    MN -->|routes to| VO
    VO -->|returns result via| MN
    MN -->|routes back to| Client
    VO -->|writes hash commitments| BC
    VO -->|reads DIDs| BC
    BC -->|stores smart contracts| BC
    RP -->|requests verification| VO
    RP -->|reads verification results| BC
    CA -->|issues credentials| Client
    Client -->|stores encrypted data| IPFS
    VO -->|accesses encrypted data| IPFS
    
    classDef primary fill:#4299e1,stroke:#2b6cb0,stroke-width:2px,color:white;
    classDef secondary fill:#9ae6b4,stroke:#2f855a,stroke-width:2px;
    classDef tertiary fill:#fbd38d,stroke:#c05621,stroke-width:2px;
    
    class User,Client primary;
    class RP,CA,IPFS secondary;
    class MN,VO,BC tertiary;
```

# TPIF System Architecture

This diagram illustrates the key components of the Tiered Privacy and Identity Framework (TPIF) and their interactions:

1. **User Client**: Browser extension or app that securely manages DIDs, private keys, and Verifiable Credentials
2. **Mix Network**: Provides onion routing for privacy-preserving communication
3. **Relying Parties**: Websites/applications requesting identity verification
4. **Verification Oracles**: Distributed nodes that verify credentials using MPC
5. **TPIF Blockchain**: Consortium-governed permissioned blockchain for DIDs and smart contracts
6. **Certificate Authorities**: Issue and manage Verifiable Credentials
7. **IPFS**: Decentralized encrypted storage for user data

The architecture provides multiple layers of privacy protection while enabling cryptographically verifiable authentication. All communications between components are routed through the Mix Network to ensure network-level anonymity through onion routing, which is critical for the privacy-preserving login protocol. 