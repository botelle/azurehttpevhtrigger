# azurehttpevhtrigger

Test the failure case of having separate http trigger and event hub trigger.

Using Visual Studio Code command palette, create a node typescript http trigger in a new directory
Using Visual Studio Code command palette, add a trigger for event hub.
change the event hub to use process.envf.(name) so that it won't complain about the connection string not being set when you deploy.
Using Visual Studio Code command palette, deploy to azure (having already changed that functions environment to include the referenced connection string)

You should get an error in app insights that :  The 'httpTrigger1' function is in error:  Multiple bindings with name 'httpTrigger624a61988c' discovered.  Binding names must be unique

