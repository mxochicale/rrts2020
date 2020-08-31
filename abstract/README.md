# Abstract


## Building tex abstract with:

### (a) Github Actions
#### Setting it up
1. Add `shh-rsa` key in https://github.com/settings/keys following [the documentation](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account) in github.

2. Create a new secret variable called `DEPLOY_KEY` in 
https://github.com/mxochicale/rrts2020/settings/secrets 

Where the value is taken from `id_rsa` with 
`vim ~/.ssh/id_rsa` which looks like:  
```
-----BEGIN RSA PRIVATE KEY-----
...
-----END RSA PRIVATE KEY-----
```

3. Create a gh-pages branch for the pdf files [(see more)](https://www.freecodecamp.org/forum/t/push-a-new-local-branch-to-a-remote-git-repository-and-track-it-too/13222).
```
git checkout -b pdf
rm -rf * ~.git
git commit -m 'clean pdf branch'
git push origin pdf
```

4. Create github action workflow
* Create `.github/workflows/main.yml`
* Setting up variables for pdf documents and keys in [main.yml](../.github/workflows/main.yml)
* Then: do git add, commit and push origin master.


### (b) Local build
#### build LaTeX projet
```
make
```
#### clean LaTeX project
```
make clean
```
