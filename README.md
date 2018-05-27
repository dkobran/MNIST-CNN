# Example project: How to generate graphs in Gradient

In this example,  we'll build a simple (2-hidden layer) neural network to classify hand written digits using the MNIST dataset and TensorFlow.  We'll graph the loss and the accuracy as Metrics in our Gradient Job.

### The following steps will allow you to graph data in your Jobs:

To instantiate a chart, print the following statement in your logs:

```{"chart": "<identifier>", "axis": "<label>"}```

The 'identifier' is required and can be anything you specify. It also acts as the chart title. The remaining parameters are optional. The 'axis' parameter serves as the x-axis label. Note that quotes are required around all strings.

Once the chart is instantiated, you may add data with the following statement:

```{"chart": "<identifier>", "y": <value>, "x": <value>}```

The 'identifier' is the same string you instantiated the chart with. The x and y values serve as a data point. The y value is required. If no x value is specified, however, the chart will default to time duration, meaning the x value will be the time in seconds between the beginning of the job to when the statement is printed in the job log. Note that number values do not require quotes.

Here's what a typical output of the detector will look like:

![Metrics Example](https://i.imgur.com/ZBuGMNi.png)
