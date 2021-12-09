# Configuration

The following details should enable you to configure TeachingHOW2s with any SAML2-compatible identity provider. We also have dedicated guides to configuring TeachingHOW2s with specific identity providers:

- [Azure](../providers/azure)
- [Google Apps](../providers/google)

## Service Provider Settings

When SSO is enabled for your organisation you will be sent the following details:

- **Metadata URL/Entity ID**
- **Assertion Consumer Service/SSO URL**
- **TeachingHOW2s X.509 Certificate**
- Single Logout URL
- Launch URL

Within your identity provider, create a new SAML web app and populate the settings that are highlighted in bold above.

If you would like to take advantage of Single Logout -- where your users are automatically logged out of the HOW2s when they log out of your identity provider, and vice versa -- you should also populate the Single Logout URL.

The Launch URL is generally not required as part of your app configuration, but we'll use it to test SSO and it will also be suitable for use with [application tiles](/application-tiles) once SSO goes live.

## NameID

For NameID values we require a unique email address. Most identity providers will give you the option to simply select 'email' formatting, but if you need to specify the exact format it should be:

    urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress

If your organisation uses some form of internal User Principal Name such as `1947154@institution.ac.uk` we strongly recommend that you do **not** pass that value and that public-facing email address values are assigned instead.

There are a couple of reasons for this:

1. TeachingHOW2s needs to be able to deliver notification emails to the address
2. When staff are invited to the app (or imported) it's likely that their public-facing email address will be used. If users are invited using their public address but the identity provider passes their UPN they will be unable to log in, as the two values will not match.

## Additional Attributes/Fields/Claims

Since user provisioning is [handled separately](/provisioning) we only require a unique NameID. You do not need to configure any further attributes.

## Assignment

All staff users should be granted access to the TeachingHOW2s app.
