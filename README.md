## Windows Development Environment

## Cygwin

Install Cygwin with packages:
- ssh
- git
- tmux
- vim
- inconsolata fonts
- mintty

### Mintty

Grab the `.minttyrc` file from the dotfiles repo.

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

Install Vagrant plugins: 
- `vagrant plugin install vagrant-berkshelf`
- `vagrant plugin install vagrant-scp`

## Chef recipes

Clone the cookbooks repo: `https://github.com/namabile/cookbooks.git`.

Run `berks install`.

## Other Tools

- Slack
- Google Drive
- Dashlane

## PgPass File

Set create `~/.pgpass` file for storing postgres and redshift passwords. Ensure the file has `0600` mode premssions.
