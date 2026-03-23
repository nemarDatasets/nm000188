# BNCI 2014-009 P300 dataset

BNCI 2014-009 P300 dataset.

## Dataset Overview

- **Code**: BNCI2014-009
- **Paradigm**: p300
- **DOI**: 10.1088/1741-2560/11/3/035008
- **Subjects**: 10
- **Sessions per subject**: 3
- **Events**: Target=2, NonTarget=1
- **Trial interval**: [0, 0.8] s
- **File format**: MAT
- **Data preprocessed**: True

## Acquisition

- **Sampling rate**: 256.0 Hz
- **Number of channels**: 16
- **Channel types**: eeg=16
- **Channel names**: Fz, Cz, Pz, Oz, P3, P4, PO7, PO8, F3, F4, FCz, C3, C4, CP3, CPz, CP4
- **Montage**: 10-10
- **Hardware**: g.USBamp
- **Software**: BCI2000
- **Reference**: linked earlobes
- **Ground**: right mastoid
- **Sensor type**: Ag/AgCl
- **Line frequency**: 50.0 Hz
- **Online filters**: bandpass 0.1-20 Hz
- **Impedance threshold**: 10.0 kOhm
- **Cap manufacturer**: Electro-Cap International, Inc.

## Participants

- **Number of subjects**: 10
- **Health status**: healthy
- **Age**: mean=26.8, std=5.6
- **Gender distribution**: female=10, male=0
- **BCI experience**: experienced
- **Species**: human

## Experimental Protocol

- **Paradigm**: p300
- **Task type**: spelling
- **Number of classes**: 2
- **Class labels**: Target, NonTarget
- **Trial duration**: 16.0 s
- **Study design**: P300-based BCI with two interfaces: P300 Speller (overt attention) and GeoSpell (covert attention). 36 alphanumeric characters presented. Eight stimulation sequences per trial with 16 target intensifications.
- **Feedback type**: none
- **Stimulus type**: visual_intensification
- **Stimulus modalities**: visual
- **Primary modality**: visual
- **Synchronicity**: synchronous
- **Mode**: offline
- **Training/test split**: False
- **Instructions**: Subject focused on one out of 36 different characters. At the beginning of each trial, the system prompted the subject with the character to attend. Target prompt appeared during a 2 s pre-trial interval.
- **Stimulus presentation**: stimulus_duration_ms=125, isi_ms=125, soa_ms=250, n_sequences=8, n_intensifications_per_target=16, pre_trial_interval_s=2.0, tti_min_ms=500

## HED Event Annotations

Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

```
  Target
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Target

  NonTarget
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Non-target

```
## Paradigm-Specific Parameters

- **Detected paradigm**: p300
- **Number of targets**: 36
- **Number of repetitions**: 8
- **Inter-stimulus interval**: 125.0 ms
- **Stimulus onset asynchrony**: 250.0 ms

## Data Structure

- **Trials**: 18
- **Blocks per session**: 3
- **Trials context**: 6 trials × 3 runs per session

## Preprocessing

- **Data state**: preprocessed
- **Preprocessing applied**: True
- **Steps**: bandpass filtering
- **Highpass filter**: 0.1 Hz
- **Lowpass filter**: 20.0 Hz
- **Bandpass filter**: {'low_cutoff_hz': 0.1, 'high_cutoff_hz': 20.0}
- **Filter type**: Butterworth
- **Filter order**: 8
- **Re-reference**: linked earlobes
- **Epoch window**: [0.0, 0.8]
- **Notes**: EEG acquired using g.USBamp amplifier (g.Tec, Austria), digitized at 256 Hz

## Signal Processing

- **Classifiers**: LDA, SWLDA
- **Feature extraction**: Wavelet, Time-Frequency, CWT
- **Frequency bands**: analyzed=[1.0, 20.0] Hz

## Cross-Validation

- **Method**: cross-validation
- **Folds**: 3
- **Evaluation type**: within_session

## Performance (Original Study)

- **P300 Latency Jitter Correlation**: negative correlation with accuracy

## BCI Application

- **Applications**: communication, spelling
- **Environment**: laboratory
- **Online feedback**: False

## Tags

- **Pathology**: Healthy
- **Modality**: Visual
- **Type**: P300, ERP

## Documentation

- **Description**: Complete record of P300 evoked potentials recorded with BCI2000 using two different paradigms: P300 Speller (overt attention) and GeoSpell (covert attention). 10 healthy subjects focused on one out of 36 different characters.
- **DOI**: 10.1088/1741-2560/11/3/035008
- **Associated paper DOI**: 10.3389/fnhum.2013.00732
- **License**: CC-BY-NC-ND-4.0
- **Investigators**: P Aricò, F Aloise, F Schettini, S Salinari, D Mattia, F Cincotti
- **Senior author**: F Cincotti
- **Contact**: p.arico@hsantalucia.it
- **Institution**: Fondazione Santa Lucia IRCCS
- **Department**: Neuroelectrical Imaging and BCI Lab
- **Address**: Rome, Italy
- **Country**: Italy
- **Repository**: BNCI Horizon
- **Publication year**: 2014
- **Ethics approval**: Approved by local Ethics Committee
- **Keywords**: P300 latency jitter, brain-computer interface, covert attention, wavelet analysis, single epoch

## Abstract

This dataset represents a complete record of P300 evoked potentials recorded with BCI2000 using two different paradigms: a paradigm based on the P300 Speller originally described by Farwell and Donchin in overt attention condition and a paradigm based on the GeoSpell interface used in covert attention condition. In these sessions, 10 healthy subjects focused on one out of 36 different characters. The objective was to predict the correct character in each of the provided character selection epochs.

## Methodology

Ten healthy subjects (10 female, mean age = 26.8 ± 5.6) with previous experience with P300-based BCIs attended 4 recording sessions. Scalp EEG potentials were measured using 16 Ag/AgCl electrodes arranged on an elastic cap per the 10-10 standard. Each electrode was referenced to the linked earlobes and grounded to the right mastoid. The EEG was acquired using a g.USBamp amplifier (g.Tec, Austria), digitized at 256 Hz, high pass- and low pass-filtered with cutoff frequencies of 0.1 Hz and 20 Hz, respectively. The electrode impedance did not exceed 10 kΩ. Visual stimulation, acquisition and online classification were performed with BCI2000. Each subject attended 4 recording sessions. During each session, the subject performed three runs with each of the stimulation interfaces. Each trial consisted of eight stimulation sequences, and thus, 16 intensifications of the target character. Each stimulus was intensified for 125 ms, with an inter stimulus interval (ISI) of 125 ms, yielding a 250 ms lag between the appearance of two stimuli (SOA). Pseudorandom stimulation sequences were assembled so that each target intensification would not occur within 500 ms after the previous one to avoid the attentional blink phenomenon.

## References

Riccio, A., Simione, L., Schettini, F., Pizzimenti, A., Inghilleri, M., Belardinelli, M. O., & Mattia, D. (2013). Attention and P300-based BCI performance in people with amyotrophic lateral sclerosis. Frontiers in human neuroscience, 7, 732. https://doi.org/10.3389/fnhum.2013.00732

Notes

.. note::

``BNCI2014_009`` was previously named ``BNCI2014009``. ``BNCI2014009`` will be removed in version 1.1.

.. versionadded:: 0.4.0
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.5.0 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
