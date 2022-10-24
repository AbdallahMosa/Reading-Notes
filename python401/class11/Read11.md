# Data Visualization
## what is Data Visualization

  - Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data. 

##  what is Advantages of Data Visualization
  1. Easily sharing information.
  2. Interactively explore opportunities.
  3. Visualize patterns and relationships.
 
 ## General Types of Visualizations:
  1. Chart: Information presented in a tabular, graphical form with data displayed along two axes. Can be in the form of a graph, diagram, or map
  2. Table: A set of figures displayed in rows and columns
  3. Graph: A diagram of points, lines, segments, curves, or areas that represents certain variables in comparison to each other, usually along two axes at a right angle.
  4. Geospatial: A visualization that shows data in map form using different shapes and colors to show the relationship between pieces of data and specific locations
  5. Infographic: A combination of visuals and words that represent data. Usually uses charts or diagrams.
  6. Dashboards: A collection of visualizations and data displayed in one place to help with analyzing and presenting data


  ## What is Matplotlib?
   - Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python. Matplotlib makes easy things easy and hard things possible.

  ## Installing and Importing  Matplotlib
   - ```python 
        pip install matplotlib
       ```
   -    ``` python 
        import matplotlib.pyplot as plt```
        
  ## Simple example
              ``` python import numpy as np
        import matplotlib.pyplot as plt

        from matplotlib.ticker import NullFormatter  # useful for `logit` scale

        # Fixing random state for reproducibility
        np.random.seed(19680801)

        # make up some data in the interval ]0, 1[
        y = np.random.normal(loc=0.5, scale=0.4, size=1000)
        y = y[(y > 0) & (y < 1)]
        y.sort()
        x = np.arange(len(y))

        # plot with various axes scales
        plt.figure(1)

        # linear
        plt.subplot(221)
        plt.plot(x, y)
        plt.yscale('linear')
        plt.title('linear')
        plt.grid(True)


        # log
        plt.subplot(222)
        plt.plot(x, y)
        plt.yscale('log')
        plt.title('log')
        plt.grid(True)


        # symmetric log
        plt.subplot(223)
        plt.plot(x, y - y.mean())
        plt.yscale('symlog', linthreshy=0.01)
        plt.title('symlog')
        plt.grid(True)

        # logit
        plt.subplot(224)
        plt.plot(x, y)
        plt.yscale('logit')
        plt.title('logit')
        plt.grid(True)
        # Format the minor tick labels of the y-axis into empty strings with
        # `NullFormatter`, to avoid cumbering the axis with too many labels.
        plt.gca().yaxis.set_minor_formatter(NullFormatter())
        # Adjust the subplot layout, because the logit one may take more space
        # than usual, due to y-tick labels like "1 - 10^{-3}"
        plt.subplots_adjust(top=0.92, bottom=0.08, left=0.10, right=0.95, hspace=0.25,
                            wspace=0.35)

        plt.show()
   
 -   ![alt](https://matplotlib.org/2.0.2/_images/pyplot_scales.png)             
  
      
      
      
