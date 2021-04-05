# 201 Day 12
[Back to Table of Contents](../reading-notes.md)<br/>

#### Today's Reading:<br/>

**Articles**: 
- [Chart.js](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)
- [Documentation](https://www.chartjs.org/docs/latest/)
- [Drawing Shapes](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)
- [Applying Styles](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)
- [Drawing Text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)


## Chart.js

Chart.js is a javascript plugin that programs the html `<canvas>` element.<br />

Here's a demo of this in use, pulled from [Sara Vieira on webdesignerdepot.com](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/):

```javascript
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <!-- import plugin script -->
        <script src='Chart.min.js'></script>
    </head>
    <body>
        <!-- line chart canvas element -->
        <canvas id="buyers" width="600" height="400"></canvas>
        <!-- pie chart canvas element -->
        <canvas id="countries" width="600" height="400"></canvas>
        <!-- bar chart canvas element -->
        <canvas id="income" width="600" height="400"></canvas>
        <script>
            // line chart data
            var buyerData = {
                labels : ["January","February","March","April","May","June"],
                datasets : [
                {
                    fillColor : "rgba(172,194,132,0.4)",
                    strokeColor : "#ACC26D",
                    pointColor : "#fff",
                    pointStrokeColor : "#9DB86D",
                    data : [203,156,99,251,305,247]
                }
            ]
            }
            // get line chart canvas
            var buyers = document.getElementById('buyers').getContext('2d');
            // draw line chart
            new Chart(buyers).Line(buyerData);
            // pie chart data
            var pieData = [
                {
                    value: 20,
                    color:"#878BB6"
                },
                {
                    value : 40,
                    color : "#4ACAB4"
                },
                {
                    value : 10,
                    color : "#FF8153"
                },
                {
                    value : 30,
                    color : "#FFEA88"
                }
            ];
            // pie chart options
            var pieOptions = {
                 segmentShowStroke : false,
                 animateScale : true
            }
            // get pie chart canvas
            var countries= document.getElementById("countries").getContext("2d");
            // draw pie chart
            new Chart(countries).Pie(pieData, pieOptions);
            // bar chart data
            var barData = {
                labels : ["January","February","March","April","May","June"],
                datasets : [
                    {
                        fillColor : "#48A497",
                        strokeColor : "#48A4D1",
                        data : [456,479,324,569,702,600]
                    },
                    {
                        fillColor : "rgba(73,188,170,0.4)",
                        strokeColor : "rgba(72,174,209,0.4)",
                        data : [364,504,605,400,345,320]
                    }
                ]
            }
            // get bar chart canvas
            var income = document.getElementById("income").getContext("2d");
            // draw bar chart
            new Chart(income).Bar(barData);
        </script>
    </body>
</html>
```

### Drawing Shapes

- fillRect(x, y, width, height)
- strokeRect(x, y, width, height)
- clearRect(x, y, width, height)
- beginPath()
- closePath()
- stroke()
- fill()
- arc(x, y, radius, startAngle, endAngle, anticlockwise)
- arcTo(x1, y1, x2, y2, radius)

### Applying Colors

- fillStyle = color
- strokeStyle = color
- lineWidth = value
- lineCap = type
- lineJoin = type
- miterLimit = value
- getLineDash()
- setLineDash
- lineDashOffset = value


## Drawing Text

- fillText(text, x, y [, maxWidth])
- strokeText(text, x, y [, maxWidth])
- font = value
- textAlign - value
- textBaseline = value
- direction = value
