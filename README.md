# Yet Another TiddlyWiki Site

## Create a wiki from the template

1. Visit <https://github.com/doitian/tiddlywiki-template>.
2. Create a new repository from the template.
3. Create a new repository in GitLab with the same name.
4. Generate a key pair.
5. Add the pub key to GitLab as the deploy key with the write permission.
6. Add the private key as the secret `DEPLOY_KEY` in GitHub.
7. Add the output of `ssh-keygen -t ed25519 -C "gitlab sync" -f id_ed25519` as the secret `KNOWN_HOSTS`.
8. Rerun GitHub Actions.
9. Allow push to the protected branch in GitHub.
