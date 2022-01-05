# 2.3 Introduction to Matplotlib

## Architecture of Matplotlib
* Backend Layer (FigureCanvas, Renderer, Event)  
Has three built-in abstract interface classes
    1. FigureCanvas: `matplotlib.backend_bases.FigureCanvas`
        * Encompasses the area onto which the figure is drawn
    2. Renderer: `matplotlib.backend_bases.Renderer`
        * Knows how to draw on the FigureCanvas
    3. Event: `matplotlib.backend_bases.Event`
        * Handles user inputs such as keyboard strokes and mouse clicks
* Artist Layer (Artist)
    * Heavy lifting
    * web application, UI
    1. Comprised of one main object- **Artist**
        * Knows how to use the `Renderer` to draw on the canvas
        * Title, lines, tick labels, images are Artist instances
    2. Two types of Artist Objects:
        1. **Primitive**: Line2D, Rectangle,Circle,and Text
        2. **Composite**: Axis, Tick, Axes, Figure
    3. Each Composite Artist can contain other Composite or Primitive Artists  
* Scripting Layer (pyplot)
    * For everyday purposes
    * quick and easy generation of plots  



### Example of Python Implementation
    from matplotlib.backends.backend_agg import FigureCanvasAgg as FigureCanvas  # FigureCanvas , backend 
    from matplotlib.figure import Figure # Figure artist  
    fig=Figure()  
    canvas=FigureCanvas(fig)  
    \# create 10000 random numbers to plot using np  
    import numpy as np  
    x=np.random.randn(10000)   
    ax=fig.add_subplot(111) \# creates axes artist, adds to fig axes container, 111 is convention, creates grid with one row, one col, uses first cell in that grid for location of new axes  

    ax. hist(x,100) # axes method hist, creates rectangle artists for hist bars, adds them to axes container

    ax.set_title("Normal distribution with $\mu=0, \signma=1$')
    fig.savefig("matplotlob_histogram.png")



