# [MenheraChanRobot](https://t.me/MenheraChanrobot)

## Intro


A modular telegram Python bot running on python3 with an sqlalchemy database.

Originally a simple group management bot with multiple admin features, it has evolved, becoming extremely modular and 
simple to use.

Can be found on telegram as [Menhera](https://t.me/menherachanRobot).

Menhera and I are moderating a [support group](https://t.me/MenherachanSupport), where you can ask for help setting up your
bot, discover/request new features, report bugs, and stay in the loop whenever a new update is available. Of course
I'll also help when a database schema changes, and some table column needs to be modified/added. Note to maintainers that all schema changes will be found in the commit messages, and its their responsibility to read any new commits.

Join the [Tech channel](https://t.me/Dark_Hacker_X) For Free Knowledge.

Alternatively, [find me on telegram](https://t.me/TheDarkW3b)! (Keep all support questions in the support chat, where more people can help you.)

This Bot Is Made By [@TheDarkW3b](https://t.me/TheDarkW3b)

Special Thanks To [@RealAkito](https://t.me/realakito) for [HarukaAya](https://t.me/harukaayabot) and MrYacha For Sophie❤️

## Modules

### Setting load order.

The module load order can be changed via the `LOAD` and `NO_LOAD` configuration settings.

These should both represent lists.

If `LOAD` is an empty list, all modules in `modules/` will be selected for loading by default.

If `NO_LOAD` is not present, or is an empty list, all modules selected for loading will be loaded.

If a module is in both `LOAD` and `NO_LOAD`, the module will not be loaded - `NO_LOAD` takes priority.

### Creating your own modules.

Creating a module has been simplified as much as possible - but do not hesitate to suggest further simplification.

All that is needed is that your .py file be in the modules folder.

To add commands, make sure to import the dispatcher via

`from menhera import dispatcher`.

You can then add commands using the usual

`dispatcher.add_handler()`.

Assigning the `__help__` variable to a string describing this modules' available

commands will allow the bot to load it and add the documentation for

your module to the `/help` command. Setting the `__mod_name__` variable will also allow you to use a nicer, user

friendly name for a module.

The `__migrate__()` function is used for migrating chats - when a chat is upgraded to a supergroup, the ID changes, so 

it is necessary to migrate it in the db.

The `__stats__()` function is for retrieving module statistics, eg number of users, number of chats. This is accessed 

through the `/stats` command, which is only available to the bot owner.
