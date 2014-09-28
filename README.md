SMVC Framework Snippets
=============

This is a [Sublime Text][sublime] package which includes a collection of Snippets for Simple MVC Framework.

## Installation ##

### With Package Control (NOT YET ACTIVE)###

If you have the [Package Control][package_control] package installed, you can install SMVC Framework Snippets from inside Sublime Text itself. Open the Command Palette and select "Package Control: Install Package", then search for SMVC Framework Snippets.

### Without Package Control ###

If you haven't got Package Control installed you will need to make a clone of this repository into your packages folder, like so:

### On Mac ###

```bash
cd ~/Library/Application\ Support/Sublime\ Text\ 2/Packages/
git clone https://github.com/simple-mvc-framework/SMVC-Snippets.git SMVC-snippets
```

### On Linux ###

```bash
cd ~/.config/sublime-text-2/Packages/
git clone https://github.com/simple-mvc-framework/SMVC-Snippets.git SMVC-snippets
```

### On Windows ###

```
cd %APPDATA%/Sublime Text 2/Packages/
git clone https://github.com/simple-mvc-framework/SMVC-Snippets.git SMVC-snippets
```

[sublime]: http://www.sublimetext.com/
[package_control]: http://wbond.net/sublime_packages/package_control

All shortcuts start with the `sm` prefix

### List of avaiable shortcuts ###

### Router ###

####Any####

`smanyroute`

``` php
Router::any('', '\controllers\welcome@index');
```

`smanyrouteany`

``` php
Router::any('/(:any)', '\controllers\welcome@index');
```

`smanyroutenum`

``` php
Router::any('/(:num)', '\controllers\welcome@index');
```

`smanyrouteall`

``` php
Router::any('/(:all)', '\controllers\welcome@index');
```
####Get####

`smgetroute`

``` php
Router::get('', '\controllers\welcome@index');
```

`smgetrouteany`

``` php
Router::get('/(:any)', '\controllers\welcome@index');
```

`smgetroutenum`

``` php
Router::get('/(:num)', '\controllers\welcome@index');
```

`smgetrouteall`

``` php
Router::get('/(:all)', '\controllers\welcome@index');
```

####Post####

`smpostroute`

``` php
Router::post('', '\controllers\welcome@index');
```

`smpostrouteany`

``` php
Router::post('/(:any)', '\controllers\welcome@index');
```

`smpostroutenum`

``` php
Router::post('/(:num)', '\controllers\welcome@index');
```

`smpostrouteall`

``` php
Router::post('/(:all)', '\controllers\welcome@index');
```
### Controller ###

`smcontroller`

``` 
<?php namespace controllers;
use core\view as View;

class  extends \core\controller{

	public function __construct(){
		parent::__construct();
		
	}

	public function index(){
		
	}
	
}
```

`smcon`

``` 
public function __construct(){
	parent::__construct();
	
}
```

`smdocblock`

``` 
/*
 * Welcome controller
 *
 * @author 
 * @version 1.0
 * @date 
 */
```

`smdatatitle`

``` 
$data['title'] = '';
```

`smview`

``` 
View::rendertemplate('header', $data);
View::render('/', $data);
View::rendertemplate('footer', $data);
```

`smloadlang`

``` 
$this->language->load('');
```

`smgetlang`

``` 
$this->language->get('');
```
