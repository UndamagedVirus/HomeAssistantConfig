
# node-red-contrib-bool-gate [![npm version](https://img.shields.io/npm/v/node-red-contrib-bool-gate.svg?style=flat)](https://www.npmjs.org/package/node-red-contrib-bool-gate) [![npm downloads](https://img.shields.io/npm/dm/node-red-contrib-bool-gate.svg?style=flat)](https://www.npmjs.org/package/node-red-contrib-bool-gate) [![Unlicense](https://img.shields.io/badge/un-license-green.svg?style=flat)](http://unlicense.org)

Node RED node to include boolean logic gates.

## Installation

```bash
$ npm install node-red-contrib-bool-gate
```

Restart Node-RED and use the node!

Or from the Node-RED's palette, search for "node-red-contrib-bool-gate".

Check example at "Import > Examples > boolean logic"

### Boolean condition

If you know how the boolean logic work, you can skip this section.

The boolean logic is a way to determine a condition regarding to the input.

|Condition A|Condition B|AND|NAND|OR|NOR|XOR|XNOR
|-|-|-|-|-|-|-|-|
|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>
|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>
|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>
|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>

You can do it to for more than 2 condition :

|Condition A|Condition B|Condition C|AND|NAND|OR|NOR|XOR|XNOR
|-|-|-|-|-|-|-|-|-|
|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>
|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>
|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>
|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>
|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>
|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>
|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>
|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: #cf4343;text-align : center; font-weight : bold; padding : 0px 5px;">false</div>|<div style="color:white;background-color: green;text-align : center; font-weight : bold; padding : 0px 5px;">true</div>

 [You can follow this link to learn more about the boolean logic.](https://en.wikipedia.org/wiki/Boolean_algebra)

## Usage

### Notion of Rules

A rule can be read from top, like :

&lt;**TOPIC**&gt;&lt;**PROPERTY**&gt;&lt;**CONDITION**&gt;&lt;**VALUE**&gt;

with topic, the topic of incomming message (if needed), property to perform the test, condition the condition you want for the property and value the value you want for the property (if needed).

You can pick property from everywhere :
* from the incomming message
* from the flow context
* from the global context

The following condition are implemented :
* ==
* !=
* &lt;
* &lt;=
* &gt;
* &gt;=
* is between
* contains
* match regex
* is true
* is false
* is null
* is not null

You can pick value from the following type (depending on your condition) :
* number
* string
* message's property
* flow's property
* global's property
* regex
* previous value

## Configuration

Please take you time to create your gate, by following these steps :

* Select the **type of gate** you want for your node (between AND and NAND for the and-gate and OR, NOR, XOR and XNOR for the or-gate)
* Tick the "**True restriction**" checkbox if you want to have output only when the gate is at true state.
* Fill if needed the "**Input message topic**" input to filter your incomming message
* Select the **property** you need to check (Default : **msg**, assuming you defined the input message topic)
* Select the **condition**(Defautl : **=**)
* Type the **value** you want for your property, assuming you picked up the correct type
* Add a rule by cliking on **+ add** below the list, and repeat the procedure 

**See the node information for more details**
