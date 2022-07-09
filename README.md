# Bigital's Portfolio Deployment Pipeline
Currently it is easier for me to build my Nuxt portfolio with 

```bash
$ npm run generate
```
then copy and paste the resulting build dist. 

Be sure to configure whatever server with a yaml file that points to this repo like so:

```bash
---
    deployment:
        tasks:
            - export DEPLOYPATH=/home/repo/public_html/
           
            - /bin/cp root/file.ext $DEPLOYPATH
            - /bin/cp -R root/folder $DEPLOYPATH
```
with root being the root folder, file.ext being each seperate file, and -R prefix before each seperate folder.
