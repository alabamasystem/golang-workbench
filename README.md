# pre-requisites
-  DOOM EMACS installed, synchronized and updated

## the system will ask the following

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
[redacted@redacted:~/redacted/redacted-workbench/redacted-redacted-redacted/golang-workbench]$ nix develop
warning: creating lock file "/redacted/redacted/redacted/redacted-redacted/redacted-redacted-redacted/golang-workbench/flake.lock": 
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

You will get as outputs at the end, the coordinates for the go executable and gopls assistant

## initiate the go project
```bash
go mod init
```
## create the main folder
```bash
touch main.go
```

## open `main.go` with DOOM EMACS













