---
title: "Registries for Credential Exchange"
category: info

docname: draft-hinton-credential-exchange-latest
submissiontype: independent # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
# consensus: true
v: 3
# area: AREA
# workgroup: Internet Engineering Task Force # "Internet Engineering Task Force" is fine for individual submissions.
keyword:
  - credential exchange
  - credential types
  - extensions
venue:
#  group: WG
#  type: Working Group
#  mail: WG@example.com
#  arch: https://example.com/WG
  github: "Credential-Provider-SIG/Credential-Exchange-IANA"
  latest: "https://Credential-Provider-SIG.github.io/Credential-Exchange-IANA/draft-hinton-credential-exchange.html"

author:
  - fullname: Oscar Hinton
    organization: Bitwarden
    email: ohinton@bitwarden.com
  - fullname: René Léveillé
    organization: 1Password
    email: rene.leveille@1password.com

normative:
  CredentialExchangeFormat:
    author:
      org: Fido Alliance
    title: Credential Exchange Format
    date: 2025-08-14
    target: https://fidoalliance.org/specs/cx/cxf-v1.0-ps-20250814.html
...

--- abstract

This specification defines IANA registries for Fido Alliance Credential Exchange Format (CXF) credential types and extension identifiers.

--- middle

# Introduction

The FIDO Alliance’s credential exchange specifications define a standard format for transferring all types of credentials in a credential manager including passwords, passkeys and more in a manner that is secure by default.

This specification establishes IANA registries for the Credential Exchange Format [CredentialExchangeFormat] credential types and extension identifiers. The initial values for these registries are in the IANA Considerations section of the [CredentialExchangeFormat] specification.

## Requirements Notation and Conventions

The key words "**MUST**", "**MUST NOT**", "**REQUIRED**", "**SHALL**", "**SHALL
NOT**", "**SHOULD**", "**SHOULD NOT**", "**RECOMMENDED**", "**NOT RECOMMENDED**",
"**MAY**", and "**OPTIONAL**" in this document are to be interpreted as
described in BCP 14 {{!RFC2119}} {{!RFC8174}} when, and only when, they
appear in all capitals, as shown here.

# IANA Considerations

This specification establishes two registries:

- The "Credential Exchange Credential Type Identifiers" registry (see {{type-registry}})
- The "Credential Exchange Extension Identifiers" registry (see {{extension-registry}})

Any additional processes established by the expert(s) after the publication of this document will be recorded on the registry web page at the discretion of the expert(s).

## Credential Exchange Format Credential Type Identifier Registry {#type-registry}

Credential Exchange Format credential type identifiers are JSON compatible strings defined in ["Credential Types Registry"](https://fidoalliance.org/specs/cx/cxf-v1.0-ps-20250814.html#sctn-iana-credential-types-registry). Credential type identifiers **MUST** be unique across all registered credential type identifiers.

### Registering Credential Type Identifiers {#registering-credential-types}

Credential Exchange Format credential type identifiers are registered using the Specification Required policy (see Section 4.6 of {{!RFC8126}}).

The "Credential Exchange Format Credential Type Identifiers" registry is located at <https://www.iana.org/assignments/credential-exchange>.

Registration requests consist of at least the following information:

{: newline="true"}
Credential type identifier:
: An identifier meeting the requirements given in {{type-registry}}.

Description:
: A short description of the credential type.

Requires an additional payload:
: A "Y" or "N" value indicating whether the credential type requires an additional payload outside of the Credential Exchange Format JSON document.

Specification Document(s):
: Reference to the document or documents that specify the credential type.

Registrations MUST reference a freely available, stable specification, e.g., as described in Section 4.6 of {{!RFC8126}}. This specification MUST include security and privacy considerations relevant to the credential type.

### Registration Request Processing

As noted in {{registering-credential-types}}, Credential Exchange Format credential type identifiers are registered using the Specification Required policy.

### Initial Values in the Credential Type Identifiers Registry

The values listed in the ["Credential Types Registry"](https://fidoalliance.org/specs/cx/cxf-v1.0-rd-20250313.html#sctn-iana-credential-types-registry) section of the [CredentialExchangeFormat] specification will be used to populate the initial values in the registry. The Change Controller entry for each of those registrations is:

{: newline="true"}
Change Controller:
: Fido Alliance Technical Working Group (todo: email)

## Credential Exchange Extension Identifiers Registry {#extension-registry}

Credential Exchange Format extension identifiers are JSON compatible strings defined in ["Extension Registry"](https://fidoalliance.org/specs/cx/cxf-v1.0-ps-20250814.html#sctn-iana-extension-registry). Extension identifiers **MUST** be unique across all registered extension identifiers.

### Registering Extension Identifiers {#registering-extension-identifiers}

Credential Exchange Format extension identifiers are registered using the Specification Required policy (see Section 4.6 of {{!RFC8126}}).

The "Credential Exchange Format Extension Identifiers" registry is located at <https://www.iana.org/assignments/credential-exchange>.

Registration requests consist of at least the following information:

{: newline="true"}
Extension name identifier:
: An identifier meeting the requirements given in {{type-registry}}.

Description:
: A short description of the credential type.

Requires an additional payload:
: A "Y" or "N" value indicating whether the credential type requires an additional payload outside of the Credential Exchange Format JSON document.

Specification Document(s):
: Reference to the document or documents that specify the credential type.

Registrations MUST reference a freely available, stable specification, e.g., as described in Section 4.6 of {{!RFC8126}}. This specification MUST include security and privacy considerations relevant to the extension.

### Registration Request Processing

As noted in {{registering-extension-identifiers}}, Credential Exchange Format extension identifiers are registered using the Specification Required policy.

### Initial Values in the Credential Exchange Extension Identifiers Registry

The values listed in the ["Extension Registry"](https://fidoalliance.org/specs/cx/cxf-v1.0-rd-20250313.html#sctn-iana-extension-registry) section of the [CredentialExchangeFormat] specification will be used to populate the initial values in the registry. The Change Controller entry for each of those registrations is:

{: newline="true"}
Change Controller:
: Fido Alliance Technical Working Group (todo: email)

# Security Considerations

See [CredentialExchangeFormat] for relevant security considerations.

--- back
