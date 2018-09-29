# strict
[![GitHub license](https://img.shields.io/github/license/MWH-json/strict.svg)](https://github.com/MWH-json/strict/blob/master/LICENSE)

Mini World Plugin Style Guide for **strict** Mini Developers!

***just to clarify, this style guide will be our new style guide for future plugin pack, our old plugin packs will not be updated with this style guide because of time***

## Overview

* Plugins
  * Comments in useless/not used keys are allowed.
  * Not using spaces in keys is not allowed.
  * Every new object should be separated/have a line break.
  * Your Plugins should have a custom File Name that describes the Plugin itself.
  * and basically [this](https://www.ietf.org/rfc/rfc4627.txt).

## Table of Contents

* [Getting Started](#getting-started)
* [Plugin](#plugin)
  * [Comments](#comments)
  * [Spaces](#spaces)
  * [Objects](#objects)
  * [File Names](#file-names)

## Getting Started

If you're going to use **strict** for your next open-source Plugin Pack, you should use one of the badges below:

> Original
[![strict Plugin Style](https://img.shields.io/badge/plugin_style-strict-red.svg)](https://github.com/MWH-json/strict)
```url
[![strict Plugin Style](https://img.shields.io/badge/plugin_style-strict-red.svg)](https://github.com/MWH-json/strict)
```

> Material
[![strict Plugin Style](https://img.shields.io/badge/plugin_style-strict-red.svg?longCache=true&style=flat-square)](https://github.com/MWH-json/strict)
```url
[![strict Plugin Style](https://img.shields.io/badge/plugin_style-strict-red.svg?longCache=true&style=flat-square)](https://github.com/MWH-json/strict)
```

---

## Plugin

### Comments

Normally, JSON **doesn't** support comments in JSON Files, but you can add new **useless** JSON keys to add your own comments, **only** to declare what your plugin does:

> good
```json
{
"//": "this line will be not executed, yay!",
  "foreign_ids": [],
  
	"mod_desc": {
		"author": "1000872134",
		"filename": "hello-world",
		"uuid": "87e5bf17-40b0-47ab-8388-0db79a120c76",
		"version": "1"
	},
  
	"property": {
		"copyid": 10100,
		"describe": "Hello World!",
		"icon": "minicoin",
		"id": 100004,
		"model": "minicoin",
		"name": "Coin",
		"stack_max": 10000
   	}
   
}
```

> bad
```json
{
//this line will raise an error and the plugin would be not executed, not yay.
  "foreign_ids": [],
  
	"mod_desc": {
		"author": "1000872134",
		"filename": "hello-world",
		"uuid": "87e5bf17-40b0-47ab-8388-0db79a120c76",
		"version": "1"
	},
  
	"property": {
		"copyid": 10100,
		"describe": "Hello World!",
		"icon": "minicoin",
		"id": 100004,
		"model": "minicoin",
		"name": "Coin",
		"stack_max": 10000
   	}
   
}
```

### Spaces

**strict** doesn't like that you don't use spaces in your keys, because the spaces give readability to your object, try to use them in every key.

> good
```json
{
  "foreign_ids": [],
  
	"mod_desc": {
		"author": "1000872134",
		"filename": "hello-world",
		"uuid": "87e5bf17-40b0-47ab-8388-0db79a120c76",
		"version": "1"
	},
  
	"property": {
		"copyid": 10100,
		"describe": "Hello World!",
		"icon": "minicoin",
		"id": 100004,
		"model": "minicoin",
		"name": "Coin",
		"stack_max": 10000
   	}
   
}
```

> bad
```json
{
  "foreign_ids":[],
  
	"mod_desc":{
		"author":"1000872134",
		"filename":"hello-world",
		"uuid":"87e5bf17-40b0-47ab-8388-0db79a120c76",
		"version":"1"
	}, 
  
  	"property":{
		"copyid":10100,
		"describe":"Hello World!",
		"icon":"minicoin",
		"id":100004,
		"model":"minicoin",
		"name":"Coin",
		"stack_max":10000
   	}
   
}
```

### Objects

Your Plugins should have their objects separated by a line break.

> good
```json
{
  "foreign_ids": [],
  
	"mod_desc": {
		"author": "1000872134",
		"filename": "hello-world",
		"uuid": "87e5bf17-40b0-47ab-8388-0db79a120c76",
		"version": "1"
	},
  
	"property": {
		"copyid": 10100,
		"describe": "Hello World!",
		"icon": "minicoin",
		"id": 100004,
		"model": "minicoin",
		"name": "Coin",
		"stack_max": 10000
   	}
   
}
```

> bad
```json
{
  "foreign_ids": [],
	"mod_desc": {
		"author": "1000872134",
		"filename": "hello-world",
		"uuid": "87e5bf17-40b0-47ab-8388-0db79a120c76",
		"version": "1"
	},
	"property": {
		"copyid": 10100,
		"describe": "Hello World!",
		"icon": "minicoin",
		"id": 100004,
		"model": "minicoin",
		"name": "Coin",
		"stack_max": 10000
   	}
}
```

### File Names

Your Plugins should have a custom File Name that replaces the one that is generated automatically by the game, this to have a better Plugin managing in your Project.

> good (file is called hello-world.json)
```json
{
  "foreign_ids": [],
  
	"mod_desc": {
		"author": "1000872134",
      		"//": "All good, the filename is hello-world!",
		"filename": "hello-world",
		"uuid": "87e5bf17-40b0-47ab-8388-0db79a120c76",
		"version": "1"
	},
	
	"property": {
		"copyid": 10100,
		"describe": "Hello World!",
		"icon": "minicoin",
		"id": 100004,
		"model": "minicoin",
		"name": "Coin",
		"stack_max": 10000
   	}
   
}
```

> bad (file is called 2943803856.json)
```json
{
  "foreign_ids": [],
  
	"mod_desc": {
		"author": "1000872134",
      		"//": "Bad, bad, bad! The filename has the automatic generated filename.",
		"filename": "2943803856",
		"uuid": "87e5bf17-40b0-47ab-8388-0db79a120c76",
		"version": "1"
	},
  
	"property": {
		"copyid": 10100,
		"describe": "Hello World!",
		"icon": "minicoin",
		"id": 100004,
		"model": "minicoin",
		"name": "Coin",
		"stack_max": 10000
   	}
   
}
```
