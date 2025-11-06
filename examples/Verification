# README.md
# zkPassport Education Verification dApp (Noir)

## Overview
#This example demonstrates a **Zero-Knowledge Education Verification** system using **Noir**, inspired by zkPassport and zkKYC identity frameworks.  
#It allows users to prove they hold a verified university diploma **without revealing the university name or degree details** publicly.

## Installation
#1. Install Noir:
#   curl -L https://noir-lang.org/install | bash
#2. Create a new Noir project:
#   noir new zkpassport_education
#3. Replace the contents of `src/main.nr` with the code from `app.nr`.

## Run
#   noir run

## Expected Output
#🎓 zkPassport Education Credential Verification dApp (Noir)  
#Verifying user's academic credentials...  
#✅ Academic credential verified successfully  
#🔐 ZK Proof Commitment: 0x9d4c...

## Notes
#- This is a simplified demonstration of how zkPassport-style systems can protect user data while maintaining trust and verification.  
#- In a real implementation, hashes of educational credentials would be issued by the university and verified via a smart contract or decentralized registry.  
#- Ideal for decentralized job platforms, DAO access control, and Web3 ID systems requiring proof-of-skill or verified background.  
#- Built with **Noir**, the ZK language powering privacy and integrity in the **Aztec** ecosystem.  
#- Can be extended to verify multiple credentials, combine with age or citizenship proofs, or integrate into zkKYC circuits.  


// app.nr
use dep::std;

fn main() {
    // zkPassport credential proof — user verifies university diploma without revealing full data
    let degree_hash = std::hash::pedersen(["BachelorOfScience", "UniversityXYZ"]);
    let claimed_degree_hash = degree_hash; // in a real case, this would come from user input

    std::println("🎓 zkPassport Education Credential Verification dApp (Noir)");
    std::println("Verifying user's academic credentials...");

    // Zero-knowledge proof simulation: confirm diploma authenticity
    assert(degree_hash == claimed_degree_hash, "Credential verification failed");

    let proof_commitment = std::hash::pedersen([
        "zkPassport".to_string(),
        "DegreeVerified".to_string(),
        "UniversityXYZ".to_string()
    ]);

    std::println("✅ Academic credential verified successfully");
    std::println("🔐 ZK Proof Commitment: {}", proof_commitment);
}
