# Small World Features 

By: Jimuel Celeste, Jr., jimueljr@ualberta.ca 

Objective: To extract small-world features from speech data. 

Small-world features for Alzheimer'd disease classification are described in Nasrolahzadeh et al. (2025). The proposed method converts a spontaneous speech recording (time series) into a visibility graph (VG). Three features are then calculated from this graph representation of speech. First is the average shortest path length (L) of the graph; second is the clustering coefficient (C); and last is the small-world parameter $\sigma$ (S) which describes the "small-worldness" of the graph. An extensive analysis of these parameters have been detailed in the cited paper; readers are referred to read their demonstrative analysis. 

In this work, the objective is to extract second-order features (statistical descriptors) from the small-world features described above. The original approach extracted the three features from speech segments. The recordings were segmented (please see Nasrolahzadeh et al. (2018) for the segmentation description) before extracting the features. Therefore, for one participant recording, there would be multiple features computed from the multiple segments from that recording. Our proposed approach is to extract features, still from the segments, but allow for the calculation of second-order features which summarizes the features from all the segments. 

The idea of second-order features is based on widely-used benchmark feature sets in the area of Cognitive Health Assessment with Machine Learning, such as ComParE 2016 (Schuller et al. 2016 and Weninger et al. 2013) and eGeMAPS (Eyben et al. 2016) which could be extracted using openSMILE (Eyben et al. 2010). In these feature sets, low-level descriptors are first extracted. In the context of small-world features, these are L, C, and S. Second-order features then pertain to statistical descriptors as in the minimum, Q1, mean, median, Q3, maximum, and standard deviation. In this proposed extended small-world feature set, these descriptors will be calculated from the L, C, and S from speech segments. 

Extended Small-World Feature Set (n=21): 
1. Average Path Length (L) x {min, Q1, mean, median, Q3, max, standard deviation} = 7 features
2. Clustering Coefficient (C) x {min, Q1, mean, median, Q3, max, standard deviation} = 7 features
3. Small-World Parameter Sigma (S) x {min, Q1, mean, median, Q3, max, standard deviation} = 7 features

References
- Eyben, F., Scherer, K. R., Schuller, B. W., Sundberg, J., Andre, E., Busso, C., Devillers, L. Y., Epps, J., Laukka, P., Narayanan, S. S., & Truong, K. P. (2016). The Geneva Minimalistic Acoustic Parameter Set (GeMAPS) for Voice Research and Affective Computing. IEEE Transactions on Affective Computing, 7(2), 190–202. https://doi.org/10.1109/TAFFC.2015.2457417
- Eyben, F., Wöllmer, M., & Schuller, B. (2010). Opensmile: The munich versatile and fast open-source audio feature extractor. Proceedings of the 18th ACM International Conference on Multimedia, 1459–1462. https://doi.org/10.1145/1873951.1874246
- Nasrolahzadeh, M., Mohammadpoory, Z., & Haddadnia, J. (2018). Higher-order spectral analysis of spontaneous speech signals in Alzheimer’s disease. Cognitive Neurodynamics, 12(6), 583–596. https://doi.org/10.1007/s11571-018-9499-8
- Nasrolahzadeh, M., Mohammadpoory, Z., & Haddadnia, J. (2025). Small-world networks propensity in spontaneous speech signals of Alzheimer’s disease: Visibility graph analysis. Scientific Reports, 15(1), 4860. https://doi.org/10.1038/s41598-025-88947-9
- Schuller, B., Steidl, S., Batliner, A., Hirschberg, J., Burgoon, J. K., Baird, A., Elkins, A., Zhang, Y., Coutinho, E., & Evanini, K. (2016). The INTERSPEECH 2016 Computational Paralinguistics Challenge: Deception, Sincerity & Native Language. Interspeech 2016, 2001–2005. https://doi.org/10.21437/Interspeech.2016-129
- Weninger, F., Eyben, F., Schuller, B. W., Mortillaro, M., & Scherer, K. R. (2013). On the Acoustics of Emotion in Audio: What Speech, Music, and Sound have in Common. Frontiers in Psychology, 4. https://doi.org/10.3389/fpsyg.2013.00292
