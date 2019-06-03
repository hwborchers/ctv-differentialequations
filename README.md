CRAN Task View: Differential Equations
--------------------------------------

|                 |                                                         | 
|-----------------|---------------------------------------------------------|
| **Maintainer:** | Karline Soetaert and Thomas Petzoldt                    | 
| **Contact:**    | karline.soetaert at nioz.nl                             | 
| **Version:**    | 2019-05-27                                              | 
| **URL:**        | <https://CRAN.R-project.org/view=DifferentialEquations> | 

(NOTE: This is a kind of fork of the original Differential Equations Task
 View on CRAN, but reorganizing the sections and extending the descriptions
 for my own gusto and purposes. --- HwB)

Differential equations (DE) are mathematical equations that describe how
a quantity changes as a function of one or several (independent)
variables, often time or space. Differential equations play an important
role in biology, chemistry, physics, engineering, economy and other
disciplines.

Differential equations can be separated into stochastic versus
deterministic DEs. Problems can be split into initial value problems
versus boundary value problems. One also distinguishes ordinary
differential equations from partial differential equations, differential
algebraic equations and delay differential equations. All these types of
DEs can be solved in R. DE problems can be classified to be either stiff
or nonstiff; the former type of problems are much more difficult to
solve.

The [dynamic models
SIG](https://stat.ethz.ch/mailman/listinfo/r-sig-dynamic-models) is a
suitable mailing list for discussing the use of R for solving
differential equation and other dynamic models such as individual-based
or agent-based models.

This task view was created to provide an overview on the topic. If we
forgot something, or if a new package should be mentioned here, please
let the maintainers know.

**Ordinary Differential Equations (ODEs)**

In an ODE, the unknown quantity is a function of a single independent
variable. Several packages offer to solve ODEs.

-   The "odesolve" package was the first to solve ordinary differential
    equations in R. It contained two integration methods. It has been
    replaced by the package [deSolve](https://cran.r-project.org/package=deSolve).
-   The package [deSolve](https://cran.r-project.org/package=deSolve) contains
    several solvers for solving ODE, DAE, DDE and PDE. It can deal with
    stiff and nonstiff problems.
-   The package [deTestSet](https://cran.r-project.org/package=deTestSet) contains
    solvers designed for solving very stiff equations.
-   The package [odeintr](https://cran.r-project.org/package=odeintr) generates and
    compiles C++ ODE solvers on the fly using Rcpp and
    [Boost](http://www.boost.org/) [odeint](http://www.odeint.com/) .
-   The R package [diffeqr](https://cran.r-project.org/package=diffeqr) provides a
    seamless interface to the **DifferentialEquations.jl** package from
    the Julia programming language. It has unique high performance
    methods for solving ODE, SDE, DDE, DAE and more. Models can be
    written in either R or Julia. It requires an installation of the
    Julia language.
-   Package [pracma](https://cran.r-project.org/package=pracma) implements several
    adaptive Runge-Kutta solvers such as ode23, ode23s, ode45, or the
    Burlisch-Stoer algorithm to obtain numerical solutions for ODEs with
    high accuracy.
-   Package [rODE](https://cran.r-project.org/package=rODE) (inspired from the book
    of Gould, Tobochnik and Christian, 2016) aims to show physics, math
    and engineering students how ODE solvers can be made with R's S4
    classes.
-   Package [sundialr](https://cran.r-project.org/package=sundialr) provides a way
    to call the 'CVODE' function from the 'SUNDIALS' C ODE solving
    library. The package requires the ODE to be written as an 'R' or
    'Rcpp' function.


**Stochastic Differential Equations (SDEs)**

In a stochastic differential equation, the unknown quantity is a
stochastic process.

-   The package [sde](https://cran.r-project.org/package=sde) provides functions for
    simulation and inference for stochastic differential equations. It
    is the accompanying package to the book by Iacus (2008).
-   The package [pomp](https://cran.r-project.org/package=pomp) contains functions
    for statistical inference for partially observed Markov processes.
-   Packages [adaptivetau](https://cran.r-project.org/package=adaptivetau) and
    [GillespieSSA](https://cran.r-project.org/package=GillespieSSA) implement
    Gillespie's "exact" stochastic simulation algorithm (direct method)
    and several approximate methods.
-   The package [Sim.DiffProc](https://cran.r-project.org/package=Sim.DiffProc)
    provides functions for simulation of Itô and Stratonovitch
    stochastic differential equations.
-   Package [QPot](https://cran.r-project.org/package=QPot) analyzes 2-dimensional
    systems of stochastic differential equations using quasi-potential
    analysis.
-   Package [diffeqr](https://cran.r-project.org/package=diffeqr) can solve SDE
    problems using the **DifferentialEquations.jl** package from the
    Julia programming language.

**Delay Differential Equations (DDEs)**

In a DDE, the derivative at a certain time is a function of the variable
value at a previous time.

-   The [dde](https://cran.r-project.org/package=dde) package implements solvers for
    ordinary (ODE) and delay (DDE) differential equations, where the
    objective function is written in either R or C. Suitable only for
    non-stiff equations. Support is also included for iterating
    difference equations.
-   The package [PBSddesolve](https://cran.r-project.org/package=PBSddesolve)
    (originally published as "ddesolve") includes a solver for non-stiff
    DDE problems.
-   Functions in the package [deSolve](https://cran.r-project.org/package=deSolve)
    can solve both stiff and non-stiff DDE problems.
-   Package [diffeqr](https://cran.r-project.org/package=diffeqr) can solve DDE
    problems using the **DifferentialEquations.jl** package from the
    Julia programming language.

**Partial Differential Equations (PDEs)**

PDEs are differential equations in which the unknown quantity is a
function of multiple independent variables. A common classification is
into elliptic (time-independent), hyperbolic (time-dependent and
wavelike), and parabolic (time-dependent and diffusive) equations. One
way to solve them is to rewrite the PDEs as a set of coupled ODEs, and
then use an efficient solver.

-   The R-package [ReacTran](https://cran.r-project.org/package=ReacTran) provides
    functions for converting the PDEs into a set of ODEs. Its main
    target is in the field of ''reactive transport'' modelling, but it
    can be used to solve PDEs of the three main types. It provides
    functions for discretising PDEs on cartesian, polar, cylindrical and
    spherical grids.
-   The package [deSolve](https://cran.r-project.org/package=deSolve) contains
    dedicated solvers for 1-D, 2-D and 3-D time-varying ODE problems as
    generated from PDEs (e.g. by
    [ReacTran](https://cran.r-project.org/package=ReacTran)).
-   Solvers for 1-D time varying problems can also be found in the
    package [deTestSet](https://cran.r-project.org/package=deTestSet).
-   The package [rootSolve](https://cran.r-project.org/package=rootSolve) contains
    optimized solvers for 1-D, 2-D and 3-D algebraic problems generated
    from (time-invariant) PDEs. It can thus be used for solving elliptic
    equations.

Note that, to date, PDEs in R can only be solved using finite
differences. At some point, we hope that finite element and spectral
methods will become available.

**Differential Algebraic Equations (DAEs)**

Differential algebraic equations comprise both differential and
algebraic terms. An important feature of a DAE is its differentiation
index; the higher this index, the more difficult to solve the DAE.

-   The package [deSolve](https://cran.r-project.org/package=deSolve) provides two
    solvers, that can handle DAEs up to index 3.
-   Three more DAE solvers are in the package
    [deTestSet](https://cran.r-project.org/package=deTestSet).
-   Package [diffeqr](https://cran.r-project.org/package=diffeqr) can solve DAE
    problems using the **DifferentialEquations.jl** package from the
    Julia programming language.

**Boundary Value Problems (BVPs)**

BVPs have solutions and/or derivative conditions specified at the
boundaries of the independent variable.

-   Package [bvpSolve](https://cran.r-project.org/package=bvpSolve) deals only with
    this type of equations.
-   The package [ReacTran](https://cran.r-project.org/package=ReacTran) can solve
    BVPs that belong to the class of reactive transport equations.
-   Package [diffeqr](https://cran.r-project.org/package=diffeqr) can also solve
    BVPs using the **DifferentialEquations.jl** package from the Julia
    programming language.

**Other**

-   The [simecol](https://cran.r-project.org/package=simecol) package provides an
    interactive environment to implement and simulate dynamic models.
    Next to DE models, it also provides functions for grid-oriented,
    individual-based, and particle diffusion models.
-   The [RxODE](https://cran.r-project.org/package=RxODE) package provides
    facilities for running simulations from ordinary differential
    equation (ODE) models. A compilation manager translates the ODE
    model into C, compiles it, and dynamically loads the object code
    into R for improved computational efficiency. Additionally, RxODE
    allows ODEs to be solved in parallel using the liblsoda library and
    OpenMP.
-   Package [scaRabee](https://cran.r-project.org/package=scaRabee) offers
    frameworks for simulation and optimization of
    Pharmacokinetic-Pharmacodynamic Models.
-   In the package [FME](https://cran.r-project.org/package=FME) are functions for
    inverse modelling (fitting to data), sensitivity analysis,
    identifiability and Monte Carlo Analysis of DE models.
-   The package [nlmeODE](https://cran.r-project.org/package=nlmeODE) has functions
    for mixed-effects modelling using differential equations.
-   [mkin](https://cran.r-project.org/package=mkin) provides routines for fitting
    kinetic models with one or more state variables to chemical
    degradation data.
-   Package [dMod](https://cran.r-project.org/package=dMod) provides functions to
    generate ODEs of reaction networks, parameter transformations,
    observation functions, residual functions, etc. It follows the
    paradigm that derivative information should be used for optimization
    whenever possible.
-   The package [CollocInfer](https://cran.r-project.org/package=CollocInfer)
    implements collocation-inference for continuous-time and
    discrete-time stochastic processes.
-   Root finding, equilibrium and steady-state analysis of ODEs can be
    done with the package [rootSolve](https://cran.r-project.org/package=rootSolve).
-   The [deTestSet](https://cran.r-project.org/package=deTestSet) package contains
    many test problems for differential equations.
-   The [PBSmodelling](https://cran.r-project.org/package=PBSmodelling) package adds
    GUI functions to models.
-   [phaseR](https://cran.r-project.org/package=phaseR) is an R package for the
    qualitative analysis of one and two dimensional autonomous ODE
    systems, using phase plane methods.
-   Package [cOde](https://cran.r-project.org/package=cOde) supports the automatic
    creation of dynamically linked code for packages
    [deSolve](https://cran.r-project.org/package=deSolve)
    [bvpSolve](https://cran.r-project.org/package=bvpSolve) (or a built-in
    implementation of the sundials cvode solver) from inline C embedded
    in the R code.
-   Package [rodeo](https://cran.r-project.org/package=rodeo) is an object oriented
    system and code generator that creates and compiles efficient
    Fortran code for [deSolve](https://cran.r-project.org/package=deSolve) from
    models defined in stoichiomatry matrix notation.
-   Package [ecolMod](https://cran.r-project.org/package=ecolMod) contains the
    figures, data sets and examples from a book on ecological modelling
    (Soetaert and Herman, 2009).
-   [primer](https://cran.r-project.org/package=primer) is a support package for the
    book of Stevens (2009).

### CRAN packages:

-   [adaptivetau](https://cran.r-project.org/package=adaptivetau)
-   [bvpSolve](https://cran.r-project.org/package=bvpSolve) (core)
-   [cOde](https://cran.r-project.org/package=cOde)
-   [CollocInfer](https://cran.r-project.org/package=CollocInfer)
-   [dde](https://cran.r-project.org/package=dde)
-   [deSolve](https://cran.r-project.org/package=deSolve) (core)
-   [deTestSet](https://cran.r-project.org/package=deTestSet)
-   [diffeqr](https://cran.r-project.org/package=diffeqr)
-   [dMod](https://cran.r-project.org/package=dMod)
-   [ecolMod](https://cran.r-project.org/package=ecolMod)
-   [FME](https://cran.r-project.org/package=FME)
-   [GillespieSSA](https://cran.r-project.org/package=GillespieSSA)
-   [mkin](https://cran.r-project.org/package=mkin)
-   [nlmeODE](https://cran.r-project.org/package=nlmeODE)
-   [odeintr](https://cran.r-project.org/package=odeintr)
-   [PBSddesolve](https://cran.r-project.org/package=PBSddesolve)
-   [PBSmodelling](https://cran.r-project.org/package=PBSmodelling)
-   [phaseR](https://cran.r-project.org/package=phaseR)
-   [pomp](https://cran.r-project.org/package=pomp)
-   [pracma](https://cran.r-project.org/package=pracma)
-   [primer](https://cran.r-project.org/package=primer)
-   [QPot](https://cran.r-project.org/package=QPot)
-   [ReacTran](https://cran.r-project.org/package=ReacTran)
-   [rODE](https://cran.r-project.org/package=rODE)
-   [rodeo](https://cran.r-project.org/package=rodeo)
-   [rootSolve](https://cran.r-project.org/package=rootSolve) (core)
-   [RxODE](https://cran.r-project.org/package=RxODE)
-   [scaRabee](https://cran.r-project.org/package=scaRabee)
-   [sde](https://cran.r-project.org/package=sde) (core)
-   [Sim.DiffProc](https://cran.r-project.org/package=Sim.DiffProc)
-   [simecol](https://cran.r-project.org/package=simecol)
-   [sundialr](https://cran.r-project.org/package=sundialr)

### Related links:

-   CRAN Task View: [ChemPhys](ChemPhys.html)
-   CRAN Task View: [Econometrics](Econometrics.html)
-   CRAN Task View: [Environmetrics](Environmetrics.html)
-   CRAN Task View: [Optimization](Optimization.html)
-   CRAN Task View: [Pharmacokinetics](Pharmacokinetics.html)
-   [Wikipedia: Differential
    equation](http://en.wikipedia.org/wiki/Differential_equation)
-   [R-Forge website for package
    deSolve](http://deSolve.r-forge.r-project.org)
-   [R-Forge website for package
    pomp](http://pomp.r-forge.r-project.org)
-   [Book: Iacus, SM. 2008. Simulation and Inference for Stochastic
    Differential Equations: with R examples,
    Springer](http://www.springer.com/978-0-387-75838-1)
-   [Book: Soetaert, K. and P.M.J. Herman, 2009. A Practical Guide to
    Ecological Modelling, using R as a simulation Platform,
    Springer.](http://www.springer.com/life+sciences/ecology/book/978-1-4020-8623-6)
-   [Book: Stevens, H, 2009. A Primer of Ecology with R,
    Springer.](http://www.springer.com/life+sci/ecology/book/978-0-387-89881-0)
-   [Book: Soetaert, K., Cash, J. and Mazzia, F. 2012. Solving
    Differential Equations in R,
    Springer.](http://www.springer.com/statistics/computanional+statistics/book/978-3-642-28069-6)
