# Monkey Speak Extended Script Engine
This is a fork of Squizles [Monkeyspeak](https://github.com/captkirk88/monkeyspeak)

## Description
MonkeySpeakEx is a dragonspeak-like interpreter written in C# 4.5. MonkeySpeakEx has a light footprint, less than 100kb size. Runtime memory usage is small making it very friendly in mobile environments.

## What is Monkey Speak?
Monkey Speak is a script language based on natural speech resembling [Furcadia&copy; Dragon Speak](http://www.furcadia.com/beekins/masons/knowledgebase/tds.html). It consists of causes, conditions and effects. 

``` Monkey Speak
(0:0) when the script is started,
    (5:250) create a table as %myTable.
    (5:100) set %hello to {hi}
    (5:101) set %i to 0
    (5:252) with table %myTable put {%hello} in it at key {myKey1}.
    (5:252) with table %myTable put {%hello} in it at key {myKey2}.
    (5:252) with table %myTable put {%hello} in it at key {myKey3}.
    (5:252) with table %myTable put {%hello} in it at key {myKey4}.
    (5:252) with table %myTable put {%hello} in it at key {myKey5}.
    (5:252) with table %myTable put {%hello} in it at key {myKey6}.
    (5:252) with table %myTable put {%hello} in it at key {myKey7}.
    (6:250) for each entry in table %myTable put it into %entry,
        (5:102) print {%entry} to the console.
        (5:150) take variable %i and add 1 to it.
        (5:102) print {%i} to the console.
    (6:454) after the loop is done,
        (5:102) print {I'm Mr. Meeseeks, look at me!} to the console.

(0:0) when the script is started,
    (5:101) set %answer to 0
    (5:101) set %life to 42
    (6:450) while variable %answer is not %life,
        (5:150) take variable %answer and add 1 to it.
        (1:102) and variable %answer equals 21,
            (5:450) exit the current loop.
    (6:454) after the loop is done,
        (5:102) print {I'm Mr. Meeseeks, look at me!} to the console.
```

The Engine loads the script into a new Page that contains the Triggers. Triggers can be compared to functions since they are used to perform a function in MonkeySpeakEx. Triggers are assigned specific TriggerHandlers (delegates) that are executed whenever the engine detects that trigger. Only one TriggerHandler delegate is assigned per Trigger.

## Features

* Native supported data types (string, double) 
* Local variable scope per Page 
* Multiple conditional statements using (1:##) triggers 
* [Default libraries](https://starship-avalon-projects.github.io/MonkeySpeakExtendedEngine/html/f0801825-eba4-44b1-4629-82ca22d81e8a.htm) Sys, IO, Math, Debug, Timers 
* Easy to extend by extending [AbstractBaseLibrary](https://starship-avalon-projects.github.io/MonkeySpeakExtendedEngine/html/16b41a55-314a-c426-9aaf-22da47e8e065.htm) or attaching TriggerHandlerAttribute to a method 
* Compilable scripts for faster loading or sending over the network 
* Thread safe, can execute multiple pages asynchronously. (beta) 
* EXE compiler (beta)
* Loops
* Tables

## Examples
The Red-Laser eyed [Furcadia&copy;](http://cms.furcadia.com) bot,

[Silver Monkey](http://silvermonkey.tsprojects.org)

## Apache License
Version 2.0, January 2004
http://www.apache.org/licenses/

## Disclaimer
The project "MonkeySpeakEx" and it's development team is in no way affiliated with Dragon's Eye Productions or [Catnip Studios](https://www.catnipstudios.com/). MonkeySpeakEx is free for life. Free as in FREE BEER!!

_Important:_ MonkeySpeakEx's compiled file format is not compatible with Dragon Speak's compiled file format.
