---
layout: default
---

<style>
/* Add CSS styles here */
/* Your existing styles here */
</style>

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

<!-- Add a container for the chart -->
<div id="chart-container" style="width: 100%; height: 400px;"></div>

<script src="https://d3js.org/d3.v6.min.js"></script>
<script>
// Add your interactive graph code here using D3.js
// Example bar chart code:
const data = [
  { label: 'A', value: 10 },
  { label: 'B', value: 20 },
  { label: 'C', value: 15 },
  { label: 'D', value: 25 },
  { label: 'E', value: 30 }
];

const margin = { top: 20, right: 30, bottom: 40, left: 40 };
const width = 600 - margin.left - margin.right;
const height = 400 - margin.top - margin.bottom;

const svg = d3.select('#chart-container')
  .append('svg')
  .attr('width', width + margin.left + margin.right)
  .attr('height', height + margin.top + margin.bottom)
  .append('g')
  .attr('transform', `translate(${margin.left}, ${margin.top})`);

const x = d3.scaleBand()
  .domain(data.map(d => d.label))
  .range([0, width])
  .padding(0.1);

const y = d3.scaleLinear()
  .domain([0, d3.max(data, d => d.value)])
  .nice()
  .range([height, 0]);

svg.selectAll('.bar')
  .data(data)
  .enter().append('rect')
  .attr('class', 'bar')
  .attr('x', d => x(d.label))
  .attr('y', d => y(d.value))
  .attr('width', x.bandwidth())
  .attr('height', d => height - y(d.value));

// Add axes
svg.append('g')
  .attr('class', 'x-axis')
  .attr('transform', `translate(0,${height})`)
  .call(d3.axisBottom(x));

svg.append('g')
  .attr('class', 'y-axis')
  .call(d3.axisLeft(y));

</script>

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

<!-- The rest of your Markdown content... -->
