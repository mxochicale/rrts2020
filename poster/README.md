# Poster

## Building tex poster with:

### (a) Github Actions
#### Setting it up
3. Create a issuenumber-name branch for the poster files
```
git checkout -b 1-poster-submission
```

4. Ammends github action workflow
* Add branchs in [`.github/workflows/main.yml`](../.github/workflows/main.yml)
* Then: do 

```
git add .
git commit -m 'genesis of poster'
git push origin 1-poster-submission
```

### (b) Local build
#### build LaTeX projet
```
make
```
#### clean LaTeX project
```
make clean
```
