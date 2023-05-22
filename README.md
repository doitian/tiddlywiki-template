# Yet Another TiddlyWiki Site

## Create a wiki from the template

1. Visit <https://github.com/doitian/tiddlywiki-template>.
2. Create a new repository from the template.
3. Enable the GitHub Pages feature.
4. Create a new repository in GitLab with the same name.
5. Generate a key pair.
6. Add the pub key to GitLab as the deploy key with the write permission.
7. Add the private key as the secret `DEPLOY_KEY` in GitHub.
8. Add the output of `ssh-keygen -t ed25519 -C "gitlab sync" -f id_ed25519` as the secret `KNOWN_HOSTS`.
9. Rerun GitHub Actions.
10. Allow push to the protected branch in GitHub.
