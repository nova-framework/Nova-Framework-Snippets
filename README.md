SMVC Framework Snippets
=============

![Simple MVC Framework](http://simplemvcframework.com/app/templates/smvc/img/logo.png)

This is a [Sublime Text][sublime] package which includes a collection of Snippets for [Simple MVC Framework.](http://simplemvcframework.com)

## Installation

### With Package Control

If you have the [Package Control][package_control] package installed, you can install SMVC Framework Snippets from inside Sublime Text itself. Open the Command Palette and select "Package Control: Install Package", then search for Simple MVC Framework Snippets.

All shortcuts start with the `sm` prefix to use type the snippet and press tab.

### List of avaiable shortcuts ###

(placeholder) = cursor will be placed on each tab.

####Routes
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

####Core
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

####Helpers

#####Assets
* [Assert CSS](#smassetscss)
* [Assert JS](#smassetsjs)

#####Csrf (Cross Site Request Forgeries)
* [Csrf Make Token](#smcsrfmaketoken)
* [Csrf Is Token Valid](#smcsrfistokenvalid)

#####Data
* [Data print_r](#smdatapr)
* [Data strlen](#smdatals)
* [Data strtolower](#smdatastl)
* [Data stringtoupper](#smdatastu)
* [Data ucwords](#smdataucw)
* [Data var_dump](#smdatavd)

#####Url
* [Url Autolink](#smurlautolink)
* [Url Template Path](#smurltemppath)
* [Url Previous](#smurlprev)
* [Url Redirect](#smurlredirect)
* [Url Generate Safe Slug](#smurlgeneratesafeslug)
* [Url Segments](#smurlsegments)
* [Url Get Segment](#smurlgetsegment)
* [Url First Segment](#smurlfirstsegment)
* [Url Last Segment](#smurllastsegment)

#####Session
* [Session Set](#smsesset)
* [Session Pull](#smsespull)
* [Session Get](#smsesget)
* [Session id](#smsesid)
* [Session Display](#smsesdisplay)
* [Session Destroy](#smsesdestroy)


### Router

####Any

#####smanyroute

``` php
Router::any('(placeholder)', 'Controllers\Welcome@index');
```

#####smanyrouteany

``` php
Router::any('(placeholder)/(:any)', 'Controllers\Welcome@index');
```

#####smanyroutenum

``` php
Router::any('(placeholder)/(:num)', 'Controllers\Welcome@index');
```

#####smanyrouteall

``` php
Router::any('(placeholder)/(:all)', 'Controllers\Welcome@index');
```
####Get####

#####smgetroute

``` php
Router::get('(placeholder)', 'Controllers\Welcome@index');
```

#####smgetrouteany

``` php
Router::get('(placeholder)/(:any)', 'Controllers\Welcome@index');
```

#####smgetroutenum

``` php
Router::get('(placeholder)/(:num)', 'Controllers\Welcome@index');
```

#####smgetrouteall

``` php
Router::get('(placeholder)/(:all)', 'Controllers\Welcome@index');
```

####Post

#####smpostroute

``` php
Router::post('(placeholder)', 'Controllers\Welcome@index');
```

#####smpostrouteany

``` php
Router::post('(placeholder)/(:any)', 'Controllers\Welcome@index');
```

#####smpostroutenum

``` php
Router::post('(placeholder)/(:num)', 'Controllers\Welcome@index');
```

#####smpostrouteall

``` php
Router::post('(placeholder)/(:all)', 'Controllers\Welcome@index');
```
### Controller

#####smcontroller

```
namespace Controllers;

use Core\View;
use Core\Controller;

/*
*
* class_name controller
*/
class class_name extends Controller
{

    /**
     * Call the parent construct
     */
    public function __construct()
    {
        parent::__construct();
    }

    /**
     * Define Index method
     */
    public function index()
    {

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
View::renderTemplate('header', $data);
View::render('(placeholder)/(placeholder)', $data);
View::renderTemplate('footer', $data);
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
use Core\View;
```

#####smalias

```
use Helpers\(placeholder);
```

#####smfun

```
public function (placeholder)((placeholder)){
	(placeholder)
}
```

#####smdbselect

```
$this->db->select("SELECT * FROM ".PREFIX."(placeholder)"(placeholder));
```

#####smdbinsert

```
$this->db->insert(PREFIX.'(placeholder)',$data);
```

#####smdblastid

```
$this->db->lastInsertId('(placeholder)');
```

#####smdbupdate

```
$this->db->update(PREFIX.'(placeholder)',$data, $where);
```

#####smdbdelete

```
$this->db->delete(PREFIX.'(placeholder)',$data);
```

#####smdbtrun

```
$this->db->truncate($table);
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


#####smassetscss

```
Assets::css('(placeholder)');
```

#####smassetsjs

```
Assets::js('(placeholder)');
```

#####smcsrfmaketoken

```
Csrf::makeToken();
```

#####smcsrfistokenvalid

```
Csrf::isTokenValid();
```


#####Data
* [Data print_r](#smdatapr)
* [Data strlen](#smdatasl)
* [Data strtolower](#smdatastl)
* [Data stringtoupper](#smdatastu)
* [Data ucwords](#smdataucw)
* [Data var_dump](#smdatavd)

#####smdatapr

```
Data::pr('(placeholder)');
```

#####smdatasl

```
Data::sl('(placeholder)');
```

#####smdatastl

```
Data::stl('(placeholder)');
```

#####smdatastu

```
Data::stu('(placeholder)');
```

#####smdataucw

```
Data::ucw('(placeholder)');
```

#####smdatavd

```
Data::vd('(placeholder)');
```

#####smurlautolink

```
Url::autolink('(placeholder)' (placeholder));
```

#####smurltemppath

```
Url::templatePath();
```

#####smurlprev

```
Url::previous();
```

#####smurlredirect

```
Url::redirect('(placeholder)');
```

#####smurlgeneratesafeslug

```
Url::generateSafeSlug('(placeholder)');
```

#####smurlsegments

```
Url::segments();
```

#####smurlgetsegment

```
Url::getSegment('(placeholder)', '(placeholder)');
```

#####smurlfirstsegment

```
Url::firstSegment('(placeholder)');
```

#####smurllastsegment

```
Url::lastSegment('(placeholder)');
```

#####smsesset

```
Session::set('(placeholder)','(placeholder)');
```

#####smsespull

```
Session::pull('(placeholder)');
```

#####smsesget

```
Session::get('(placeholder)');
```

#####smsesid

```
Session::id();
```

#####smsesdisplay

```
Session::display();
```

#####smsesdestroy

```
Session::destroy('(placeholder)');
```
