# Run this in browser(Normal way) with the latest commit from main branch:
```
https://tamilsfd25.github.io/
```
# Running with Nix (Recommended for both development and regular use)
Install Nix :-
Refer : https://determinate.systems/blog/determinate-nix-installer/
```bash
curl --proto '=https' --tlsv1.2 -sSf -L https://install.determinate.systems/nix | sh -s -- install
```


Run this in terminal(latest commit):
```bash
nix run github:tamilsfd25/tamilsfd25.github.io
```
This is the equivalent of the follows without polluting your directories. 
```bash
git clone https://github.com/tamilsfd25/tamilsfd25.github.io.git
cd tamilsfd25.github.io
xdg-open index.html
```
Also like a website, this'll fetch the latest changes from the main branch and do this.
Note: On first run it's a little slow coz it cache. 

# Any benefits? Actually yes

When someone gives a PR and you want to try the exact site locally?
Just run this:
```bash
# Note: Here 1 is the PR number
nix run github:tamilsfd25/tamilsfd25.github.io/pull/{PR NUMBER}/head

# Note: b7f67dab81 is the commit SHA
nix run github:tamilsfd25/tamilsfd25.github.io/b7f67dab81
```


This allows you to try the site at any commit, PR in the history with just single command.