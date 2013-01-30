---
title: StockChart
slug: php-dataviz-ui-stockchart
tags: api, php
publish: true
---

# \Kendo\Dataviz\UI\StockChart

A PHP class representing Kendo [StockChart](/api/web/stockchart).


## Usage

To use StockChart in a PHP page instantiate a new instance, configure it via the available
configuration [methods](#methods) and output it by `echo`-ing the result of the `render` method.

### Using Kendo StockChart

    <?php
    // Create a new instance of StockChart and specify its id
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');

    // Configure it
    $stockChart->autoBind(true)

    // Output it

    echo $stockChart->render();
    ?>


## Methods

### autoBind
Indicates whether the chart will call read on the data source initially.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `boolean`



#### Example 
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->autoBind(true);

### axisDefaults
Default options for all chart axes.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value ``



### axisLabelClick
Fires when an axis label is clicked.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->axisLabelClick('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onAxisLabelClick(e) {
            // handle the axisLabelClick event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->axisLabelClick('onAxisLabelClick');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->axisLabelClick(new \Kendo\JavaScriptFunction('function(e) { }'));

### addCategoryAxisItem

Adds one or more StockChartCategoryAxisItem to the StockChart.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value[, $value2, ...] `\Kendo\Dataviz\UI\StockChartCategoryAxisItem|array`

#### Example - using \Kendo\Dataviz\UI\StockChartCategoryAxisItem

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $categoryAxisItem = new \Kendo\Dataviz\UI\StockChartCategoryAxisItem();
    $baseUnit = 'value';
    $categoryAxisItem->baseUnit($baseUnit);
    $stockChart->addCategoryAxisItem($categoryAxisItem);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $baseUnit = 'value';
    $stockChart->addCategoryAxisItem(array('baseUnit' => $baseUnit));

#### Example - adding more than one StockChartCategoryAxisItem

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $first  = new \Kendo\Dataviz\UI\StockChartCategoryAxisItem();
    $second = new \Kendo\Dataviz\UI\StockChartCategoryAxisItem();
    $stockChart->addCategoryAxisItem($first, $second);

### chartArea

The chart area configuration options.
This is the entire visible area of the chart.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `\Kendo\Dataviz\UI\StockChartChartArea|array`


#### Example - using [\Kendo\Dataviz\UI\StockChartChartArea](/api/wrappers/php/kendo/dataviz/ui/stockchartchartarea)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $chartArea = new \Kendo\Dataviz\UI\StockChartChartArea();
    $background = 'value';
    $chartArea->background($background);
    $stockChart->chartArea($chartArea);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $background = 'value';
    $stockChart->chartArea(array('background' => $background));

### dataBound
Fires when the chart has received data from the data source
and is about to render it.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->dataBound('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onDataBound(e) {
            // handle the dataBound event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->dataBound('onDataBound');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->dataBound(new \Kendo\JavaScriptFunction('function(e) { }'));

### dataSource

Sets the data source of the dataSource.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `\Kendo\Data\DataSource|array`

#### Example - using [\Kendo\Data\DataSource](/api/wrappers/php/kendo/data/datasource)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $dataSource = new \Kendo\Data\DataSource();
    $stockChart->dataSource($dataSource);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $schema = new \Kendo\Data\DataSourceSchema();
    $stockChart->dataSource(array('schema' => $schema));

### dateField
The field containing the point date.
It is used as a default field for all date axes, including the navigator pane.The data item field value must be either:

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string`



#### Example 
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->dateField('value');

### drag
Fires as long as the user is dragging the chart using the mouse or swipe gestures.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->drag('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onDrag(e) {
            // handle the drag event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->drag('onDrag');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->drag(new \Kendo\JavaScriptFunction('function(e) { }'));

### dragEnd
Fires when the user stops dragging the chart.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->dragEnd('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onDragEnd(e) {
            // handle the dragEnd event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->dragEnd('onDragEnd');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->dragEnd(new \Kendo\JavaScriptFunction('function(e) { }'));

### dragStart
Fires when the user has used the mouse or a swipe gesture to drag the chart.The drag operation can be aborted by calling e.preventDefault().

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->dragStart('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onDragStart(e) {
            // handle the dragStart event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->dragStart('onDragStart');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->dragStart(new \Kendo\JavaScriptFunction('function(e) { }'));

### legend

The chart legend configuration options.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `\Kendo\Dataviz\UI\StockChartLegend|array`


#### Example - using [\Kendo\Dataviz\UI\StockChartLegend](/api/wrappers/php/kendo/dataviz/ui/stockchartlegend)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $legend = new \Kendo\Dataviz\UI\StockChartLegend();
    $background = 'value';
    $legend->background($background);
    $stockChart->legend($legend);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $background = 'value';
    $stockChart->legend(array('background' => $background));

### navigator

The data navigator configuration options.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `\Kendo\Dataviz\UI\StockChartNavigator|array`


#### Example - using [\Kendo\Dataviz\UI\StockChartNavigator](/api/wrappers/php/kendo/dataviz/ui/stockchartnavigator)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $navigator = new \Kendo\Dataviz\UI\StockChartNavigator();
    $autoBind = true;
    $navigator->autoBind($autoBind);
    $stockChart->navigator($navigator);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $autoBind = true;
    $stockChart->navigator(array('autoBind' => $autoBind));

### addPane

Adds one or more StockChartPane to the StockChart.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value[, $value2, ...] `\Kendo\Dataviz\UI\StockChartPane|array`

#### Example - using \Kendo\Dataviz\UI\StockChartPane

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $pane = new \Kendo\Dataviz\UI\StockChartPane();
    $background = 'value';
    $pane->background($background);
    $stockChart->addPane($pane);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $background = 'value';
    $stockChart->addPane(array('background' => $background));

#### Example - adding more than one StockChartPane

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $first  = new \Kendo\Dataviz\UI\StockChartPane();
    $second = new \Kendo\Dataviz\UI\StockChartPane();
    $stockChart->addPane($first, $second);

### plotArea

The plot area configuration options. This is the area containing the plotted series.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `\Kendo\Dataviz\UI\StockChartPlotArea|array`


#### Example - using [\Kendo\Dataviz\UI\StockChartPlotArea](/api/wrappers/php/kendo/dataviz/ui/stockchartplotarea)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $plotArea = new \Kendo\Dataviz\UI\StockChartPlotArea();
    $background = 'value';
    $plotArea->background($background);
    $stockChart->plotArea($plotArea);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $background = 'value';
    $stockChart->plotArea(array('background' => $background));

### plotAreaClick
Fires when plot area is clicked.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->plotAreaClick('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onPlotAreaClick(e) {
            // handle the plotAreaClick event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->plotAreaClick('onPlotAreaClick');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->plotAreaClick(new \Kendo\JavaScriptFunction('function(e) { }'));

### select
Fires when the user drags the drag handle to a new position.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->select('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onSelect(e) {
            // handle the select event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->select('onSelect');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->select(new \Kendo\JavaScriptFunction('function(e) { }'));

### selectEnd
Fires when the user stops dragging the drag handle.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->selectEnd('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onSelectEnd(e) {
            // handle the selectEnd event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->selectEnd('onSelectEnd');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->selectEnd(new \Kendo\JavaScriptFunction('function(e) { }'));

### selectStart
Fires when the user start to dragging the drag handle.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->selectStart('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onSelectStart(e) {
            // handle the selectStart event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->selectStart('onSelectStart');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->selectStart(new \Kendo\JavaScriptFunction('function(e) { }'));

### addSeriesItem

Adds one or more StockChartSeriesItem to the StockChart.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value[, $value2, ...] `\Kendo\Dataviz\UI\StockChartSeriesItem|array`

#### Example - using \Kendo\Dataviz\UI\StockChartSeriesItem

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $seriesItem = new \Kendo\Dataviz\UI\StockChartSeriesItem();
    $aggregate = 'value';
    $seriesItem->aggregate($aggregate);
    $stockChart->addSeriesItem($seriesItem);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $aggregate = 'value';
    $stockChart->addSeriesItem(array('aggregate' => $aggregate));

#### Example - adding more than one StockChartSeriesItem

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $first  = new \Kendo\Dataviz\UI\StockChartSeriesItem();
    $second = new \Kendo\Dataviz\UI\StockChartSeriesItem();
    $stockChart->addSeriesItem($first, $second);

### seriesClick
Fires when chart series are clicked.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->seriesClick('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onSeriesClick(e) {
            // handle the seriesClick event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->seriesClick('onSeriesClick');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->seriesClick(new \Kendo\JavaScriptFunction('function(e) { }'));

### seriesColors
The default colors for the chart's series. When all colors are used, new colors are pulled from the start again.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `array`



#### Example 
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->seriesColors(new array());

### seriesDefaults

Default values for each series.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `\Kendo\Dataviz\UI\StockChartSeriesDefaults|array`


#### Example - using [\Kendo\Dataviz\UI\StockChartSeriesDefaults](/api/wrappers/php/kendo/dataviz/ui/stockchartseriesdefaults)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $seriesDefaults = new \Kendo\Dataviz\UI\StockChartSeriesDefaults();
    $gap = 1;
    $seriesDefaults->gap($gap);
    $stockChart->seriesDefaults($seriesDefaults);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $gap = 1;
    $stockChart->seriesDefaults(array('gap' => $gap));

### seriesHover
Fires when chart series are hovered.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->seriesHover('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onSeriesHover(e) {
            // handle the seriesHover event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->seriesHover('onSeriesHover');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->seriesHover(new \Kendo\JavaScriptFunction('function(e) { }'));

### theme
Sets Chart theme. Available themes: default, blueOpal, black.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string`



#### Example 
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->theme('value');

### title

The chart title configuration options or text.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `\Kendo\Dataviz\UI\StockChartTitle|array`


#### Example - using [\Kendo\Dataviz\UI\StockChartTitle](/api/wrappers/php/kendo/dataviz/ui/stockcharttitle)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $title = new \Kendo\Dataviz\UI\StockChartTitle();
    $align = 'value';
    $title->align($align);
    $stockChart->title($title);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $align = 'value';
    $stockChart->title(array('align' => $align));

### tooltip

The data point tooltip configuration options.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `\Kendo\Dataviz\UI\StockChartTooltip|array`


#### Example - using [\Kendo\Dataviz\UI\StockChartTooltip](/api/wrappers/php/kendo/dataviz/ui/stockcharttooltip)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $tooltip = new \Kendo\Dataviz\UI\StockChartTooltip();
    $background = 'value';
    $tooltip->background($background);
    $stockChart->tooltip($tooltip);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $background = 'value';
    $stockChart->tooltip(array('background' => $background));

### transitions
A value indicating if transition animations should be played.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `boolean`



#### Example 
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->transitions(true);

### addValueAxisItem

Adds one or more StockChartValueAxisItem to the StockChart.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value[, $value2, ...] `\Kendo\Dataviz\UI\StockChartValueAxisItem|array`

#### Example - using \Kendo\Dataviz\UI\StockChartValueAxisItem

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $valueAxisItem = new \Kendo\Dataviz\UI\StockChartValueAxisItem();
    $color = 'value';
    $valueAxisItem->color($color);
    $stockChart->addValueAxisItem($valueAxisItem);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $color = 'value';
    $stockChart->addValueAxisItem(array('color' => $color));

#### Example - adding more than one StockChartValueAxisItem

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $first  = new \Kendo\Dataviz\UI\StockChartValueAxisItem();
    $second = new \Kendo\Dataviz\UI\StockChartValueAxisItem();
    $stockChart->addValueAxisItem($first, $second);

### addXAxisItem

Adds one or more StockChartXAxisItem to the StockChart.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value[, $value2, ...] `\Kendo\Dataviz\UI\StockChartXAxisItem|array`

#### Example - using \Kendo\Dataviz\UI\StockChartXAxisItem

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $xAxisItem = new \Kendo\Dataviz\UI\StockChartXAxisItem();
    $baseUnit = 'value';
    $xAxisItem->baseUnit($baseUnit);
    $stockChart->addXAxisItem($xAxisItem);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $baseUnit = 'value';
    $stockChart->addXAxisItem(array('baseUnit' => $baseUnit));

#### Example - adding more than one StockChartXAxisItem

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $first  = new \Kendo\Dataviz\UI\StockChartXAxisItem();
    $second = new \Kendo\Dataviz\UI\StockChartXAxisItem();
    $stockChart->addXAxisItem($first, $second);

### addYAxisItem

Adds one or more StockChartYAxisItem to the StockChart.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value[, $value2, ...] `\Kendo\Dataviz\UI\StockChartYAxisItem|array`

#### Example - using \Kendo\Dataviz\UI\StockChartYAxisItem

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $yAxisItem = new \Kendo\Dataviz\UI\StockChartYAxisItem();
    $baseUnit = 'value';
    $yAxisItem->baseUnit($baseUnit);
    $stockChart->addYAxisItem($yAxisItem);

#### Example - using array

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $baseUnit = 'value';
    $stockChart->addYAxisItem(array('baseUnit' => $baseUnit));

#### Example - adding more than one StockChartYAxisItem

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $first  = new \Kendo\Dataviz\UI\StockChartYAxisItem();
    $second = new \Kendo\Dataviz\UI\StockChartYAxisItem();
    $stockChart->addYAxisItem($first, $second);

### zoom
Fires as long as the user is zooming the chart using the mousewheel.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->zoom('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onZoom(e) {
            // handle the zoom event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->zoom('onZoom');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->zoom(new \Kendo\JavaScriptFunction('function(e) { }'));

### zoomEnd
Fires when the user stops zooming the chart.

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->zoomEnd('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onZoomEnd(e) {
            // handle the zoomEnd event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->zoomEnd('onZoomEnd');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->zoomEnd(new \Kendo\JavaScriptFunction('function(e) { }'));

### zoomStart
Fires when the user has used the mousewheel to zoom the chart.The zoom operation can be aborted by calling e.preventDefault().

#### Returns
`\Kendo\Dataviz\UI\StockChart`

#### Parameters

##### $value `string|\Kendo\JavaScriptFunction`

#### Example - using string which defines a JavaScript function

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->zoomStart('function(e) { }');

#### Example - using string which defines a JavaScript name
    <script>
        function onZoomStart(e) {
            // handle the zoomStart event.
        }
    </script>
    <?php
    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->zoomStart('onZoomStart');
    ?>

#### Example - using [\Kendo\JavaScriptFunction](/api/wrappers/php/kendo/javascriptfunction)

    $stockChart = new \Kendo\Dataviz\UI\StockChart('StockChart');
    $stockChart->zoomStart(new \Kendo\JavaScriptFunction('function(e) { }'));
