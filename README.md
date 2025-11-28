# pre-requisites
DOOM EMACS installed, synchronized and updated

Deploy EMACS in your systems following the official guide
`https://github.com/doomemacs/doomemacs?tab=readme-ov-file#install`

Once installed, execute doctor and address any problems
```bash
/home/user/.config/emacs/bin/doom doctor
```

then, perform a full emacs synchronization
```bash
/home/user/.config/emacs/bin/doom sync
```
you have a strong EMACS baseline. Now you must activate the core doom emacs golang toolchain

## open `/home/REDACTED/doom/init.el`
## find the `:lang` section
## activate the Language Server Protocol technology for DOOM EMACS removing the comment character that turn off the line.
```elisp
lsp ; Language Server Protocol
```
if the line does not exist, declare it.

## remove the comments in the line that activates the Language Server Protocol technology for The Go Programming Language
```elisp
(go +lsp) ; Enable LSP support for Go
```
then, perform a full emacs synchronization
```bash
/home/REDACTED/.config/emacs/bin/doom sync
```

## in the system unit where you are going to work, create the folder for the project (the `working directory`)
```bash
mkdir "$(name-of-the-working-directory)"
```

## move the terminal to the target working directory
```bash
cd "$(name-of-the-working-directory)"
```

## inside the working directory, clone the flake.nix
```bash
git clone https://github.com/alabamasystem/golang-workbench.git
```

## inside the working directory, go to the cloned folder
```bash
golang-workbench
```

## execute the flake with nix develop
```bash
nix develop
```

## you should see an output as follows
```bash
[REDACTED@REDACTED:~/REDACTED/REDACTED-workbench/REDACTED-REDACTED-REDACTED/golang-workbench]$ nix develop
warning: creating lock file "/REDACTED/REDACTED/REDACTED/REDACTED-REDACTED/REDACTED-REDACTED-REDACTED/golang-workbench/flake.lock": 
• Added input 'flake-utils':
    'https://api.flakehub.com/f/pinned/numtide/flake-utils/0.1.102%2Brev-11707dc2f618dd54ca8739b309ec4fc024de578b/0193276d-5b8f-7dbc-acf1-41cb7b54ad2e/source.tar.gz?narHash=sha256-l0KFg5HjrsfsO/JpG%2Br7fRrqm12kzFHyUHqHCVpMMbI%3D' (2024-11-13)
• Added input 'flake-utils/systems':
    'github:nix-systems/default/da67096a3b9bf56a91d16901293e51ba5b49a27e?narHash=sha256-Vy1rq5AaRuLzOxct8nz4T6wlgyUR7zLU309k9mBC768%3D' (2023-04-09)
• Added input 'nixpkgs':
    'https://api.flakehub.com/f/pinned/NixOS/nixpkgs/0.2505.813095%2Brev-1c8ba8d3f7634acac4a2094eef7c32ad9106532c/019ab6d8-0005-7317-844d-5d868444249f/source.tar.gz?narHash=sha256-dY9qLD0H0zOUgU3vWacPY6Qc421BeQAfm8kBuBtPVE0%3D' (2025-11-24)
/nix/store/v1kv6rv70sjbafs87p6jwrs68wyry5by-go-1.24.9/bin/go
go version go1.24.9 linux/amd64
/nix/store/qrzz6xjlmaarcshxa5z4k547ndp1wpba-gopls-0.19.1/bin/gopls
(nix:nix-shell-env) 
```

You will get as outputs at the end, the coordinates for the go executable and gopls assistant like in this example:

```bash
/nix/store/v1kv6rv70sjbafs87p6jwrs68wyry5by-go-1.24.9/bin/go
go version go1.24.9 linux/amd64
/nix/store/qrzz6xjlmaarcshxa5z4k547ndp1wpba-gopls-0.19.1/bin/gopls
```

## initiate the go project
```bash
go mod init
```
## create the main file
```bash
touch main.go
```

## open `main.go` with DOOM EMACS
## `Alt+F2` `emacs-$(version) /home/REDACTED/working-folder-golang-workbench`
if everything is working fine, you are going to receive a message from the Go Language Server Protocol in the LSP message window

```doom-emacs-lsp
main.go is not part of any project

i ==> Import project root
I ==> Import project by selecting root directory
. ==> Import project at current directory
d ==> Do not ask again for the current project by selecting ignore path interactively
n ==> Do nothing: ask again when opening other files for current project 
```

to work in the current working directory, select `i`












