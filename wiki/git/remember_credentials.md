# Configure Git to remember user credentials
### 1. Set global configuration to store your inputted credentials
```bash
git config --global credential.helper store
```
*NOTE: this setting was previously `credentials.manager store`, but is now `credential.helper store`*

This will store credentials per-site **in plaintext** in the file `~/.git-credentials` with the following format:
```
https://username:password@github.com
https://username:password@gitlab.com
```

You may optionally store your name and email address as well:
```bash
git config --global user.name "Your Name"
git config --global user.email "you@email.com"
```

### 2. Generate a Personal Access Token to use when authenticating
You can generate a token by going to [GitHub `Settings` -> `Developer Settings` -> `Personal Access Tokens`](https://github.com/settings/tokens) and click `Generate new token` on the top right. 

Enter a note describing the token's use (I usually enter the name of the computer / platform) and check the first checkbox (`repo`) to allow this token to read from and write to repositories. Then, click `Generate token` at the bottom.

Copy the token to your clipboard. Once you navigate away from the page it will not be shown again.

### 3. Clone / pull / push to a repository requiring credentials
When prompted for a GitHub password, enter the token you just generated.
