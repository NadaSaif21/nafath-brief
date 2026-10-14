Version: NAFATH-V3
Track: Cybersecurity 

## Overview
A government AI assistant requires six IT fields to work together so citizens can receive reliable answers through a mobile app Software development manages public API changes through semantic versioning helping developers maintain compatibility AI uses retrieval-augmented generation to ground answers in relevant service documents Mobile technology applies iOS App Transport Security to protect connections between the app and its servers Networking uses IPv6 to support a growing number of connected devices Cybersecurity addresses malicious instructions that could manipulate the assistant, while data management protects stored conversations through appropriate anonymization or pseudonymization. Together,these fields support a reliable public service, with my cybersecurity track focusing on direct and indirect prompt injection and ways to reduce the risk
## Software
For the assistant’s stable public API, Semantic Versioning uses MAJOR.MINOR. PATCH. MAJOR must increase when a change breaks compatibility, such as removing an endpoint used by the mobile app MINOR increases when compatible functionality is added or existing functionality is marked as deprecated PATCH increases for compatible bug fixes these rules help developers understand whether an update requires changes to the app

Resource: Semantic Versioning 2.0.0 - https://semver.org/
## AI
Retrieval-Augmented Generation (RAG) combines information retrieval with text generation the assistant first retrieves relevant passages from a document collection, then uses them to generate an answer. For government services, retrieving current, approved guidance can reduce reliance on the model’s stored knowledge and help produce more factual responses However, RAG does not guarantee correctness, so retrieved information and generated answers still need evaluation

Resource: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks - https://arxiv.org/abs/2005.11401
## Mobile
On iOS, App Transport Security (ATS) requires connections made through the URL Loading System, such as URLSession, to use HTTPS and meet TLS security requirements, including trusted certificates and secure encryption. If the government app requests a plain HTTP endpoint, ATS blocks the connection by default and logs an error configured exceptions can permit insecure connections, but weaken protection and should be avoided where possible

Resource: Preventing Insecure Network Connections - https://developer.apple.com/documentation/security/preventing-insecure-network-connections
## Networking
IPv4 uses 32-bit addresses, providing about 4.3 billion possible addresses, whereas IPv6 uses 128-bit addresses and provides a vastly larger address space. This expansion supports many more connected devices and more levels of addressing hierarchy. As citizens access government services through growing numbers of phones and other devices, IPv6 provides addressing capacity for continued growth and supports simpler address autoconfiguration

Resource: RFC 8200 - Internet Protocol, Version 6 (IPv6) Specification - https://www.rfc-editor.org/rfc/rfc8200
## Cybersecurity
Prompt injection occurs when input manipulates an AI model into unintended behavior. Direct injection comes through a user’s prompt, while indirect injection comes from external content, such as a retrieved webpage or document. For the government assistant, two risk reduction measures are separating and clearly identifying untrusted external content, and enforcing least privilege so the assistant can access only necessary data and functions. These controls reduce risk without guaranteeing complete prevention

Resource: LLM01:2025 Prompt Injection - https://genai.owasp.org/llmrisk/llm01-prompt-injection/
## Data
Anonymization transforms chat logs so citizens are no longer identifiable, including through information remaining in the conversation. Pseudonymization replaces or removes identifiers, but separately held information can still link records to individuals. Under the UK GDPR framework described by the ICO, truly anonymous information falls outside data protection law, while pseudonymized logs remain personal data for an agency holding the identifying information and require safeguards

Resource: What are the appropriate safeguards? - https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/the-research-provisions/what-are-the-appropriate-safeguards/
## Misconception in My Track
A common misconception is that prompt injection can only come from a message typed directly by a user. In fact, indirect prompt injection can also come from external content, such as a webpage or document retrieved by the assistant. In OWASP’s “LLM01:2025 Prompt Injection” resource, the “Indirect Prompt Injections” heading explains this distinction. Therefore, the government assistant must treat retrieved content as untrusted and limit its access privileges, rather than assuming that filtering user messages alone is sufficient
## Open Question
How can a government agency detect and prevent prompt injection attacks while keeping its AI assistant useful and easy for citizens to use?
