# Yet Another TiddlyWiki Site

## Create a wiki from the template

### Preparation

1. Generate a key pair for GitLab Sync: `ssh-keygen -t ed25519 -C "gitlab sync" -f id_ed25519`
2. **GitLab:** Create a new repository in GitLab with the same name.
3. **GitLab:** Add the pub key to GitLab as the deploy key with the write permission.

### GitHub Repository

1. Visit <https://github.com/doitian/tiddlywiki-template>.
2. Create a new repository from the template.
3. Enable the GitHub Pages feature.
4. Add the private key as the secret `DEPLOY_KEY` in GitHub.
5. Add the output of `ssh-keygen -t ed25519 -C "gitlab sync" -f id_ed25519` as the secret `KNOWN_HOSTS`.
6. Rerun GitHub Actions.

### Post-Actions

1. **GitLab:** Allow push to the protected branch.
2. **GitHub:** Grant personal token access to the new repository.
