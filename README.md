# xIST 

**Contents**: This repository contains the following two packages: 1) *xIST (linear Scalar Tensor)* - a package implementing general scalar-tensor theories and tools for their investigation. 2) *COPPER (COsmological Parametrized PERturbations)* - a Mathematica notebook building on xIST to investigate these theories. Latest versions and release dates are:

*xIST*, version 0.7.3, {2016, 3, 29}, 
*COPPER*, version 0.8.0, {2016, 3, 29} 

CopyRight (C) 2016, *Johannes Noller*, under the General Public License. 


**Installation notes**: xIST and COPPER require a working installation of Mathematica and xAct. For details, downloads and documentation for xAct please go to http://www.xact.es. After downloading the files from this repository (and unzipping, if required), the downloaded xIST folder and its contents should be copied into the existing xAct folder (i.e. into the same directory as, for example, the xTensor folder). Depending on the installation directory chosen for xAct this can vary. Common destinations are:

Linux:
   - system-wide: `/usr/share/Mathematica/Applications/xAct`
   - single-user: `$HOME/.Mathematica/Applications/xAct`

Mac OS:
   - system-wide: `/Library/Mathematica/Applications/xAct`
   - single-user: `/Users/<user>/Library/Mathematica/Applications/xAct`

MSWindows:
   - system-wide: `C:\Documents and settings\All Users\Application data\Mathematica\Applications\xAct\`
   - single-user: `C:\Documents and settings\<user>\Application Data\Mathematica\Applications\xAct\`

In general the folder structure has to be
```
..../Mathematica/Applications/xAct/xIST/xIST.m
```
with the \`\`Kernel'' folder in the same directory as the xIST.m package file. After a successful installation the xIST package can be loaded by typing
```
<<xAct`xIST`
```
into a Mathematica notebook. Note that there are no spaces in this command. COPPER automatically loads the xIST package and is self-contained, so all computations in the COPPER notebook can be run once xIST is installed. xIST and COPPER have been tested on Windows, Mac and Linux and on Mathematica 10.3.1.0 and 9.0.1.0. 


**Methodology and computation notes**: The COPPER notebook takes the general ansatz for a quadratic action of perturbations for a tensor and a scalar in an FRW-like background as discussed in the accompanying paper *A general theory of linear cosmological
perturbations: scalar-tensor and vector-tensor theories (http://arxiv.org/abs/1604.01396)* and as is already contained in the xIST package. It then computes all Noether constraints from requiring this action to be diffeomorphism-invariant. Finally it solves all constraints and in that way obtains the true number of independent background functions/coefficients in the full quadratic perturbative action. We present the full actions derived in this way and expressions relating the free coefficients to the original ansatz.


**Comparison with accompanying paper "arXiv:1604.01396"**: The Lagrangians used in the \`\`Lagrangian setup" sections throughout COPPER are imported from the xIST package and should be compared with equations 4.5-4.9 and G.1-G.2 of the accompanying *arXiv:1604.01396*. Note that, while in the paper different letters (T's and L's) are used for background (time-dependent) coefficients in this action, in the COPPER file we stick with a uniform convention of labelling all coefficients in our starting action as L's. Otherwise our starting expressions are identical and the final answers expressed in terms of \`\`alpha'' coefficients are equivalent, see e.g. equation 4.15 as compared to the final action in the 3rd order \`\`Beyond Horndeski'' case computed in COPPER or equation 3.30 in the paper as compared to the final action in the GR case computed in COPPER (final actions in COPPER are expressed in Fourier-space, whereas in the paper we have kept explicit spatial derivatives in the final actions).


**Known issues and bugs**: All the individual sections in COPPER can be computed without any known issues/problems arising. However, when computing the \`\`Lagrangian setup'' sections of several of the sections in COPPER in succession (e.g. as part of evaluating the full notebook), a problem with the internal vbundles and index recognition appears. This is due to a bug when calling the xAct MakeRule function (giving rise to a "VBundleOfIndex::unknown" error that aborts the computation). If this occurs, the simplest solution is to re-start the kernel/only carry out the computations in one of the sections at a time and re-starting the kernel and re-loading xIST whenever one would like to move on. I'm working to resolve this issue fully so no such manual workaround is required. 
