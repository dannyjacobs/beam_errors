# Understanding Cross-coupling in dense packed arrays

## Cross-coupling beam models
We compare simulated beam models of 3 antennas in HERA-19 hex with the legacy NF beam model.
''' beam_comparison_updated.ipynb ''' provides some comparison plots.
Delay space comparison of cross-coupling beams with legacy beam model show direction dependent delay response for different baselines. Baselines with EW component show the dependence.

## Visibility simulations:
###### Simulator: [Pyuvsim](https://pyuvsim.readthedocs.io/en/latest/)
###### Skymodels: 
1. 1src 
2. A-team 
3. GLEAM sources > 100 mJy

###### Simulation box sizes:
1. 820 ch x 97.7 kHz (110-190 MHz), 10s x 8640 (24hrs), 3 Ants (from HERA-19 hex)
2. 820 ch x 97.7 kHz (110-190 MHz), 10s x 8640 (24hrs), 3 Ants (from HERA-19 hex)
3. 192 ch x 97.7 kHz (117-134 MHz), 10s x 540 (1.5hrs), 3 Ants (from HERA-19 hex)

###### Beam models:
- NF legacy beam model for all antennas
- Separate cross-coupling beams for each antenna 
- Single cross-coupling beam for all antennas

###### Notebooks: 
1. 1src: ''' delayspec_1src_new.ipynb '''
2. A-team: ''' delayspec_Ateam_new.ipynb '''
3. GLEAM: ''' delayspec_GLEAM_new.ipynb '''

We observe structure beyond the horizon in delay spectra of visibilities with cross-coupling.
Some of the structure in delay-fringe rate space is similar to semi-analytical simulation by Alec.

## Assessing performance of mutual-coupling mitigation methods
Mitigation of cross-coupling using X-talk filter developed by NK
Initial tests show over-subtraction of power on delay modes used for filter. Further investigation is required.
 