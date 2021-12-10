# Overview

![HOW2 Logo](images/logo-how2.png){ width="150" }

TeachingHOW2s is a professional development platform for teachers. It offers a variety of collaborative learning features and supports single sign-on (SSO), acting as a SAML2 service provider.

This site is intended to act as an SSO integration guide for IT teams in purchasing organisations. For further details on the TeachingHOW2s platform or for general support, see [teachinghow2s.com](https://teachinghow2s.com).

## Integration Process

1. [Contact us](https://teachinghow2s.com/contact) to request SSO activation for your organisation. We'll provide you with SAML credentials to plug in to your identity provider.

2. [Configure](configuration) your identity provider using the details we've provided.

3. Send us corresponding credentials for your configuration.

4. We'll enable SSO in "Test Mode". In this mode you will be able to test SSO authentication using a launch URL that we provide but, for the time being, password authentication will remain active for [standard login requests](https://app.teachinghow2s.com/login) and new user activations.[^1]

5. Once you've verified that SSO authentication is working reliably via your launch URL we'll disable test mode.

6. SSO is fully active. Password authentication will be disabled and all login requests will be routed through your identity provider.

[^1]: This ensures that if there are any issues with our initial SSO configuration your users won't have access to the app disrupted.
