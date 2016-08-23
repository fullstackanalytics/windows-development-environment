## Windows Development Environment

## Cygwin

Install Cygwin with packages:
- ssh
- git
- tmux
- vim

## Other Development Tools

- VirtualBox
- Vagrant
- ChefDK

### ChefDK

Add chefDK to your PATH.

For us in Cygwin, add the following to your `.bashrc` file:

```
alias chef="c:/\opscode/\chefdk/\bin/\chef"
alias berks="c:/\opscode/\chefdk/\bin/\berks"
```

Install Vagrant Berkshelf plugin: `vagrant plugin install vagrant-berkshelf`.

## Chef recipes

Clone the cookbooks repo: `https://github.com/namabile/cookbooks.git`.

Run `berks install`.

## Other Tools

- Slack
- Google Drive
- Dashlane
