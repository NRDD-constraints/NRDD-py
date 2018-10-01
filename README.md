# NRDD_constraints : A python tool for calculating the direct-detection exclusion plot for the WIMP-nucleon cross section in a non-relativistic effective model. 

The <code> NRDD_constraints</code> tool provides simple interpolating functions written in python that return the most constraining limit on the dark matter-nucleon scattering cross section for a list of non-relativistic effective operators  that corresponds to the diagonal terms listed in Table 2 of [arXiv: 1809.XXXXX](https://arxiv.org/). The package contains three files:

* The code, **NRDD_constraints.py** 
* A simple driver, **NRDD_constraints-example.py**
* A data file, **data.npy**

You can get the latest version of <code> NRDD_constraints</code> from [github](https://github.com/NRDD-constraints/NRDD).

# Installation

The tool can be downloaded from [https://github.com/NRDD-constraints/NRDD/archive/master.zip](https://github.com/NRDD-constraints/NRDD/archive/master.zip) or cloned by,

<code> git clone https://github.com/NRDD-constraints/NRDD </code>

# Usage

Please see **appendix B** of [arXiv: 1809.XXXXX](https://arxiv.org/) and **NRDD_constraints-example.py** for a detailed explanation. 

*Brief overview for using <code> NRDD_constraints</code>*

Import the package:

<code> import NRDD_constraints as NR </code>

This defines two functions:

* <code> sigma_nucleon_bound(**inter, mchi, r**) </code> which interpolates the bound on the effective WIMP-nucleon cross-section defined in Eq. (B.1) as a function of the WIMP mass 
mchi and of the ratio r (DM-neutron to DM-proton couplings) in the ranges 0.1 GeV < mchi < 100 GeV, -10000 < r < 10000.

   The <code> **inter** </code> parameter is a string that selects the interaction term
and can be chosen in the list provided by second function <code> print_interactions() </code>.

* <code> print_interactions()</code> gives the possible interactions:

['O1_O1','O3_O3', 'O4_O4', 'O5_O5', 'O6_O6', 
'O7_O7', 'O8_O8', 'O9_O9', 'O10_O10', 'O11_O11',
'O12_O12', 'O13_O13', 'O14_O14', 'O15_O15'
'O5_O5_qm4', 'O6_O6_qm4', 'O11_O11_qm4'] 

The output of <code> sigma_nucleon_bound(**inter, mchi, r**) </code> corresponds to the results of 
[1805.06113](https://arxiv.org/abs/1805.06113) (updated to
the XENON1T bound in [1805.12562](https://arxiv.org/abs/1805.12562)) with the exception of the long-range interaction terms with a photon propagator, which have been discussed in [arXiv: 1809.XXXXX](https://arxiv.org/). 

# Citation

If you use <code> NRDD_constraints</code> please cite the following papers: [1805.06113](https://arxiv.org/abs/1805.06113),
[arXiv: 1809.XXXXX](https://arxiv.org/)

# Authors

* Stefano Scopel (Sogang University)
* Gaurav Tomar (Sogang University)
* Jong–Hyun Yoon (Sogang University)
* Sunghyun Kang (Sogang University)

# License

<code> NRDD_constraints</code> is distributed under the MIT license.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
