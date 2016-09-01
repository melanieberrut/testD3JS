# testD3JS
testD3JS


## Data visualisation

### What is Data visualisation

#### Definition of Data visualisation
 - presentation of data in a graphical / pictoral format. Abstracted in some schematic form.
 - oftem more understood through graphic visualisation
 
#### Advantages of Data visualisation
 - Easier to rad and understand
 - absord data & information in new and more constructuve ways
 - visualise relationship & patterns
 - compare data
 - is the data complete?
 - trends over time

#### Examples of Data visualisation
 - Maps
 - Charts: bar, pie, line, histograms, scatterplots
 - tables and lists
 - blueprints and schematics

### What is D3
It's a JavaScript library used to manipulate document based on data. D3 combines powerful visualisation components and a data driven approach to manipulating de DOM
D3 allows us to display:
 - HTML
 - SVG
 - CSS

#### Binding Data
 - arbitrary data to the DOm and apply data driven transformation to the page/ doc
 - parse test, json, html, csv, tsv

#### Advantages of D3
 - data visualisation
 - things you can do in JS, but can be done in less code in D3
 - minimal overhead and extremly fast
 - open web standards & familiar conventions
 - support large data sets
 - reuse code through components and plugins

### What are Scales ?
  > "Scales are functions that map from an input domain to an output range"
Your data may only have an input domain of 100 but an SVG viewpoint width a length of only 100
Example:
Domain: 0 - 1000
Range   0 - 100

**Input domain**: range of possible data values. The lowest unit of the data to the highest

**Output Range**: the raneg of possible output values commonly used as display values in px units

[100, 400, 1000, 900, 750] - **input domain** is [100, 1000] or [0, 1000]
If you decide the shortest bar will be 10px tall and the tallest bar will be 500, then your **output range** is [10,500]

#### Creating scales
```javascript
// d3.scale.TYPEOFSCALE

var scale =  d3.scale.linear();

scale(4.5) 		// returns 4.5 (1:1) - no input domain set yet

scale.domain([100, 1000]) 	// set the input domain
scale.range([10, 500]) 	    // set the Output Range

Scale(1000)  	// Returns 500

```
**Quantitative**: For continuous input domains, such as numbers
**Ordinal**: For discrete input deomain, such as names or categories
**Time Scales**: For time domains

##### Linear scales
Most common, choice for continious output range. Mapping is _linear_ meaning that the output range value _y_ can be expressed as a linear function or the input domain value.
<pre>d3.scale.linear()</pre>

##### Identity scales
special case of linear scale, where the domain and range are identical. Occasionally useful with pixel coordinates
<pre>d3.scale.identity()</pre>

##### Power scales
Similar to linear scales, expect there is an exponential transform that is applied to the input domain value before the output range is computed. Support negative values
<pre>d3.scale.sqrt()</pre>

##### Log scales
Similar to linear scales, expect there is a logarithmic transform that is applied to the input domain value before the output range is computed
<pre>d3.scale.log()</pre>

##### Quantize scales
Variant of a discrete range, the input is still continuous and is divided into segmenets based on the number of values in the output range
<pre>d3.scale.quantize()</pre>

##### Threshold scales
Similar to quantize scale except they allow you to map arbitrary subsets of the domain to discrete values. The input is continuous and divided into slices based on a set of threshold values.
<pre>d3.scale.quantize()</pre>





