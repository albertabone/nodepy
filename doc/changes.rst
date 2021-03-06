
.. _changes:

What's new in Version 0.4
==========================
Version 0.4 of NodePy inclues numerous bug fixes and new features.
The most significant new feature is the use of exact arithmetic for
construction and analysis of many methods, using SymPy.  Because exact
arithmetic can be slow, NodePy automatically switches to floating point
arithmetic for some operations, such as numerical integration of initial value
problems.  If you find operations that seem excessively slow let me know.
You can always revert to floating-point representation of a method by
using method.__num__().

Other new features and fixes include:

    * Improvements to linear multistep methods:
        * Stability region plotting
        * Zero-stability
        * `A(\alpha)`-stability angles
    * Automatic selection of plotting region for stability region plots
    * Code base now hosted on Github (github.com/ketch/nodepy)
    * Documentation corrections
    * Use MathJax (instead of jsMath) in docs
    * Much greater docstring coverage
    * Many more examples in docs (can be run as doctests)
        * For example, 95 doctests covering 25 items in runge_kutta_method.py
    * Extrapolation methods based on GBS (midpoint method) -- thanks to Umair bin Waheed
    * Construction of simple linear finite difference matrices
    * Analysis of the potential for parallelism in Runge-Kutta methods
        * Number of sequentially-dependent stages
        * Plotting of stage dependency graph
    * Automatic reduction of reducible Runge-Kutta methods
    * A heuristic method for possibly-optimal splittings of Runge-Kutta methods
      into upwind/downwind parts
    * Fix bugs in computation of stability intervals
    * Fix bugs in stability region plotting
    * New examples in nodepy/examples/
    * Spectral difference matrices for linear advection -- thanks to Matteo Parsani


