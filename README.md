# Telia Tunnistus Pre-prod OIDC Integration for Relying Party

## 📌 Endpoints

### 🔐 OpenID Connect Metadata

- **Federation Entity Statement**  
  [`/.well-known/openid-federation`](https://tunnistus-pp.telia.fi/.well-known/openid-federation)

- **OIDC Provider Metadata**  
  [`/uas/.well-known/openid-configuration`](https://tunnistus-pp.telia.fi/uas/.well-known/openid-configuration)

- **OAuth 2.0 Provider Metadata**  
  [`/uas/.well-known/oauth-authorization-server`](https://tunnistus-pp.telia.fi/uas/.well-known/oauth-authorization-server)

### 🔑 Keys

- **JWKS (Public Keys)**  
  [`/uas/oauth2/metadata.jwks`](https://tunnistus-pp.telia.fi/uas/oauth2/metadata.jwks)

- **Signed JWKS**  
  [`/openid_provider/signed_jwks.jwt`](https://tunnistus-pp.telia.fi/openid_provider/signed_jwks.jwt)

### 🔁 OAuth2 Endpoints

- **Authorization Endpoint**  
  [`/uas/oauth2/authorization`](https://tunnistus-pp.telia.fi/uas/oauth2/authorization)

- **Token Endpoint**  
  [`/uas/oauth2/token`](https://tunnistus-pp.telia.fi/uas/oauth2/token)

## 📄 Integration Document

📥 [Telia Tunnistus Integration Guide To Identification Broker Service (PDF)](Telia%20Tunnistus%20-%20Integration%20guide%20to%20identification%20broker%20service%20v2.29.pdf)
