<h2 align="center">Magnetized Accretion-Ejection Structures</h2>

<br>

<p align="center">
    A <strong>1D MHD solver</strong> for astrophysical accretion disk launching self-collimated jets.
    <br>
    Written in <strong>Fortran</strong> using the <strong>OpenMP</strong> API and the <strong>MPI</strong> library.
</p>

<br>

<p align="center">
    <img src="https://github.com/nathanzimniak/maes/blob/main/docs/images/banner.png">
</p>

<br>

> [!IMPORTANT]
> The code is not publicly available at this time. You can still explore the computed solutions here: [maes_website](https://nathanzimniak.github.io/maes_website/).

<br>

> ### Physical Model

The code solves the steady-state, axisymmetric MHD equations. Solutions are self-similar (i.e., based on a separation of variables ansatz), allowing the original system of PDEs to be reduced to a system of ODEs that can be solved within a semi-analytical framework. A detailed description can be found in the following papers (and references therein): [Ferreira 1997](https://ui.adsabs.harvard.edu/abs/1997A%26A...319..340F/abstract), [Casse+ 2000a](https://ui.adsabs.harvard.edu/abs/2000A%26A...353.1115C/abstract), [Jacquemin-Ide+ 2019](https://ui.adsabs.harvard.edu/abs/2019MNRAS.490.3112J/abstract), [Zimniak+ 2024](https://ui.adsabs.harvard.edu/abs/2024A%26A...692A..99Z/abstract).

#

> ### Numerical Method

The MHD equations are stiff, requiring the use of an implicit integration scheme with adaptive step size and order. The solver relies on backward differentiation formulas (BDF, Hall & Watt 1976), to ensure numerical stability and accurate crossing of critical points.

#

> ### Requirements

- **Build tool**: make
- **Compiler**: gfortran with Fortran 2018 and OpenMP support
- **Libraries**: MPI, HDF5
