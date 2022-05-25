# SSH Key

## Generating a new SSH key

Generating a new SSH Key with no passphrase.

```shell
ssh-keygen -t rsa -b 4096 -f ~/.ssh/example_id_rsa -C email@example.com -N ''
```

Ensure the ssh-agent is running.

```shell
eval "$(ssh-agent -s)"
```

Add your SSH private key to the ssh-agent.

```shell
ssh-add ~/.ssh/example_id_rsa
```

Copies the contents of the id_rsa.pub file to your clipboard.

```shell
# MacOS
pbcopy < ~/.ssh/example_id_rsa.pub

# Window
clip < ~/.ssh/example_id_rsa.pub

# Linux
cat ~/.ssh/example_id_rsa.pub
```

[Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent){:target="_blank"}

## Register multiple SSH keys

If you need to connect to the same host with different keys then you can achieve it by:

```shell
$ vim ~/.ssh/config
Host example.github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/example_id_rsa
  IdentitiesOnly yes
```

Example of git clone using multiple ssh keys.

```shell
git clone git@example.github.com:username/repo.git
```

## Troubleshooting

On Linux and macOS, verify that the permissions on your IdentityFile are 400.

```shell
chmod 400 ~/.ssh/example_id_rsa
```

If the config file is new, don't forget to do.

```shell
chmod 600 ~/.ssh/config
```
