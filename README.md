# Readme
Remove all roles from an inactive user : 
When a user in an instance is inactive, it's a good practice to remove all roles assigned to that user. Following piece of code helps to remove all the roles from the inactive user.
~~~
var gr = new GlideRecord('sys_user_has_role');
gr.addEncodedQuery('user.active=false');
gr.query();
gr.deleteMultiple();
~~~
