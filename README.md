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
* [Assert CSS](#smcss)
* [Assert JS](#smjs)

#####Csrf (Cross Site Request Forgeries)
* [Csrf Make Token](#maketoken)
* [Csrf Is Token Valid](#istokenvalid)

#####Data
* [Data print_r](#smpr)
* [Data strlen](#smls)
* [Data strtolower](#smstl)
* [Data stringtoupper](#smstu)
* [Data ucwords](#smucw)
* [Data var_dump](#smvd)

#####Url
* [Url Autolink](#smautolink)
* [Url Template Path](#smtemppath)
* [Url Previous](#smprev)
* [Url Redirect](#smredirect)
* [Url Generate Safe Slug](#smgeneratesafeslug)
* [Url Segments](#smsegments)
* [Url Get Segment](#smgetsegment)
* [Url First Segment](#smfirstsegment)
* [Url Last Segment](#smlastsegment)

#####Session
* [Session Set](#smsetses)
* [Session Pull](#smpullses)
* [Session Get](#smgetses)
* [Session id](#smidses)
* [Session Display](#smdisplayses)
* [Session Destroy](#smdestroyses)


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


#####smcss

```
Assets::css('(placeholder)');
```

#####smjs

```
Assets::js('(placeholder)');
```

#####smmaketoken

```
Csrf::makeToken();
```

#####smistokenvalid

```
Csrf::isTokenValid();
```

#####smpr

```
Data::pr('(placeholder)');
```

#####smsl

```
Data::sl('(placeholder)');
```

#####smstl

```
Data::stl('(placeholder)');
```

#####smstu

```
Data::stu('(placeholder)');
```

#####smucw

```
Data::ucw('(placeholder)');
```

#####smvd

```
Data::vd('(placeholder)');
```

#####smautolink

```
Url::autolink('(placeholder)' (placeholder));
```

#####smtemppath

```
Url::templatePath();
```

#####smprev

```
Url::previous();
```

#####smredirect

```
Url::redirect('(placeholder)');
```

#####smgeneratesafeslug

```
Url::generateSafeSlug('(placeholder)');
```

#####smsegments

```
Url::segments();
```

#####smgetsegment

```
Url::getSegment('(placeholder)', '(placeholder)');
```

#####smfirstsegment

```
Url::firstSegment('(placeholder)');
```

#####smlastsegment

```
Url::lastSegment('(placeholder)');
```

#####smsetses

```
Session::set('(placeholder)','(placeholder)');
```

#####smpullses

```
Session::pull('(placeholder)');
```

#####smgetses

```
Session::get('(placeholder)');
```

#####smidses

```
Session::id();
```

#####smdisplayses

```
Session::display();
```

#####smdestroyses

```
Session::destroy('(placeholder)');
```
