atk4-boot-template
==================

A bootstrap template for Agile toolkit 4

![Alt text](/aboot-template.png "Optional title")

To utilize most of the template you have to add xavoc-addons to your application root ie

Your_Application
|-atk4
|-atk4-addons
|-xavoc-addons
|-lib
	|-Frontent.php
|-config-default.php
|-index.php

....

Now paste the following code in you Frontend to use xavoc-addons

        $this->addLocation('.',array(
            "addons"=>'xavoc-addons'
        ));

After 

		$this->addLocation('atk4-addons',array(
                    'php'=>array(
                        'mvc',
                        'misc/lib',
                        'filestore/lib',
                        )
                    ))
        ->setParent($this->pathfinder->base_location);

Now instead of using simple Atk4 Menu you just have to 'boot/Menu' ie

in Frontend.php => init() function add menus

	$m=$this->add('boot/Menu',array('fixed_top'=>true),'Menu');  
    $m->addMenuItem('index','Home');
    $m->addMenuItem('aboutus','About Xavoc');
    $m->addMenuItem('products','Products');
    $m->addMenuItem('services','Services');
    $m->addMenuItem('contactus','Contact Us');
    $m->setBrand('Xavoc <br/>International'); // <== This is new function added to set Brand

and for now thats it ... Working on the template so right now its on less but once completed template will be converted to css 

