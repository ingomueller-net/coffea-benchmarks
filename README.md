# Coffea Benchmarks
This repository offers solutions to the benchmarks listed [here](https://github.com/iris-hep/adl-benchmarks-index) completed in [Coffea](https://github.com/CoffeaTeam/coffea).

The input data file is: root://eospublic.cern.ch//eos/root-eos/benchmark/Run2012B_SingleMu.root

The solutions in the benchmarks/ folder are in response to the list linked above:

1. Plot the missing ET of all events.
2. Plot pT of all jets in all events.
3. Plot pT of jets with |η| < 1.
4. Plot the missing ET of events that have at least two jets with pT > 40 GeV.
5. Plot the missing ET of events that have an opposite-sign muon pair with an invariant mass between 60 and 120 GeV.
6. Plot pT of the trijet system with the mass closest to 172.5 GeV in each event and plot the maximum b-tagging discriminant value among the jets in the triplet.
7. Plot the sum of pT of jets with pT > 30 GeV that are not within 0.4 in ΔR of any lepton with pT > 10 GeV.
8. For events with at least three leptons and a same-flavor opposite-sign lepton pair, find the same-flavor opposite-sign lepton pair with the mass closest to 91.2 GeV and plot the transverse mass of the missing energy and the leading other lepton.

The solutions in the oldbenchmarks/ folder are in response to an older set of benchmarks, namely:

1. Plotting the Missing ET (or any event level variable).
2. Plotting the Jet pT (or any variable that is a per-event array).
3. Plotting the Jet pT for jets that have an jet pT > 20 GeV and abs(jet eta) < 1.0
4. Plotting the Missing ET for jets with at least 2 jets with Jet pT > 40 and abs(jet Eta) < 1.0
5. Plot the opposite-sign muon pair mass for all combinations of muons
6. Plot the Missing ET for events that have an opposite-sign muon pair mass in the range 60-120 GeV (double loop over single collection, math)
7. Plot the sum of the pT of jets with pT > 30 GeV that are not within 0.4 from any lepton with pt > 10 GeV (looping over two collections)
8. For events with exactly three leptons and a same-flavor opposite-sign lepton pair, find the same-flavor opposite-sign lepton pair with the mass closest to 91.2 GeV and plot the transverse mass of the missing energy and the leading other lepton.

Note that for exercise 8, the n = 3 leptons case is fairly straightforward, whereas the n >= 3 leptons case is currently far more complicated and requires the usage of numba. Both solutions have been provided, with the former in oldbenchmarks/ and the latter in benchmarks/.

I have sought to provide detailed explanations for how each of these things is done in Coffea. Therefore, a lot of the code has verbose comments, which I hope are more helpful than they are distracting!
