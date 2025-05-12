# Telia Tunnistus Pre-production 
## OIDC Integration for Relying Parties

## 📑 Table of Contents
- [📌 Endpoints](#%EF%B8%8F-endpoints)
  - [🔐 OpenID Connect Metadata](#-openid-connect-metadata)
  - [🔑 Keys](#-keys)
  - [🔁 OAuth2 Endpoints](#-oauth2-endpoints)
- [📄 Integration Document](#-integration-document)
- [📋 Regulatory Compliance Requirements for Strong Electronic Identification (Finland)](#regulatory-compliance-requirements-for-strong-electronic-identification-finland)
  - [🔐 General Information](#-general-information)
  - [📢 Official Announcements](#-official-announcements)
  - [📘 Regulation 72B: Identification and Trust Services](#-regulation-72b-identification-and-trust-services)
  - [🔧 Technical Profiles](#-technical-profiles)
    - [OpenID Connect (OIDC)](#openid-connect-oidc)
    - [SAML](#saml)

## 📌 Endpoints

### 🔐 OpenID Connect Metadata

- **Federation Entity Statement**  
  [`/.well-known/openid-federation`](https://tunnistus-pp.telia.fi/.well-known/openid-federation)

- **OIDC Provider Metadata**  
  [`/uas/.well-known/openid-configuration`](https://tunnistus-pp.telia.fi/uas/.well-known/openid-configuration)

- **OAuth 2.0 Provider Metadata**  
  [`/uas/.well-known/oauth-authorization-server`](https://tunnistus-pp.telia.fi/uas/.well-known/oauth-authorization-server)
<br/><br/>

### 🔑 Keys

- **JWKS (Public Keys)**  
  [`/uas/oauth2/metadata.jwks`](https://tunnistus-pp.telia.fi/uas/oauth2/metadata.jwks)

- **Signed JWKS**  
  [`/openid_provider/signed_jwks.jwt`](https://tunnistus-pp.telia.fi/openid_provider/signed_jwks.jwt)
<br/><br/>

### 🔁 OAuth2 Endpoints

- **Authorization Endpoint**  
  [`/uas/oauth2/authorization`](https://tunnistus-pp.telia.fi/uas/oauth2/authorization)

- **Token Endpoint**  
  [`/uas/oauth2/token`](https://tunnistus-pp.telia.fi/uas/oauth2/token)
<br/><br/>

## 📄 Integration Document

📥 [Telia Tunnistus Integration Guide To Identification Broker Service (PDF)](files/Telia%20Tunnistus%20-%20Integration%20guide%20to%20identification%20broker%20service%20v2.29.pdf)
<br/><br/>

## Regulatory Compliance Requirements for Strong Electronic Identification (Finland)

Below are official documents and directives related to electronic identification and trust services in Finland, provided by the Finnish Transport and Communications Agency (Traficom) and the National Cyber Security Centre (NCSC-FI).

### 🔐 General Information

- [Electronic Identification – General Information (FI)](https://www.kyberturvallisuuskeskus.fi/fi/toimintamme/saantely-ja-valvonta/sahkoinen-tunnistaminen)
<br/><br/>

### 📢 Official Announcements

- [Liikenne- ja viestintäviraston tiedote 2025 (FI)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/Liikenne-ja_viestint%C3%A4viraston_tiedote_2025.pdf)
- [Traficom Announcement 2025 (EN)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/Traficom_Announcement_2025_EN.pdf)
<br/><br/>

### 📘 Regulation 72B: Identification and Trust Services

- [Regulation 72B (FI)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/M72B_2022_M%C3%84%C3%84R%C3%84YS_72B_tunnistus-_ja_luottamuspalvelut_julkaistu.pdf)
- [Explanatory Memorandum for Regulation 72B (FI)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/M72B_2022_M%C3%84%C3%84R%C3%84YS_72B_tunnistus-_ja_luottamuspalvelut_PERUSTELUMUISTIO.pdf)
- [Regulation 72B (EN)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/M72B_2022_M%C3%84%C3%84R%C3%84YS_72B_tunnistus-_ja_luottamuspalvelut_ENG_julkaistu.pdf)
- [Explanatory Memorandum for Regulation 72B (EN)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/M72B_2022_M%C3%84%C3%84R%C3%84YS_72B_tunnistus-_ja_luottamuspalvelut_PERUSTELUMUISTIO_ENG.pdf)
<br/><br/>

### 🔧 Technical Profiles

#### OpenID Connect (OIDC)

- [Traficom S213/2023 – OIDC Profile v2.2 for the Finnish Trust Network (EN)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/Traficom_S213_2023_OIDC_Profile_v2_2_for_the_Finnish_Trust_Network_EN.pdf)

#### SAML

- [Traficom S212/2023 – SAML Profile for the Finnish Trust Network (EN)](https://www.kyberturvallisuuskeskus.fi/sites/default/files/media/file/Traficom_S212_2023_SAML_Profile_for_the_Finnish_Trust_Network_EN.pdf)

> _Note: The interface descriptions are available in English only to ensure wide use and prevent interpretation differences._
