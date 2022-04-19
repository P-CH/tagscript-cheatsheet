# Default Variables and Discord Objects

## Default Variables
```diff
{unix}          --> 10 digits of the current UNIX time
{uses}          --> number of times the tag has been used
{message}       --> all arguments after the prefix and tag name
{args}          --> same as {message}, more on that down below...
+ Examples:
{unix}          --> returns something like 1650368829
{uses}          --> returns something like 23
    Now lets imagine the message someone sent was "!tag hello everyone!" with "!" being the prefix and "tag" being the tag name.
{message}       --> returns "hello everyone!"
{args}          --> same as {message}
```

### About {message} and {args}
These two come with more than you think...

Firstly, you need to know that they are indexable. That means you can get a certain argument (arguments are words or numbers seperated by spaces in this case) by supplying an index number.
```diff
+ Example:
Lets say the command used was "!tag this is a test".
{message} or {args}         --> "this is a test"
{message(1)} or {args(1)}   --> "this"
{message(4)} or {args(4)}   --> "test"
```
Instead of typing out these long blocks, there is a shorter way to do the same thing. Please note that this shortcut is based on the ``{message}`` block (this could be important if you overwrite the default variables with your own...).
```diff
+ Exmaple:
Using the same string as before, we can do:
{1}         --> "this"
{4}         --> "test"
```

## Discord Variables
Lets take a look at the basic usage first...
```
{user}      --> the nickname of the user who ran the tag
{target}    --> the nickname of the user who was mentioned with the tag (if no user is mentioned, this is the same as {user})
{server}    --> the name of the server
{channel}   --> the name of the channel
```
Knowing these, you can access more specific information. The general structure of the blocks is ``{variable(property)}``. For the sake of keeping the following section as short as possible, there will just be the properties without their surrounding block...

### {user} and {target}
```
avatar      --> links to the users avatar
icon        --> same as avatar
id          --> the users Discord ID
mention     --> used to ping the user with it
created_at  --> date and time the account was created
joined_at   --> date and time the user joined the server
color       --> hexadecimal color value of the users highest role
name        --> the users name, not nickname
proper      --> the users name and their discriminator
roleids     --> list of IDs for all roles the user has, starting with the lowest role
position    --> the users "hierarchy level", the position of the users highest role (starting with 0 at @everyone)
```

### {server}
```
icon        --> link to the servers icon
id          --> the servers ID
owner       --> username and discriminator of the server owner
random      --> username and discriminator of a random user in the server
members     --> amount of members in the server
roles       --> amount of roles in the server
channels    --> amount of channels in the server
created_at  --> date and time the server was created
```

### {channel}
```
id          --> the channels ID
topic       --> the channels topic
slowmode    --> the channels current slowmode
position    --> the channels position in the channel creation timeline (starting with 0 for the first channel created in the server)
mention     --> clickable referral link to the channel
```