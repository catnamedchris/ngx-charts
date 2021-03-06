# Normalized Area Chart

## Normalized Area Chart

{% embed data="{\"url\":\"https://embed.plnkr.co/ULbzY7ZmdugBRrb8SgdQ?show=preview\",\"type\":\"rich\",\"title\":\"Normalized Area Chart\",\"description\":\"Created on Plnkr: Helping developers build the web.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://embed.plnkr.co/favicon.ico\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://shot.plnkr.co/ULbzY7ZmdugBRrb8SgdQ.png?d=2017-03-31T15:21:32.474Z\",\"width\":400,\"height\":300,\"aspectRatio\":0.75},\"embed\":{\"type\":\"reader\",\"url\":\"https://embed.plnkr.co/plunk/ULbzY7ZmdugBRrb8SgdQ?autoCloseSidebar&deferRun&show=preview\",\"html\":\"<div style=\\"left: 0; width: 100%; height: 0; position: relative; padding-bottom: 66.6667%;\\"><iframe src=\\"https://embed.plnkr.co/plunk/ULbzY7ZmdugBRrb8SgdQ?autoCloseSidebar&amp;deferRun&amp;show=preview\\" style=\\"border: 0; top: 0; left: 0; width: 100%; height: 100%; position: absolute;\\" allowfullscreen scrolling=\\"no\\"></iframe></div>\",\"aspectRatio\":1.5}}" %}

## Inputs

| Property              | Type               | Default Value | Description                                                                                                                      |
| --------------------- | ------------------ | ------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| view                  | number\[\]         |               | the dimensions of the chart \[width, height\]. If left undefined, the chart will fit to the parent container size                |
| results               | object\[\]         |               | the chart data                                                                                                                   |
| scheme                | object             |               | the color scheme of the chart                                                                                                    |
| schemeType            | string             | 'ordinal'     | the color scale type. Can be either 'ordinal' or 'linear'                                                                        |
| customColors          | function or object |               | custom colors for the chart. Used to override a color for a specific value                                                       |
| animations            | boolean            | true          | enable animations                                                                                                                |
| legend                | boolean            | false         | show or hide the legend                                                                                                          |
| legendTitle           | string             | 'Legend'      | the legend title                                                                                                                 |
| legendPosition        | string             | 'right'       | the legend position ['right', 'below']                                                                                           |
| xAxis                 | boolean            | false         | show or hide the x axis                                                                                                          |
| yAxis                 | boolean            | false         | show or hide the y axis                                                                                                          |
| showGridLines         | boolean            | true          | show or hide the grid lines                                                                                                      |
| roundDomains          | boolean            | false         | round domains for aligned gridlines                                                                                              |
| showXAxisLabel        | boolean            | false         | show or hide the x axis label                                                                                                    |
| showYAxisLabel        | boolean            | false         | show or hide the y axis label                                                                                                    |
| xAxisLabel            | string             |               | the x axis label text                                                                                                            |
| yAxisLabel            | string             |               | the y axis label text                                                                                                            |
| xAxisTickFormatting   | function           |               | the x axis tick formatting                                                                                                       |
| yAxisTickFormatting   | function           |               | the y axis tick formatting                                                                                                       |
| xAxisTicks            | any\[\]            |               | predefined list of x axis tick values                                                                                            |
| yAxisTicks            | any\[\]            |               | predefined list of y axis tick values                                                                                            |
| timeline              | boolean            | false         | display a timeline control under the chart. Only available if x scale is date                                                    |
| autoScale             | boolean            | false         | set the minimum value of the y axis to the minimum value in the data, instead of 0                                               |
| curve                 | function           |               | the interpolation function used to generate the curve. It accepts any [d3.curve](https://github.com/d3/d3-shape#curves) function |
| gradient              | boolean            | false         | fill elements with a gradient instead of a solid color                                                                           |
| activeEntries         | object\[\]         | \[\]          | elements to highlight                                                                                                            |
| tooltipDisabled       | boolean            | false         | show or hide the tooltip                                                                                                         |
| tooltipTemplate       | TemplateRef        |               | a custom ng-template to be displayed inside the tooltip when hovering a single point                                             |
| seriesTooltipTemplate | TemplateRef        |               | a custom ng-template to be displayed inside the tooltip when hovering series                                                     |

## Outputs

| Property   | Description                                |
| ---------- | ------------------------------------------ |
| select     | click event                                |
| activate   | element activation event \(mouse enter\)   |
| deactivate | element deactivation event \(mouse leave\) |

## Data Format

The data format is multi series:

```text
[
  {
    "name": "Germany",
    "series": [
      {
        "name": "2010",
        "value": 7300000
      },
      {
        "name": "2011",
        "value": 8940000
      }
    ]
  },

  {
    "name": "USA",
    "series": [
      {
        "name": "2010",
        "value": 7870000
      },
      {
        "name": "2011",
        "value": 8270000
      }
    ]
  }
]
```
