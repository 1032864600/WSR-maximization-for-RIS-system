## WSR maximization for RIS system

This repository contains the source codes of the Fig.4(b) in the paper ``Weighted Sum-Rate Maximization for Reconfigurable Intelligent Surface Aided Wireless Networks'' published IEEE Transactions on Wireless Communications.

The recent version of this paper can also be found in ArXiv (see <https://arxiv.org/abs/1912.11999>)

One previous version of this paper is named ``Weighted Sum-Rate Optimization for Intelligent Reflecting Surface Enhanced Wireless Networks'', which can be found in ArXiv as well (see <https://arxiv.org/abs/1905.07920>). The short version has been presented in IEEE GLOBECOM 2019.

## Introduction of the codes

### Plot fig.4(b)

Run the file ``converge_plot.m''. You may get the following figure

<img src="./fig4.jpg" height="360" width="450" >

### Generate random channel

To generate one snapshot for simulation, one may run following three files in sequence：

+ ``generate_location.m'': Random the users' locations
+ ``generate_pathloss.m'': Calucate the pathloss according to the locations
+ ``generate_channel.m''" Randomly generate the channel realizations

### Main codes for the algorithms

The following are the main code files for the 5 algorihtms shown in the figure.

+ ``without_RIS.m'': There's no RIS in the system.
+ ``RIS_phaserand.m'': The RIS adopts random phase.
+ ``converge_AO_perfect.m'': Alternating optimization approach illustrated in Section III. Note that, to support the Riemannian conjugate gradient (RCG) algorithm, one should download the Manopt toolbox from <https://www.manopt.org/> at first.
+ ``converge_A2_perfect.m'': Proposed algorithm under the perfect CSI setup.
+ ``converge_A2_imperfect.m'': Proposed algorithm under the imperfect CSI setup.

