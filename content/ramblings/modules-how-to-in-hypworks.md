---
title: "Modules How-to in Hypworks"
date: 2006-06-07
tags: ["Frustrations"]
---

Before we proceed in the steps on how to create a module in Hypworks, let us first define Hypworks. So what is Hypworks? From its website which is located at http://hypworks.sourceforge.net, Hypworks is an MVC PHP framework designed to modularize and ease the development of web applications, together with various tools like Smarty and ADODB.

Now we have the definition out of the way, we can start now on how to make a module in Hypworks. Just a small reminder before proceeding that there are two types of
modules in Hypworks. They are the view module which consists of an optional logic
written in php and a view written in smarty and html and the action
module which consists of just the logic. Below is a summary of steps for both modules courtesy of Wigi and modified by me. These steps will be explained later.

View Module
1. Edit modules.ini
2. Create the Data Access Object (DAO)
3. Create the view module (convention is modulename.php)
4. Restrict the access for the module
5. Load the required DAO
6. Gather all the data you need to display or manipulate
7. Assign all variables to the template for displaying
8. Display the template
9. Edit the template
10. Test the module

Action Module
1. Edit modules.ini
2. Create the Data Access Object (DAO)
3. Create the action module (convention is modulename.action.php)
4. Restrict the access for the module
5. Load the required DAO
6. Manipulate data
7. Add error messages or success messages
8. Forward to a view module
9. Test the module

Since there are common steps for the two types of modules, we will just explain all the steps here and just put a note if it is specifically for the view module or the action modules. And now for the details.

Edit modules.ini

The modules.ini file is located at modules/modules.ini. It has the following syntax.
- [module name here] - module name is alphanumeric and should be inside square brackets. The convention for the name of the action module has ".do" as a suffix. For example, [login] is for the view module and [login.do] is for its corresponding action modules. This is required for both modules.
- title = "Title" - title will appear on the browser's title bar. This is optional and for view module only.
- path = "items/additem.php" for the view module and path = "items/additem.action.php" for the action module - path is, just as its name says, the path for the logic file. This is optional for view module but required for action module.
- body = "items/additem.tpl" - body is the path for the template file. This is optional and for view module only.
- template = "main.tpl" - template is the path for the master temaplte. This is optional and for view module only.

Create the Data Access Object (DAO)

DAOs are located at modules/dao/. The convention for naming DAOs is singulartablename.class.php. For example, you hava a table which has a name "Items" then its equivalent DAO is Item.class.php. The format for DAOs is


require_once APP_CORE . "/HypDao.class.php";

class Item extends HypDao {

// put your functions here

}

?>

Create the view module or the action module

This is just saving a file named modulename.php or modulename.action.php in the directory specified in path in modules.ini.

Restrict the access for the module

In restricting the user access for any module, we need to use the Hypworks function restrict(). Its usage is $this->restrict(USER_ADMIN, USER_VOTER); where USER_ADMIN and USER_VOTER is a global constants defined in modules/constants.php.

Load the required DAO

Loading the required DAO is just like the previous step but this time using the loadDao() function. Its usage is Hypworks::loadDao('Item'); where Item is a class name of a DAO which can be found at modules/dao/Item.class.php.

Gather all the data you need to display or manipulate or Manipulate data

This step is where the user logic comes in. You can, for example, retrieve data from the database using some functions from the DAO you loaded or insert data to the database and so on.

Assign all variables to the template for displaying (view module)

In this step, we will need to use another function of Hypworks which is the assign() function. Its usage is $this->assign(compact('variable', 'anothervariable'));. The assign function accepts an associative array of data. This means that $variable and $anothervariable should exist and is converted to an associative array using the php function compact. For more information on compact, please see http://php.net/compact.

Display the template (view module)

Displaying the template simply means that you put $this->display() into your view module logic.

Edit the template (view module)

In this step you should edit the template defined in body in modules.ini to make sure that the data you pass are displayed correctly.

Add error messages or success messages (action module)

This step is useful for passing messages to view modules. Hypworks has functions for this which are $this->addError('erroridentifier', 'Error message'); and $this->addMessage('messageidentifier', 'Message again');. You can also check if there are existing errors or messages by using $this->hasError() and $this->hasMessage(). These two functions return a boolean value.

Forward to a view module (action module)

This step uses the Hypworks function forward(). Its usage is $this->forward('something') where something is a module or a full URL. This function can also be used in view modules for redirecting it to other view modules.

Test the module







This step speaks for itself.

That's it. You can now create Hypworks modules. Next time, I will post examples of Hypworks modules.