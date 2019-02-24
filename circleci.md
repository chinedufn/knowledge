## Deploying to GitHub Pages

#### CircleCI SSH Key

Their instructions lead to an invalid key

https://discuss.circleci.com/t/cant-add-an-ssh-key-in-ssh-permissions/26344

```sh
# Paste these in one at a time since some have prompts.
openssl genrsa -out ~/.ssh/circleci 2048
ssh-keygen -y -f ~/.ssh/circleci > ~/.ssh/circleci.pub
ssh-keygen -m pem -f ~/.ssh/circleci
cat ~/.ssh/circleci
cat ~/.ssh/circleci.pub

rm ~/.ssh/circleci
rm ~/.ssh/circleci.pub
```
