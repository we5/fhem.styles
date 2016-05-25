# FHEM Styles

Improved version of the dkstyles found on: http://blog.krannich.de/mein-fhem/

## Installation

Just checkout the repository and copy the files into the appropriate ```$FHEM_PATH```.

Instead of copying the files I recommend creating a few symbolic links:
```bash
> ln -s $REPO_DIR/build/we5styles.css $FHEM_PATH/www/pgm2/we5styles.css
> ln -s $REPO_DIR/fonts/MetaWebPro $FHEM_PATH/www/fonts/MetaWebPro
```

Then in FHEM you have to set the correct style prefixes:
```
attr WEB stylesheetPrefix we5
```

## Screenshots

![](https://www.dropbox.com/s/k2zfdcj4c3nnemh/Screenshot%202016-05-25%2011.36.26.png?dl=1)

## Customization

You have to have Ruby installed on your system with the Bundler gem. Just   enter ```bundle install``` and sit back and relax.

Afterwards you can easily change the original SCSS files and compile the styles with this command:

```bash
sass --scss --style=compact src/* build/*
```

For even more convenience let it watch the ```src```directory:

```bash
sass --scss --style=compact --watch src:build
```
