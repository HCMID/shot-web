# shot-web

Source for website at <http://shot.holycross.edu>.


## Build and deploy from the `src` directory

From a julia terminal, activate the local directory (`]activate`) and build the `__site` directory:

```
using Franklin
optimize( prepath="/Library/WebServer/Documents/", minify = false )
```

Then from a shell in the `src` directory:

```
rsync -avz __site/ USER@shot.holycross.edu:/Library/WebServer/Documents
```
