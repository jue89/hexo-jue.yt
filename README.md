# jue.yt

**Sorry for my bad English. You are familiar with that language and I did some silly mistakes? Send me a PR and I will own you some beers :)**

## Further instructions for hackers

You hacked my server and want to correct some misspelled words? Or you are future me who forgot how to put everything together? Please stick to the following procedure:

Get all data and dependencies:

``` sh
# Install hexo stuff
npm install -g hexo-cli

# Get the sources and dependencies
git clone --recurse-submodules git@github.com:jue89/hexo-jue.yt.git
cd hexo-jue.yt
git checkout develop
npm install
```

Correct the silly typos and check everything:

``` sh
hexo generate
hexo server
```

Everything is fine? Give yourself a tap on the wrist, commit your changes and upload the ```/public``` folder:

``` sh
git commit -a -m"Spellman!"
git checkout master
git merge --no-ff -m"Published" develop
git push --all -u
scp -r public/* user@server.net:www/jue.yt
```
