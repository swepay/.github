# Swepay

> **Financial infrastructure for Brazilian fintechs, starting with trust.**

[![Website](https://img.shields.io/badge/website-swepay.co-1e2327)](https://swepay.co)
[![Docs](https://img.shields.io/badge/docs-docs.swepay.co-1e2327)](https://docs.swepay.co)
[![AWS Marketplace](https://img.shields.io/badge/AWS%20Marketplace-CA%20Manager-FF9900)](https://aws.amazon.com/marketplace/pp/prodview-q4fypw6qrmayo)

Swepay builds the identity, certificate, and authentication layers that regulated Brazilian fintechs use to integrate partners, ship products, and operate at regulatory scale — delivered as APIs, so platform teams stop stitching vendors together with glue code.

Everything runs on cloud-native infrastructure in **sa-east-1 (São Paulo)**. Data residency is the default, not a configuration toggle.

---

## Products

| Product | What it is | Status |
|---|---|---|
| **[CA Manager](https://aws.amazon.com/marketplace/pp/prodview-q4fypw6qrmayo)** | mTLS certificate API for B2B partner authentication. Issue, renew, and revoke certificates via REST, with managed CRL/OCSP and an audit trail. | `Available now` |
| **Native Guard** | Managed OIDC/OAuth2 multi-realm identity server — a managed alternative to operating Keycloak yourself. | `In development` |
| **Native Passkey** | FIDO2/WebAuthn passwordless authentication API, designed mobile-first for strong customer authentication. | `Coming soon` |
| **Native Email** | Transactional email API for regulated services: deliverability and an auditable send trail, with Brazilian residency by default. | `Coming soon` |

**CA Manager** is generally available and billed through the **AWS Marketplace** — subscribe, receive your API credentials, and start issuing certificates without a sales call.

---

## Why one platform

Building a regulated fintech in Brazil usually means picking a separate vendor for every layer — IAM, PKI, passwordless, transactional email — and then maintaining the glue code between them forever. Each vendor brings its own API model, its own audit format, and its own roadmap.

Swepay replaces that fragmentation with one coherent surface: a shared identity model, a shared audit trail, and a single vendor relationship. Each product solves a real problem on its own, and each is designed to coexist with the others.

---

## What Swepay is not

We are explicit about scope, so you know exactly when we are the wrong tool:

- **Not a payment gateway.** We do not move money or process transactions.
- **Not an ICP-Brasil Certificate Authority.** CA Manager issues *private* certificates for B2B mTLS between partners you explicitly trust. Those certificates are **not** valid for Open Finance Brasil, Pix/DICT, or SPB — for those scenarios you obtain certificates from an ICP-Brasil AC.
- **Not a KYC or onboarding provider.**

---

## Resources

- 🌐 **Website:** [swepay.co](https://swepay.co) (global) · [swepay.com.br](https://swepay.com.br) (Brasil)
- 🛒 **CA Manager on AWS Marketplace:** [aws.amazon.com/marketplace](https://aws.amazon.com/marketplace/pp/prodview-q4fypw6qrmayo)

---

## Contact

- **General:** contact@swepay.co
- **Security:** security@swepay.co

Found a security issue in a Swepay product? Please email **security@swepay.co** instead of opening a public issue.
