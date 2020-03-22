# Control Block

## Description

* Control blocks are used to distinguish standard HTML input elements from Sodium input elements in a [Form File](../program-structure/form-file.md).
* Control blocks cannot be nested.
* Sodium CSS rules only applies to input elements in Control Block and Data Block elements.
* Sodium event/triggers only applies to input elements in Control Block and Data Block elements.
* Control block's name is mandatory and must be unique in a form file.

## Declaration

```text
<controlblock
    control-block-name  = "">
</controlblock>
```

## Properties

###  control-block-name property

 **Mandatory :** yes  
 **Unique :** yes  
 **Data Type :** char  
 **Default Value:** -  
 **Predefined Values Allowed:** -

## Triggers

None

## Allowed Inner HTML Elements

 Standard HTML Tags  
 [Inputs](inputs/)  
 [Tree Element](tree-element.md)

## Built-in Functions

