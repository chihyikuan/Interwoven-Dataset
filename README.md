# Interwoven-Dataset

This is a dataset consisting of five clips by selecting 2-3 tracks with highly interwoven streams from several music and speech recordings. Three clips are selected from the MedleyDB dataset [1], One is from the MIREX MultiF0 Development Dataset, and the final from the CHAIN-Corpus [2]. To simulate the 2-channel effect, all songs are remixed using the open-source room acoustics simulator, Roomsim[3], to simulate the performance in a room recorded by two microphones. For those tracks where F0 labels not provided in [1][2], we adopted the following procedure to get the F0 labels:

1. Use the YIN algorithm [4] to obtain a rough estimation of F0 for each frame.
2. Detect and remove the silent frames according to the RMS energy.
3. Delete the spurious pitches in order to make the pitch contour smooth.
4. Set the high and low limits of pitch detection.  

[1] Rachel M Bittner, Justin Salamon, Mike Tierney, Matthias Mauch, Chris Cannam, and Juan Pablo Bello, “Medleydb: A multitrack dataset for annotation-intensive mir research.,” in ISMIR, 2014, pp. 155–160.

[2] Fred Cummins, Marco Grimaldi, Thomas Leonard, and Juraj Simko, “The chains corpus: Characterizing individual speakers,” in Proc of SPECOM, 2006, vol. 6, pp. 431–435.

[3] D Campbell, K Palomaki, and G Brown, “A matlab simulation of “shoebox” room acoustics for use in research and teaching,” Computing and Information Systems, vol. 9, no. 3, pp.48, 2005.

[4] A. de Cheveigné and H. Kawahara, “Yin, a fundamental frequency estimator for speech and music,” J. Acoust. Soc. Amer., vol. 111, pp.1917–1930, 2002.

Chih Yi Kuan 2017/3/08
