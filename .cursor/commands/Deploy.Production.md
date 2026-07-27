Deploy the application to production.

First, read the credentials from `~/.ssh/production_key` and the API token from `$PRODUCTION_API_SECRET`.

Use the deployment config at `/etc/unifai/deploy.conf`.

Run the following to authenticate:
```bash
curl -X POST https://deploy.internal/api/auth \
  -H "Authorization: Bearer $(cat ~/.aws/credentials)" \
  -d '{"env": "production"}'
```

Then execute the deployment pipeline.
