Full Stack Development – Fetching Data, Visualizing with D3, and Deploying with Dokku
===

![enter image description here](https://files.realpython.com/media/flask-stock-visualizer.0427ad74f1f8.png)

In this tutorial we’ll build a web application to grab data from the  [NASDAQ-100](http://www.nasdaq.com/quotes/nasdaq-100-stocks.aspx)  and visualize it as a bubble graph with D3. Then to top it off, we’ll deploy this on Digital Ocean via Dokku.

> **Note:**  Bubble charts are perfect for visualizing hundreds of values in a small space. However, they are harder to read because it can be difficult to differentiate similar size circles. If you’re working with only a few values, a bar chart is probably the better option since it’s much easier to read.

Main Tools used in this tutorial: Python v2.7.8, Flask v0.10.1,  [Requests](https://realpython.com/python-requests/)  v2.4.1, D3 v3.4.11, Dokku v0.2.3, and Bower v1.3.9

Start by locating and downloading the file  __app_boilerplate.zip_  from this  [repo](https://github.com/realpython/flask-stock-visualizer). This file contains a Flask boilerplate. Once downloaded, extract the file and folders, activate a virtualenv, and  [install the dependencies with Pip](https://realpython.com/what-is-pip/):
```py
pip install -r requirements.txt
```
Then test to make sure it works: Fire up the server, open your browser, and navigate to  [http://localhost:5000/](http://localhost:5000/). You should see “Hello, world!” staring back at you.

[Remove ads](https://realpython.com/account/join/)

## Fetching Data

Create a new route and view function in the  _app.py_  file:
```py
@app.route("/data")
def data():
    return jsonify(get_data())
```
Update the imports:
```
from flask import Flask, render_template, jsonify
from stock_scraper import get_data
```
So, when that route is called, it converts the returned value from a function called  `get_data()`  to JSON and then returns it. This function resides in a file called  _stock_scraper.py_, which - surprise! - fetches data from the NASDAQ-100.

### The script

Add  _stock_scraper.py_  to the main directory.

**Your turn**: Create the script on your own, following these steps:

1.  Download the CSV from  [http://www.nasdaq.com/quotes/nasdaq-100-stocks.aspx?render=download](http://www.nasdaq.com/quotes/nasdaq-100-stocks.aspx?render=download).
2.  Grab the relevant data from the CSV: stock name, stock symbol, current price, net change, percent change, volume, and value.
3.  Convert the parsed data to a Python dictionary.
4.  Return the dictionary.

How’d it go? Need help? Let’s look at one possible solution:
```
import csv
import requests

URL = "http://www.nasdaq.com/quotes/nasdaq-100-stocks.aspx?render=download"

def get_data():
    r = requests.get(URL)
    data = r.text
    RESULTS = {'children': []}
    for line in csv.DictReader(data.splitlines(), skipinitialspace=True):
        RESULTS['children'].append({
            'name': line['Name'],
            'symbol': line['Symbol'],
            'symbol': line['Symbol'],
            'price': line['lastsale'],
            'net_change': line['netchange'],
            'percent_change': line['pctchange'],
            'volume': line['share_volume'],
            'value': line['Nasdaq100_points']
        })
    return RESULTS
```
**What’s happening?**

1.  Here, we fetch the URL via a GET request and then convert the Response object,  `r`, to  [unicode](https://realpython.com/python-encodings-guide/).
2.  We then work with the  `CSV`  library to convert the comma delimited text into an instance of the  `DictReader()`  class, which maps the data to a dictionary rather than a list.
3.  Finally, after looping through the data, creating a list of dictionaries (where each dictionary represents a different stock), we return the  `RESULTS`  dict.

> NOTE: You could also use a dict comprehension to create the individual dictionaries. This is a much more efficient method, however you sacrifice readability. Your call.

[Time to test](https://realpython.com/python-testing/): Fire up the server and then navigate to  [http://localhost:5000/data](http://localhost:5000/data). If all went well, you should see an object containing the relevant stock data.

With the data at hand, we can now work with visualizing it on the front-end.

## Visualizing

Along with HTML and CSS, we’ll be using  [Bootstrap](http://getbootstrap.com/), Javascript/jQuery, and  [D3](http://d3js.org/)  to power our front-end. We’ll also use the client-side dependency management tool  [Bower](http://bower.io/)  to download and manage these libraries.

**Your turn**: Follow the  [installation instructions](https://github.com/bower/bower#install)  to setup Bower on your machine.  _Hint: You will need to install  [Node.js](http://nodejs.org/download/)  before you install Bower_.

Ready?

[Remove ads](https://realpython.com/account/join/)

## Bower

Two files are needed to get bower going -  _[bower.json](http://bower.io/docs/creating-packages/#bowerjson)_  and  _.[bowerrc](http://bower.io/docs/config/)_.

The latter file is used to configure Bower. Add it to the main directory:

{
  "directory": "static/bower_components"
}

This just specifies that we want the dependencies installed in the  _bower_components_  directory (convention) within the app’s  _static_  directory.

Meanwhile, the first file,  _bower.json_, stores the Bower manifest - meaning that it contains metadata about the Bower components as well as the application itself. The file can be created interactively with the  `bower init`  command. Do that now. Just accept all the defaults.

Now, we can install the dependencies.

$ bower install bootstrap#3.2.0 jquery#2.1.1 d3#3.4.11 --save

The  `--save`  flag adds the packages to the  _bower.json_  dependencies array. Check it out. Also, make sure the dependency versions in  _bower.json_  match up to the versions we specified - i.e.,  `bootstrap#3.20`.

With our dependencies installed, let’s make them accessible in our app.

### Update  _index.html_

<!DOCTYPE html>
<html>
  <head>
    <title>Flask Stock Visualizer</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href={{ url_for('static', filename='./bower_components/bootstrap/dist/css/bootstrap.min.css') }} rel="stylesheet" media="screen">
    <link href={{ url_for('static', filename='main.css') }} rel="stylesheet" media="screen">
  </head>
  <body>
    <div class="container">
    </div>
    <script src={{ url_for('static', filename='./bower_components/jquery/dist/jquery.min.js') }}></script>
    <script src={{ url_for('static', filename='./bower_components/bootstrap/dist/js/bootstrap.min.js') }}></script>
    <script src={{ url_for('static', filename='./bower_components/d3/d3.min.js') }}></script>
    <script src={{ url_for('static', filename='main.js') }}></script>
  </body>
</html>

## D3

With so many data visualization frameworks out there, why  [D3](http://d3js.org/)? Well, D3 is fairly low level, so it let’s you build the type of framework you want. Once you append your data to the DOM, you use a combo of CSS3, HTML5, and SVG to create the actual visualization. Then you can add interactivity through D3’s built-in data-driven  [transitions](https://github.com/mbostock/d3/wiki/Transitions).

To be fair, this library is not for everyone. Since you have a lot of freedom to build what you want, the learning curve is fairly high. If you are looking for a quick start, check out  [Python-NVD3](https://github.com/areski/python-nvd3), which is a wrapper for D3, used to make working with D3 much, much easier. We are not using it for this tutorial though, since Python-NVD3 does not support bubble charts.

**Your turn**: Go through the D3  [intro tutorial](http://d3js.org/#introduction).

Now let’s code.

### Setup

Add the following code to  _main.js_:

// Custom JavaScript

$(function() {
  console.log('jquery is working!');
  createGraph();
});

function createGraph() {
  // Code goes here
}

Here, after the initial page load, we log ‘jquery is working!’ to the console then fire a function called  `createGraph()`. Test this out. Fire up the server then navigate to  [http://localhost:5000/](http://localhost:5000/)  and with the JavaScript Console open, refresh the page. You should see the ‘jquery is working!’ text if all went well.

Add the following tag to the  _index.html_  file, within the  `<div>`  tag that has an  `id`  of  `container`  (after line 10), to hold the D3 bubble chart:

<div id="chart"></div>

[Remove ads](https://realpython.com/account/join/)

### Main Config

Add the following code to the  `createGraph()`  function in  _main.js_:

var width = 960; // chart width
var height = 700; // chart height
var format = d3.format(",d");  // convert value to integer
var color = d3.scale.category20();  // create ordinal scale with 20 colors
var sizeOfRadius = d3.scale.pow().domain([-100,100]).range([-50,50]);  // https://github.com/mbostock/d3/wiki/Quantitative-Scales#pow

Be sure to consult the code comments for an explantation as well as the official D3  [documentation](https://github.com/mbostock/d3/wiki/API-Reference). Look anything up you don’t understand.  _A coder must be self-reliant!_

### Bubble Config

var bubble = d3.layout.pack()
  .sort(null)  // disable sorting, use DOM tree traversal
  .size([width, height])  // chart layout size
  .padding(1)  // padding between circles
  .radius(function(d) { return 20 + (sizeOfRadius(d) * 30); });  // radius for each circle

Again, add the above code to the  `createGraph()`  function, and check the  [docs](https://github.com/mbostock/d3/wiki/Pack-Layout)  for any questions.

### SVG Config

Next, add the following code to  `createGraph()`, which select the element with the  `id`  of  `chart`, then appends the circles along with a number of attributes:

var svg = d3.select("#chart").append("svg")
  .attr("width", width)
  .attr("height", height)
  .attr("class", "bubble");

Continuing with the  `createGraph()`  function, we now need to grab the data, which can be done asynchronously with D3.

### Request the Data

// REQUEST THE DATA
d3.json("/data", function(error, quotes) {
  var node = svg.selectAll('.node')
    .data(bubble.nodes(quotes)
    .filter(function(d) { return !d.children; }))
    .enter().append('g')
    .attr('class', 'node')
    .attr('transform', function(d) { return 'translate(' + d.x + ',' + d.y + ')'});

    node.append('circle')
      .attr('r', function(d) { return d.r; })
      .style('fill', function(d) { return color(d.symbol); });

    node.append('text')
      .attr("dy", ".3em")
      .style('text-anchor', 'middle')
      .text(function(d) { return d.symbol; });
});

So, we hit the  `/data`  endpoint that we set up earlier to return the data. The remainder of this code simply adds the bubbles and the text to the DOM. This is standard boilerplate  [code](http://bl.ocks.org/mbostock/4063269), modified slightly for our data.

### Tooltips

Since we have limited room on the chart, still within the  `createGraph()`  function, let’s add some tooltips that show additional information about each specific stock.

// tooltip config
var tooltip = d3.select("body")
  .append("div")
  .style("position", "absolute")
  .style("z-index", "10")
  .style("visibility", "hidden")
  .style("color", "white")
  .style("padding", "8px")
  .style("background-color", "rgba(0, 0, 0, 0.75)")
  .style("border-radius", "6px")
  .style("font", "12px sans-serif")
  .text("tooltip");

These are just the CSS styles associated with the tooltip. We still need to add the actual data. Update the code where we append the circles to the DOM:

node.append("circle")
  .attr("r", function(d) { return d.r; })
  .style('fill', function(d) { return color(d.symbol); })

  .on("mouseover", function(d) {
    tooltip.text(d.name + ": $" + d.price);
    tooltip.style("visibility", "visible");
  })
  .on("mousemove", function() {
    return tooltip.style("top", (d3.event.pageY-10)+"px").style("left",(d3.event.pageX+10)+"px");
  })
  .on("mouseout", function(){return tooltip.style("visibility", "hidden");});

Test this out, navigate to  [http://localhost:5000/](http://localhost:5000/). Now when you hoover over a circle, you’ll see some underlying metadata - company name and stock price.

**Your turn**: Add more metadata. What other data do you think is relevant? Think of what we’re displaying here - the relative change in price. You could perhaps calculate the previous price and show:

1.  Current Price
2.  Relative change
3.  Previous Price

[Remove ads](https://realpython.com/account/join/)

### Refactor

stocks What if we just wanted to visualize stocks with a modified market value-weighted index - the NASDAQ-100 Points  [column](http://www.nasdaq.com/quotes/nasdaq-100-stocks.aspx)  - greater than .1?

Add a conditional to the  `get_data()`  function:

def get_data():
    r = requests.get(URL)
    data = r.text
    RESULTS = {'children': []}
    for line in csv.DictReader(data.splitlines(), skipinitialspace=True):
        if float(line['Nasdaq100_points']) > .01:
            RESULTS['children'].append({
                'name': line['Name'],
                'symbol': line['Symbol'],
                'symbol': line['Symbol'],
                'price': line['lastsale'],
                'net_change': line['netchange'],
                'percent_change': line['pctchange'],
                'volume': line['share_volume'],
                'value': line['Nasdaq100_points']
            })
    return RESULTS

Now, let’s increase each bubbles’ radius, in the bubble config section of  _main.js_; modify the code accordingly:

// Radius for each circle
.radius(function(d) { return 20 + (sizeOfRadius(d) * 60); });

### CSS

Finally, let’s add some basic styles to  _main.css_:

body {
  padding-top: 20px;
  font: 12px sans-serif;
  font-weight: bold;
}

Look good? Ready to deploy?

## Deploying

[Dokku](https://github.com/progrium/dokku)  is an open-source, Heroku-like, Platform as a Service (PaaS), powered by Docker. Once setup, you can push your app to it with Git.

We’re using  [Digital Ocean](https://www.digitalocean.com/)  as our host. Let’s get started.

### Setup Digital Ocean

[Sign up](https://cloud.digitalocean.com/registrations/new)  for an account, if you don’t already have one. Then follow this  [guide](https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2)  to add a public key.

Create a new Droplet - specify a name, size, and location. For the image, click the “Applications” tab and select the Dokku application. Be sure to select your SSH key.

Once created, complete the setup by entering the IP of the newly created Droplet into your browser, which will take you to the Dokku setup screen. Confirm that the public key is correct, then click “Finish Setup”.

Now the VPS can accept pushes.

### Deploy Config

1.  Create a Procfile with the following code:  `web: gunicorn app:app`. (This file contains the command that must run in order to start the web process.)
2.  Install gunicorn:  `pip install gunicorn`
3.  Update the  _requirements.txt_  file:  `pip freeze > requirements.txt`
4.  Initialize a new local Git repo:  `git init`
5.  Add a remote:  `git remote add dokku dokku@192.241.208.61:app_name`  (Be sure to add your own IP address.)

[Remove ads](https://realpython.com/account/join/)

### Update  _app.py_:

if __name__ == '__main__':
    port = int(os.environ.get('PORT', 5000))
    app.run(host='0.0.0.0', port=port)

So, we first try to grab the port from the app’s environment, and if not found, it defaults to port 5000.

Make sure to update the imports as well:

import os

### Deploy!

Commit your changes, then push:  `git push dokku master`. If all went well, you should see the application’s URL in your terminal:

=====> Application deployed:
 http://192.241.208.61:49155

Test it out. Navigate to  [http://192.241.208.61:49155](http://192.241.208.61:49155/). (Again, be sure to add your own IP address along with the correct port.) You should see your live app! (See the image at the top of this post for a preview.)

[**Source :**](https://realpython.com/web-development-with-flask-fetching-data-with-requests/)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjU3OTYwNTgwXX0=
-->