---
knope: patch
---

# Send the Gitea token in the `Authorization` header

Gitea and Forgejo API requests now send the token as `Authorization: token <token>` instead of the `access_token`
query parameter. The token no longer ends up in access logs or in error messages that include the request URL, and
requests work on Gitea instances that set `DISABLE_QUERY_AUTH_TOKEN`.
