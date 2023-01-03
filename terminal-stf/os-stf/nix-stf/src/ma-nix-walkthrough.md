ls -l ~/.nix-profile/
ls -l ~/.nix-profile/bin/
ls -l ~/.nix-profile/share/
nix profile list
nix profile history
nix profile rollback
nix profile rollback --to 2
nix profile install --profile ~/py39-profile nixpkgs#python39
nix profile install --profile ~/py310-profile nixpkgs#python310
~/py39-profile/bin/python --version
~/py310-profile/bin/python --version
