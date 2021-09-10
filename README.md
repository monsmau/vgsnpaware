
# VG SNP-Aware
Sequencing technologies has provided the basis of most modern genome sequencing studies due to its high baselevel accuracy and relatively low cost. The central obstacle is in
mapping reads to the human reference genome. The reliance on a single reference human genome could introduce substantial biases in downstream analyses. Pangenomic graph reference
representations offer an attractive approach for storing genetic variations. Moreover, including known variants in the reference makes read mapping, variant calling, and genotyping variantaware. Only recently a framework for variation graphs, VG, have improved variation-aware alignment and variant calling in general. The major bottleneck of VG is its high cost of reads mapping to a variation graph. In this paper we study the problem of SNP calling on a Variation Graph and we present a fast reads alignment tool, named VG SNP-Aware. VG SNP-Aware is able align reads exactly to a variation graph and detect SNPs based on these aligned reads. The results show that VG SNP-Aware can efficiently map
reads to a variation graph with a speed of 40x w.r.t. VG and similar accuracy on SNPs detection.



# Usage 
 

VG SNP-Aware is a custom reimplementation of the map command of VG. 
To run it, replace the mapping.cpp and map_main.cpp source files on the official project (https://github.com/vgteam/vg). 

VG SNP-Aware aims to reduce the mapping time used by VG by approximating the alignment, considering only exact matches and using a depth-limited like
search on the graph. VG SNP-Aware is able to significantly reduce the time of the alignment phase. 

To use VG SNP-Aware add the sequentialSearch parameter to the VG map command:  
* vg map -f input_reads.fq -x graph.xg -g graph.gcsa --printMin --sequentialSearch -j
* vg map -f input_reads.fq -x graph.xg -g graph.gcsa --sequentialSearch -j

The printMin parameter allows to reduce the output size to only reads with one or more reference or alternative base of SNPs.

The  VG  version is v1.29.0-44-ga74417fcb "Sospiro".


# Citation
 M. Monsù, M. Comin, "Fast Alignment of Reads to a Variation Graph with Application to SNP Detection", under submission.



