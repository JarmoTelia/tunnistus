# Telia Tunnistus Pre-Production 
## OIDC Integration for Relying Parties

## 📑 Table of Contents
1. [Endpoints](#1-endpoints)  
   &nbsp;&nbsp;1.1 [OpenID Connect Metadata](#11-openid-connect-metadata)  
   &nbsp;&nbsp;1.2 [Keys](#12-keys)  
   &nbsp;&nbsp;1.3 [OAuth2 Endpoints](#13-oauth2-endpoints)  
2. [Integration Document](#2-integration-document)  
3. [Regulatory Compliance Requirements for Strong Electronic Identification (Finland)](#3-regulatory-compliance-requirements-for-strong-electronic-identification-finland)  
   &nbsp;&nbsp;3.1 [General Information](#31-general-information)  
   &nbsp;&nbsp;3.2 [Official Announcements](#32-official-announcements)  
   &nbsp;&nbsp;3.3 [Regulation 72B: Identification and Trust Services](#33-regulation-72b-identification-and-trust-services)  
   &nbsp;&nbsp;3.4 [Technical Profiles](#34-technical-profiles)  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.4.1 [OpenID Connect (OIDC)](#341-openid-connect-oidc)  
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3.4.2 [SAML](#342-saml)
4. [Tunnistus Python Sample Application](#4-tunnistus-python-sample-application)
5. [Questions and Answers on the Traficom announcement to e-services](#5-questions-and-answers-on-the-traficom-announcement-to-e-services)

---

## 1 Endpoints

### 1.1 OpenID Connect Metadata

- **Federation Entity Statement**  
  [`/.well-known/openid-federation`](https://tunnistus-pp.telia.fi/.well-known/openid-federation)

- **OIDC Provider Metadata**  
  [`/uas/.well-known/openid-configuration`](https://tunnistus-pp.telia.fi/uas/.well-known/openid-configuration)

- **OAuth 2.0 Provider Metadata**  
  [`/uas/.well-known/oauth-authorization-server`](https://tunnistus-pp.telia.fi/uas/.well-known/oauth-authorization-server)
<br/><br/>

### 1.2 Keys

- **JWKS (Public Keys)**  
  [`/uas/oauth2/metadata.jwks`](https://tunnistus-pp.telia.fi/uas/oauth2/metadata.jwks)

- **Signed JWKS**  
  [`/openid_provider/signed_jwks.jwt`](https://tunnistus-pp.telia.fi/openid_provider/signed_jwks.jwt)
<br/><br/>

### 1.3 OAuth2 Endpoints

- **Authorization Endpoint**  
  [`/uas/oauth2/authorization`](https://tunnistus-pp.telia.fi/uas/oauth2/authorization)

- **Token Endpoint**  
  [`/uas/oauth2/token`](https://tunnistus-pp.telia.fi/uas/oauth2/token)
<br/><br/>

## 2 Integration Document

This guide provides instructions for integrating with the Telia Identification Broker Pre-Production Service, enabling strong electronic identification for test users. The service supports both OpenID Connect (OIDC) and Security Assertion Markup Language (SAML) protocols, offering secure authentication in compliance with Finnish regulations. It is intended for technical architects and developers seeking to connect their services to the Identification Broker Service.

📥 [Telia Tunnistus Integration Guide To Identification Broker Service (PDF)](files/Telia%20Tunnistus%20-%20Integration%20guide%20to%20identification%20broker%20service%20v2.30.pdf)
<br/><br/>

## 3 Regulatory Compliance Requirements for Strong Electronic Identification (Finland)

Below are official documents and directives related to electronic identification and trust services in Finland, provided by the Finnish Transport and Communications Agency (Traficom) and the National Cyber Security Centre (NCSC-FI).

### 3.1 General Information

- [Electronic Identification – General Information (FI)](https://www.kyberturvallisuuskeskus.fi/fi/toimintamme/saantely-ja-valvonta/sahkoinen-tunnistaminen)
<br/><br/>

### 3.2 Official Announcements

- [Liikenne- ja viestintäviraston tiedote 2025 (FI)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/Liikenne-ja_viestint%C3%A4viraston_tiedote_2025.pdf)
- [Traficom Announcement 2025 (EN)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/Traficom_Announcement_2025_EN.pdf)
<br/><br/>

### 3.3 Regulation 72B: Identification and Trust Services

- [Regulation 72B (FI)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/M72B_2022_M%C3%84%C3%84R%C3%84YS_72B_tunnistus-_ja_luottamuspalvelut_julkaistu.pdf)
- [Explanatory Memorandum for Regulation 72B (FI)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/M72B_2022_M%C3%84%C3%84R%C3%84YS_72B_tunnistus-_ja_luottamuspalvelut_PERUSTELUMUISTIO.pdf)
- [Regulation 72B (EN)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/M72B_2022_M%C3%84%C3%84R%C3%84YS_72B_tunnistus-_ja_luottamuspalvelut_ENG_julkaistu.pdf)
- [Explanatory Memorandum for Regulation 72B (EN)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/M72B_2022_M%C3%84%C3%84R%C3%84YS_72B_tunnistus-_ja_luottamuspalvelut_PERUSTELUMUISTIO_ENG.pdf)
<br/><br/>

### 3.4 Technical Profiles

#### 3.4.1 OpenID Connect (OIDC)

- [Traficom S213/2023 – OIDC Profile v2.2 for the Finnish Trust Network (EN)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/Traficom_S213_2023_OIDC_Profile_v2_2_for_the_Finnish_Trust_Network_EN.pdf)

#### 3.4.2 SAML

- [Traficom S212/2023 – SAML Profile for the Finnish Trust Network (EN)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/Traficom_S212_2023_SAML_Profile_for_the_Finnish_Trust_Network_EN.pdf)

> _Note: The interface descriptions are available in English only to ensure wide use and prevent interpretation differences._
<br/><br/>

## 4 Tunnistus Python Sample Application

Sample application integration with Python: https://github.com/telia-oss/tunnistus-python-sample

## 5 Questions and Answers on the Traficom announcement to e-services

**Q: How do I know if this applies to me?**<br/>
A: If your service relies on Finnish strong electronic identification methods — such as online banking credentials or the Mobile ID (Mobiilivarmenne) — then this applies to you.

**Q: How do I get started?**<br/>
A: Begin by reading Chapter 2 of the "Telia Tunnistus – Integration Guide to the Identification Broker Service" (version 2.29 or later).

**Q: I only have one key pair. Can I still test signed requests?**<br/>
A: Yes, you can use the same key pair for both signing and encryption. However, for a more secure and scalable setup, it's recommended to use separate key pairs for signing and encryption.

**Q: I already have an OIDC integration with Telia Tunnistus. How can I test signed requests?**<br/>
A: If your OIDC integration is based on public keys, signed requests are already supported. You can begin testing right away.

**Q: Does this apply to SAML integrations?**<br/>
A: This requirement applies only to OIDC integrations, not to SAML-based connections.

**Q: How do I know whether my integration uses signed requests?**<br/>
A: Your authentication request should be structured like this:<br/>
https://tunnistus-pp.telia.fi/uas/oauth2/authorization?request=eyJhbGciOiJSUzI1NiIsImtp...<br/>
You can inspect this using your browser's developer tools. The only parameter must be "request", nothing else.<br/>If the request contains other parameters, they are ignored, and only the parameters included in the signed request object are processed.
