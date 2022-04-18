# Action Blocks

Action blocks are used to, as the name implies, perform a certain pre-written action. We'll look at different types ad what they do.

Note that these blocks can technically be placed anywhere in the tag, however, it is a good practise to put them either at the beginning or the end of the code.

## Miscellaneous

### Delete
```diff
Deletes the message that triggered the tag.
+ Usage:
{del}
{delete}
```

### Silence
```diff
Prevents the output of a command ran in a command block from being displayed. (More on command blocks a bit further down...)
+ Usage:
{silent}
{silence}
```

### Override
```diff
Allows a user to run a command in a command block even though they would normally not have the permission to do so (running the command in the chat)
+ Usage:
{override}
```

## Redirects

### DMs
```diff
Redirects the tag output to the DMs of the user. This cannot be used to send DMs to someone who didnt execute the tag.
+ Usage:
{dm}
```

### Channels
```diff
Redirects to tag output to the specified channel.
+ Usage:
{redirect:channelID}
```

## Restrictions

*Note that ``errorMessage`` is an optional parameter*

### Require
```diff
This makes sure that the tag user either has a certain role or that the tag is ran in a specified channel. When supplying channel and role, make sure the channel is the first thing specified. When supplying channel and role, the tag will execute as long as one condition is met.
+ Usage:
{require(errorMessage):channelID}
{require(errorMessage):roleID}
{require(errorMessage):channelID, roleID}
```

### Blacklist
```diff
This makes sure that the tag user doesnt have a certain role or that the tag is NOT ran in a specified channel. When supplying channel and role, make sure the channel is the first thing specified. The tag will only execute when both conditions are not met (meaning the user doesnt have the role and the tag is not run in the channel).
+ Usage:
{require(errorMessage):channelID}
{require(errorMessage):roleID}
{require(errorMessage):channelID, roleID}
```

## Reactions
React blocks are used to apply reactions to a tag output or the message that triggered the tag.

Regular users can only use one react emoji per tag, in order to increase the limit to five, you have to buy Carl-Bot premium.
```diff
+ Usage:
{react: :dog:}                    --> reacts with a dog emoji to the tag output message
{reactu: :cat:}                   --> reacts with a cat emoji to the message that triggered the tag
```

## Command Blocks

Command blocks are used to execute regular commands you could also enter in the chat. They can only execute the command in them if the command is normally enabled and the user has the permission to use it. A bypass to this would be the ``override`` block.

Regular users can only use one command block per tag, in order to increase the limit to three, you have to buy Carl-Bot premium.
```diff
+ Usage:
{command: echo Hello!}                  --> acts like the tag user would put "echo Hello!" as command in the chat
{cmd: pick Pasta, Pizza, Burger}        --> acts like the tag user would put "pick Pasta, Pizza, Burger" as command in the chat
{c: level}                              --> acts like the tag user would put "level" as command in the chat
```