# nucleosome-wrapping-index

The R code in the jupyter notebook NRS-NRI-bkps.ipynb was used for calculate NRS (nucleosome wrapping score) with various bkps, and then the NRS is transformed as z-score to derive NRI (nucleosome wrapping index). The R code in the jupyter notebook NRS-NRI-140bp.ipynb was used for calculate NRS and NRI with 140 bp as the bkp specifically.
As shown in the diagram, to calculate the NRS for a genomic interval (e.g., a 10 kb bin), we first counted the length of all the DNA fragments mapped within that interval. Then we separated the DNA fragment into two groups by a fragment length “break point (bkp)” X bp. NRS is computed as the relative deviation between the number of fragments within X-250 bp (represented by variable “a”) and the number of fragments within 50-X bp (represented by variable “b”), expressed as NRS(X) = (a-b)/(a+b). For example, if the “break point” is 140bp, then NRS(140) is computed as the relative deviation between the number of DNA fragments within 140-250 bp (longer ones) and the number of DNA fragments within 50-140 bp (shorter ones). Thus, larger NRS value indicates DNA wraps tighter on nucleosomes; smaller NRS value indicates DNA wraps looser on nucleosomes. Then the raw NRS of each break point was transformed as Z-score to derive NRI. NRI is a relative metric of wrapping degree, represent the ordering of nucleosome wrapping degree of all the genomic intervals.

![image](https://github.com/WenZengqi/nucleosome-wrapping-index/assets/34879090/5e3b9bb3-25ce-4805-9343-44f6bfaa6f8b)
