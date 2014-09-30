SMVC Framework Snippets
=============

![Simple MVC Framework](http://simplemvcframework.com/app/templates/smvcf/img/logo.png)

This is a [Sublime Text][sublime] package which includes a collection of Snippets for [Simple MVC Framework.](http://simplemvcframework.com)

## Installation

### With Package Control

If you have the [Package Control][package_control] package installed, you can install SMVC Framework Snippets from inside Sublime Text itself. Open the Command Palette and select "Package Control: Install Package", then search for Simple MVC Framework Snippets.

### Without Package Control

If you haven't got Package Control installed you will need to make a clone of this repository into your packages folder, like so:

### On Mac

```bash
cd ~/Library/Application\ Support/Sublime\ Text\ 2/Packages/
git clone https://github.com/simple-mvc-framework/SMVC-Snippets.git SMVC-snippets
```

### On Linux

```bash
cd ~/.config/sublime-text-2/Packages/
git clone https://github.com/simple-mvc-framework/SMVC-Snippets.git SMVC-snippets
```

### On Windows

```
cd %APPDATA%/Sublime Text 2/Packages/
git clone https://github.com/simple-mvc-framework/SMVC-Snippets.git SMVC-snippets
```

[sublime]: http://www.sublimetext.com/
[package_control]: http://wbond.net/sublime_packages/package_control

All shortcuts start with the `sm` prefix to use type the snippet and press tab.

### List of avaiable shortcuts ###

(placeholder) = cursor will be placed on each tab.

* [Any Route](#smanyroute)
* [Any Route Any](#smanyrouteany)
* [Any Route Num](#smanyroutenum)
* [Any Route All](#smanyrouteall)
* [Get Route](#smgetroute)
* [Get Route Any](#smgetrouteany)
* [Get Route Num](#smgetroutenum)
* [Get Route All](#smgetrouteall)
* [Post Route](#smpostroute)
* [Post Route Any](#smpostrouteany)
* [Post Route Num](#smpostroutenum)
* [Post Route All](#smpostrouteall)
* [Controller](#smcontroller)
* [Construct](#smcon)
* [DocBlock](#smdocblock)
* [Data](#smdata)
* [Data Title](#smdatatitle)
* [Echo Data](#smechodata)
* [View](#smview)
* [Load Language](#smloadlang)
* [Get Language](#smgetlang)
* [Set Language](#smsetlang)
* [Use](#smuse)
* [Alias](#smalias)
* [Function](#smfun)
* [DB Select](#smdbselect)
* [DB Insert](#smdbinsert)
* [DB Last ID](#smdblastid)
* [DB Update](#smdbupdate)
* [DB Delete](#smdbdelete)
* [DB Truncate](#smdbtrun)
* [Post Data](#smpostdata)
* [this](#smthis)
* [Data Row](#smdatarow)
* [Url Autolink](#smurlautolink)
* [Url Autolink Alias](#smurlautolinka)
* [Url Get Template Path](#smurlgettemp)
* [Url Get Template Path Alias](#smurlgettempa)
* [Url Previous](#smurlprev)
* [Url Previous Alias](#smurlpreva)
* [Url Redirect](#smurlredirect)
* [Url Redirect Alias](#smurlredirecta)
* [Session Set](#smsesset)
* [Session Set Alias](#smsesseta)
* [Session Pull](#smsespull)
* [Session Pull Alias](#smsespulla)
* [Session Get](#smsesget)
* [Session Get Alias](#smsesgeta)
* [Session id](#smsesid)
* [Session id Alias](#smsesida)
* [Session Display](#smsesdisplay)
* [Session Display Alias](#smsesdisplaya)
* [Session Destroy](#smsesdestroy)
* [Session Destroy Alias](#smsesdestroya)


### Router

####Any

#####smanyroute

``` php
Router::any('(placeholder)', '\controllers\welcome@index');
```

#####smanyrouteany

``` php
Router::any('(placeholder)/(:any)', '\controllers\welcome@index');
```

#####smanyroutenum

``` php
Router::any('(placeholder)/(:num)', '\controllers\welcome@index');
```

#####smanyrouteall

``` php
Router::any('(placeholder)/(:all)', '\controllers\welcome@index');
```
####Get####

#####smgetroute

``` php
Router::get('(placeholder)', '\controllers\welcome@index');
```

#####smgetrouteany

``` php
Router::get('(placeholder)/(:any)', '\controllers\welcome@index');
```

#####smgetroutenum

``` php
Router::get('(placeholder)/(:num)', '\controllers\welcome@index');
```

#####smgetrouteall

``` php
Router::get('(placeholder)/(:all)', '\controllers\welcome@index');
```

####Post

#####smpostroute

``` php
Router::post('(placeholder)', '\controllers\welcome@index');
```

#####smpostrouteany

``` php
Router::post('(placeholder)/(:any)', '\controllers\welcome@index');
```

#####smpostroutenum

``` php
Router::post('(placeholder)/(:num)', '\controllers\welcome@index');
```

#####smpostrouteall

``` php
Router::post('(placeholder)/(:all)', '\controllers\welcome@index');
```
### Controller

#####smcontroller

``` 
<?php namespace controllers;
use core\view as View;

class (placeholder) extends \core\controller{

	public function __construct(){
		parent::__construct();
		(placeholder)
	}

	public function index(){
		(placeholder)
	}
	
}
```

#####smcon

``` 
public function __construct(){
	parent::__construct();
	(placeholder)
}
```

#####smdocblock

``` 
/*
 * (placeholder) (placeholder)
 *
 * @author (placeholder)
 * @version (placeholder)
 * @date (placeholder)
 */
```

#####smdata

``` 
$data['(placeholder)'] = '(placeholder)';
```

#####smdatatitle

``` 
$data['title'] = '(placeholder)';
```

#####smechodata

``` 
$data['(placeholder)'];
```

#####smview

``` 
View::rendertemplate('header', $data);
View::render('(placeholder)/(placeholder)', $data);
View::rendertemplate('footer', $data);
```

#####smloadlang

``` 
$this->language->load('(placeholder)');
```

#####smgetlang

``` 
$this->language->get('(placeholder)');
```

#####smsetlang

``` 
$lang['(placeholder)'] = '(placeholder)';
```

#####smuse

``` 
use core\view as View;
```

#####smalias

``` 
use core\(placeholder) as (placeholder);
```

#####smfun

``` 
public function (placeholder)((placeholder)){
	(placeholder)
}
```

#####smdbselect

``` 
$this->_db->select("SELECT * FROM ".PREFIX."(placeholder)"(placeholder));
```

#####smdbinsert

``` 
$this->_db->insert(PREFIX.'(placeholder)',$data);
```

#####smdblastid

``` 
$this->_db->lastInsertId('(placeholder)');
```

#####smdbupdate

``` 
$this->_db->update(PREFIX.'(placeholder)',$data, $where);
```

#####smdbdelete

``` 
$this->_db->delete(PREFIX.'(placeholder)',$data);
```

#####smdbtrun

``` 
$this->_db->truncate($table);
```

#####smpostdata

``` 
$postdata = array();
```

#####smthis

``` 
$this->(placeholder);
```

#####smdatarow

``` 
$data[''][0]->(placeholder);
```

#####smurlautolink

``` 
\helpers\url::autolink('(placeholder)' (placeholder));
```

#####smurlautolinka

``` 
Url::autolink('(placeholder)' (placeholder));
```

#####smurlgettemp

``` 
\helpers\url::get_template_path();
```

#####smurlgettempa

``` 
Url::get_template_path();
```

#####smurlprev

``` 
\helpers\url::previous();
```

#####smurlpreva

``` 
Url::previous();
```

#####smurlredirect

``` 
\helpers\url::redirect('(placeholder)');
```

#####smurlredirecta

``` 
Url::redirect('(placeholder)');
```

#####smsesset

``` 
\helpers\session::set('(placeholder)','(placeholder)');
```

#####smsesseta

``` 
Session::set('(placeholder)','(placeholder)');
```

#####smsespull

``` 
\helpers\session::pull('(placeholder)');
```

#####smsespulla

``` 
Session::pull('(placeholder)');
```

#####smsesget

``` 
\helpers\session::get('(placeholder)');
```

#####smsesgeta

``` 
Session::get('(placeholder)');
```

#####smsesid

``` 
\helpers\session::id();
```

#####smsesida

``` 
Session::id();
```

#####smsesdisplay

``` 
\helpers\session::display();
```

#####smsesdisplaya

``` 
Session::display();
```

#####smsesdestroy

``` 
\helpers\session::destroy('(placeholder)');
```

#####smsesdestroya

``` 
Session::destroy('(placeholder)');
```