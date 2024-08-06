# Signing git commits

https://medium.com/@timmywil/sign-your-commits-on-github-with-gpg-566f07762a43

```
brew install gnupg pinentry-mac
gpg --gen-key

# Add key to git config
gpg --list-keys
git config --global user.signingkey <PUBKEY>
```

- Add key to GitHub
  - `gpg --armor --export <PUBKEY>` to print the key
  - `github.com > Settings > SSH and GPG Keys > Add Key`
  - Paste the GPG key

## Renew expired GPG key

https://gist.github.com/TheSherlockHomie/a91d3ecdce8d0ea2bfa38b67c0355d00#2-renew-the-expired-key
