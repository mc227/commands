# VS CODE word highlighting
ctrl + shift + L (select same word)
fn + alt + click, click again (create parallel cursor lines)


highlight the word and then hit ctrl + d

---
# contains my go commands for windows compilation and ubuntu running


I'm trying to optimize my compilation of go



```terminal
$env:GOOS = "linux"
$env:GOARCH = "amd64"
go env GOOS GOARCH
go build -o mark1162 main.go


./darwin-amd64 -c simulation-new.json
```
---

git clean -df
git checkout -- .

---

git log --graph --oneline

---

gitk

---

watch -n .5 "echo 'curl 172.16.1.3:8901/api/flow/list.json'"

---
```terminal
(base) PS C:\Users\Mark Costales\Desktop\dev\pin\sos-app> history

  Id CommandLine
  -- -----------
   1 try { . "c:\Users\Mark Costales\AppData\Local\Programs\Microsoft VS Code\resources\app\out\vs\workbench\co...
   2 $env:GOOS = "linux"
   3 $env:GOARCH = "amd64"
   4 go env GOOS GOARCH
   5 go build -o mark5 main.go
   6 git status
   7 git diff
   8 git status
   9 go env GOOS GOARCH
  10 $env:GOOS = "darwin"
  11 go env GOOS GOARCH
  12 go build -o darwin-amd64 main.go
  13 $env:GOARCH = "arm64"
  14 go env GOOS GOARCH
  15 go build -o darwin-arm64 main.go
  16 echo $HITFILE
  17 echo $HIsFILE
  18 echo $HISFILE
  19 echo $HISTFILE


(base) PS C:\Users\Mark Costales\Desktop\dev\pin\sos-app> 
```

---

git pull origin integration
---

Step-by-Step Guide to Set Up ED25519 SSH Key for GitLab
1. Generate a New ED25519 SSH Key Pair:
   Open a terminal and run the following command to generate an ED25519 key pair:
   ```terminal
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```
  You will be prompted to enter a file in which to save the key. Press Enter to accept the default location (~/.ssh/id_ed25519).

  You will also be prompted to enter a passphrase. Enter a secure passphrase or leave it empty if you prefer not to use one.
2. Add Your ED25519 SSH Key to the SSH Agent:
   Ensure the SSH agent is running and add your new ED25519 private key to it:
   ```terminal
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/id_ed25519
   ```
3. Copy the Public Key to GitLab:
   Copy your public key to the clipboard. On Linux: 
   ```terminal
   xclip -sel clip < ~/.ssh/id_ed25519.pub
   ```
4. Add the SSH Key to Your GitLab Account:
   - Sign in to GitLab.
   - Go to your profile settings by clicking on your avatar in the top right corner and selecting "Preferences".
   - In the left sidebar, click on "SSH Keys".
   - Paste your public key into the "Key" field.
   - Give your key a descriptive title (like "Ubuntu VM - ED25519").
   - Click "Add key".
5. Verify SSH Key Connection to GitLab:
   ```terminal
   ssh -T git@gitlab.com
   ```
6. Clone a Repository Using SSH:
   Now you can clone repositories using SSH:
  ```bash
  git clone git@gitlab.com:username/repository.git
  ```

