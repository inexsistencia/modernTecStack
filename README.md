# modernTecStack

## for sublime-text
- **Pckage Control instalation**

  paste this code on your soblime console, a then restart sublime 
  
  NOTE: if this code does not work, go to **[Packagecontrol site] (https://packagecontrol.io/installation)**

  ```
  import urllib2,os,hashlib; h = 'eb2297e1a458f27d836c04bb0cbaf282' + 'd0e7a3098092775ccb37ca9d6b2e4b7d'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')
  ```
### package to install
Ctrl + shift + P , then type: install package <enter>, and then tipe de name of package that you want to install.

* [EditorConfig](http://editorconfig.org/)
* [emmet](http://docs.emmet.io/cheat-sheet/)

Installation
------------

- Prerequisites (see _Technology Stack_):

    * NodeJS with npm
    * Bower
    * Grunt
    * on Windows machines maybe requires [Visual Studio 2013 WD](https://www.visualstudio.com/downloads/download-visual-studio-vs#d-express-windows-desktop)

- Install:
    ```bash
    cd ~/code
    git clone 
    cd youfolderproyect
    git checkout develop
    bower install
    npm install
    ```

Run server
----------

```bash
grunt serve
```

- Your default web browser should have opened [http://localhost:9002/](http://localhost:9002/)

Build
-----

```bash
grunt build
```

That will create all the build files under the `dist` directory.
If besides creating the builds you want to start a local server, instead run:

```bash
grunt serve:build
```

Technology Stack
---------------
- Package Manager
  - [tutorial] (http://www.saltycrane.com/blog/2014/11/how-install-grunt-ubuntu-1404/)
  - [NPM](http://npmjs.org "NPM")
  - [Grunt](http://gruntjs.com "Grunt") to install by comand line
  
    ```bash
    npm install grunt
    ```
  - [Bower](http://bower.io "Bower")
  
    ```bash
    npm install -g bower
    ```
- [Sass](http://sass-lang.com "Sass")
  
  ```bash
  npm install node-sass 
  ```
- [JQuery](http://jquery.com "JQuery")
- [Angular](https://angularjs.org "Angular")


Naming & Selectors
------------------
- Use BEM methodology [https://en.bem.info/method/](https://en.bem.info/method/)
- All IDs and classes should be prefaced with `proyectsufij_classname`, short for "prname
- "
- All JS target ids and classes should be prefaced with `fol_JS_classname`, **CSS selectors should not be used as JS targets**
- Classes only for CSS
- As flat a CSS structure as possible (avoid nesting, specificity wars at all costs)
- Please do not use !important
- Mobile first - Use min-width media queries are extremely helpful when it comes to coding responsive websites because it reduces code complexity.
