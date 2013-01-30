---
title: GridGroupable
slug: php-ui-gridgroupable
tags: api, php
publish: true
---

# \Kendo\UI\GridGroupable

A PHP class representing the groupable setting of Grid.


## Methods

### messages

Sets the messages displayed during grouping.

#### Returns
`\Kendo\UI\GridGroupable`

#### Parameters

##### $value `\Kendo\UI\GridGroupableMessages|array`


#### Example - using [\Kendo\UI\GridGroupableMessages](/api/wrappers/php/kendo/ui/gridgroupablemessages)

    $groupable = new \Kendo\UI\GridGroupable();
    $messages = new \Kendo\UI\GridGroupableMessages();
    $empty = 'value';
    $messages->_empty($empty);
    $groupable->messages($messages);

#### Example - using array

    $groupable = new \Kendo\UI\GridGroupable();
    $empty = 'value';
    $groupable->messages(array('empty' => $empty));
