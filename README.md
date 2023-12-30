### Introduction
```
Methods to transform Data
Methods to draw on web pages
```

### D3 APIs

1. Transform Data
```
d3.cross
d3.max
```

2. Map data to Image Space
```
d3.scaleLinear
d3.scaleTime
```

3. Compute Layouts and Paths
```
d3.path
d3.treemap
```

4. draw the chart
```
d3.select
d3.append
```

```
d3.select("HTML TAG | ID | CLASS | CSS SELECTOR ")
d3.selectAll(selector)

let selection = d3.select("p").select(".main")
let selection = d3.selectAll("p").selectAll(".main")


```


### Data to DOM Elements 

Data points to DOM

### SVG

```
<svg width="400" height="110">
    <rect width="300" height="100"/>
</svg>

<svg width="400" height="110">
    <circle cx="50" cy="50" r="40"/>
</svg>

<svg width="400" height="110">
    <line x1="0" y1="0" x2="200" y2="200"/>
</svg>

<svg width="400" height="110">
    <path d="M150 0 L75 200 L225 200 Z"/>
</svg>
```

### D3 Blocks and Observable

* Blocks gist ,version < 4
* Observale jupyter notebooks , new

### Setup

npm node-static

### D3 Methods

> .select() and .selectall()
to target an HTML Element

> .append()
to attach new element to the DOM

> .text()/.html()
to add content 

### Scale

> .scaleLinear()
linear scale

> .scaleTime()
time scale

> .scalePow() / .scaleSqrt() / .scaleLog()
power , squareroot, log scale 

> .scaleQuantize() / .scaleQuantile() / .scaleThreshold()
quantize, quantile , threshold 

> .scaleSequential() / .scaleDiverging()
sequential / diverging 

```
d3.scaleSequential(d3.interpolateRainbow)
```

> .scaleOrdinal()
categorical , scatter

> .scaleBand()
categorical , bar chart 

### Domain and rage

> .domain([])
set of values

> .range([start,end])
return intervals of data placement 

```
.domain([]) --> input --> d3.scale --> output --> .range([])
```

* linearscale

```
[54,98,72,9,17,37,84,64]

.domain([9,98])
.range([0,980])
```

* threshold scale for chloropleth
```
[1.5K, 58.7K, 19.2K, 1.2K, 17.3K, 7.6K, 51.6K. 12.4K]

.domain([1200,58700])
.range(['light-purple','dark-purple'])

```

* ordinal , label scale 
```
['tennis','soccer','football','track','baseball']

.domain(['tennis','soccer',...])

.range([0,980])

```

### D3 Simplified 

JS
```
let dataArr = ['Data 1','Data 2','Data 3']

d3.select('body)
    .selectAll('div')
    .data(dataArr)
```

HTML
```
<body>
    <div>Data 1</div>
    <div>Data 2</div>
    <div>Data 3</div>
</body>
```

* if doesn know how many div to add etc

JS
```
d3.select('body')
    .selectAll('div')
    .data(dataArr)
    .enter()
    .append('div')
```

HTML
```
<body>
</body>
```
