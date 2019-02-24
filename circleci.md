## Deploying to GitHub Pages

#### CircleCI SSH Key

Their instructions lead to an invalid key

https://discuss.circleci.com/t/cant-add-an-ssh-key-in-ssh-permissions/26344

```sh
# Paste these in one at a time since some have prompts.
openssl genrsa -out ~/.ssh/circleci 2048
chmod 600 ~/.ssh/circleci
ssh-keygen -y -f ~/.ssh/circleci > ~/.ssh/circleci.pub
chmod 600 ~/.ssh/circleci.pub

cat ~/.ssh/circleci
echo
cat ~/.ssh/circleci.pub
echo

rm ~/.ssh/circleci
rm ~/.ssh/circleci.pub
```
