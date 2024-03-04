 # Grocy OAuth2 Middleware

This OAuthMiddleware enable OAuth2 based authentication for a 
[Grocy](https://github.com/grocy/grocy) instance.

> **Note:** This is not an official part of Grocy. 
> Please report issues here and **NOT** in the Grocy repo.

This was only tested against [authentik](https://goauthentik.io/) but it should work with any OAuth2 provider.

## Installation & Configuration

1. Copy the `OAuthMiddleware.php` to the Grocy root at `middleware/OAuthMiddleware.php`
2. Configure a OAuth app in your OAuth provider
3. Add the following settings to your `config.php` and adapt to your setup:
```php
Setting('AUTH_CLASS', 'Grocy\Middleware\OAuthMiddleware');

// Options when using OAuthMiddleware
Setting('OAUTH_CLIENT_ID', '');
Setting('OAUTH_CLIENT_SECRET', '');
Setting('OAUTH_SCOPES', 'openid profile');
Setting('OAUTH_USERNAME_CLAIM', 'preferred_username');
Setting('OAUTH_AUTH_URL', '');
Setting('OAUTH_TOKEN_URL', '');
Setting('OAUTH_USERINFO_URL', '');
```