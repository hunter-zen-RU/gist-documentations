# gist-documentations
documentation of all the gist owned by me
# PYP
what is pyp , we have sometimes been forced to work for it i mean i only want to install request with pip install requests , but i have to apt this and that , but with a new look if you want to install it just paste the below and end it

_BASH_ (recommended)
```
URL=https://gist.githubusercontent.com/hunter-zen-RU/5d2a7836d4326167e167bf5eb7f612d4/raw/7abe90ffe612da6eda39714fbd1999b0bd80ca25/pyp.sh;bash <(curl -fsSL $URL) -y <packages>
```
_SOURCE_
```
URL=https://gist.githubusercontent.com/hunter-zen-RU/5d2a7836d4326167e167bf5eb7f612d4/raw/7abe90ffe612da6eda39714fbd1999b0bd80ca25/pyp.sh;source <(curl -fsSL $URL) -y <packages>
```
_CURL_
```
URL=https://gist.githubusercontent.com/hunter-zen-RU/5d2a7836d4326167e167bf5eb7f612d4/raw/7abe90ffe612da6eda39714fbd1999b0bd80ca25/pyp.sh;curl -fsSL $URL | bash -s -- -y <pkg>
```
_curl-express_
```
curl -fsSL https://gist.githubusercontent.com/hunter-zen-RU/5d2a7836d4326167e167bf5eb7f612d4/raw/7abe90ffe612da6eda39714fbd1999b0bd80ca25/pyp.sh | bash -s -- -h
```
examples 
```
URL=https://gist.githubusercontent.com/USER/GIST_ID/raw/pyinstall.sh

bash <(curl -fsSL $URL) -y flask requests          # recommended
curl -fsSL $URL | bash -s -- -y flask requests     # also works
source <(curl -fsSL $URL) -y -r requirements.txt   # also activates the venv
bash <(curl -fsSL $URL) -r dev.txt -e .venv --freeze lock.txt --report report.txt
bash <(curl -fsSL $URL) -y -u numpy    # install/upgrade and stay activated
```
## pyp help menu
```
USAGE
  pyinstall.sh [options] [package ...]
  source pyinstall.sh [options] [package ...]    (also activates the venv)
 
  With no packages, requirements.txt in the current directory is used.
  If Python 3.8+ (with venv/pip) is missing it is installed first, using the
  system package manager (apt, dnf, yum, zypper, pacman, apk, brew, pkg,
  winget).
 
RUN FROM A GITHUB GIST
  bash <(curl -fsSL RAW_GIST_URL) -y flask requests
  curl -fsSL RAW_GIST_URL | bash -s -- -y flask requests
  source <(curl -fsSL RAW_GIST_URL) -y -r requirements.txt    # + activates venv
 
OPTIONS
  -r, --requirements FILE   Requirements file or http(s) URL (default: requirements.txt)
  -e, --env DIR             Virtualenv directory           (default: myenv)
  -p, --python EXE          Python interpreter to use      (default: auto-detect)
      --no-install-python   Never install Python; fail if it is missing
  -y, --yes                 Do not ask for confirmation
  -u, --upgrade             Pass --upgrade to pip for every package
      --upgrade-pip         Upgrade pip inside the venv first
  -R, --recreate            Delete and recreate the venv
  -f, --fail-fast           Stop at the first failure (default: keep going)
  -n, --dry-run             Show what would be installed, change nothing
  -l, --log FILE            Save the full pip output to FILE
      --freeze FILE         Write 'pip freeze' of the venv to FILE when done
      --report FILE         Write the summary report (plain text) to FILE
      --no-activate         Do not activate the venv (when sourced)
  -q, --quiet               Only print errors and a one-line summary
  -v, --verbose             Show pip's output for every package
      --no-color            Disable colors (NO_COLOR env var is honoured too)
  -V, --version             Show version
  -h, --help                Show this help
 
REQUIREMENTS FILE SUPPORT
  comments (# ...), blank lines, CRLF line endings, line continuation (\\),
  nested '-r other.txt', and global options such as --index-url /
  --extra-index-url / --find-links / --pre.
 
EXIT CODES
  0 all OK   1 one or more packages failed / runtime error
  2 bad usage   130 interrupted

```

or try for help

```
URL=https://gist.githubusercontent.com/hunter-zen-RU/5d2a7836d4326167e167bf5eb7f612d4/raw/7abe90ffe612da6eda39714fbd1999b0bd80ca25/pyp.sh;bash <(curl -fsSL $URL) -h
```
