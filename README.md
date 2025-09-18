Notebook to analyse planes of satellites identified in TNG-50 as either transient or persistent.

(c) Till Sawala (2025). Please contact me at till.sawala@helsinki.fi with any issues or questions.

You are free to use any parts of this notebook, with appropriate attribution (see below).



The notebook requires the illustris_python package: https://github.com/illustristng/illustris_python

It builds on the MW/M31 catalogue of Pillepich et al. (2024), https://www.tng-project.org/data/milkyway+andromeda/, and the TNG-50-1 merger trees, available at: https://www.tng-project.org/data/downloads/TNG50-1/

If you use parts of this script in your own work, I would appreciate a reference to the paper "Planes of satellites, at once transient and persistent". Of course, if you use the underlying simulation data, including the pre-computed data provided with this notebook, please also cite the relevant papers, as described here: https://www.tng-project.org/data/docs/background/#sec4

All positional computations are done in
. The MW/M31 catalogue uses physical positions

and is transformed when first read. Keep this in mind if you add additional simulation data.

Throughout the notebook, variables that refer to the host-centric frame described in the paper will be called transient (name contains _trans), while variables that refer to the satellite-centric frame will be called persistent (name contains _pers).

The parameters of this script that are meant to be changed are all defined below the cell Definitions. You can easily change, for example, the lookback time interval (N_snap), the number of satellites to consider (N_sat), or the definition of
(via the r_200_factor). However, please note that some annotations of the plots are manually set for the specific values chosen in the paper and don't work for other parameter combinations. They will be placed when paper_annotations is True and omitted otherwise.
