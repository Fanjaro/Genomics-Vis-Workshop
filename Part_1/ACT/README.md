# Artemis Comparison Tool (ACT)

## Installation 

### Installing Java
The current Java 11 version can always be obtained from https://jdk.java.net/archive/. 

```sh
$ tar xvf openjdk-11*_bin.tar.gz
#or
$ unzip openjdk-11*_bin.zip

$ sudo apt update

$ sudo apt install default-jdk

$ java -version

$ export JAVA_HOME=”/Library/Java/JavaVirtualMachines/jdk-11.0.1.jdk/Contents/Home”

$ export PATH="$JAVA_HOME/bin:$PATH"
```
---


### Sequence and Annotation File Formats

•     EMBL format.
 
•     GenBank format.
 
•     GFF3 format. 
 
•     FASTA nucleotide sequence files can be one of the following:
 
•      Single FASTA sequence.
 
•      Multiple FASTA sequence. 
 
•      Indexed FASTA files can be read in. The files are indexed using SAMtools:

```
samtools faidx ref.fasta
```

•     Indexed GFF3 format. This can be read in and overlaid onto an indexed FASTA file. The indexed GFF3 file contains the feature annotations. To index the GFF first sort and bgzip the file and then use tabix with "-p gff" option (see the tabix manual):
 ```
(grep ^"#" in.gff; grep -v ^"#" in.gff | sort -k1,1 -k4,4n) | bgzip >
sorted.gff.gz;
 ```
 ```
tabix -p gff sorted.gff.gz
 ```
 ---
# Tutorial
<br>

### 软件界面:

![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_splash.png)
<hr>

### 读取文件
![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_cdspred0.png)
<hr>

### 选择读取文件并打开
![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_files.png)
<hr>

### 读取 fasta 文件
![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_loaded_seq.png)
<hr>

### 读取 gff 文件
![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_loaded_contigs.png)
<hr>

### 选择条件高亮CDS
![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_orf0.png)
![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_orf1.png)
![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_orf2.png)
![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_orf3.png)
![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_orf4.png)
<hr>

### 查看感兴趣的基因
![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_orf5.png)
![avatar](https://github.com/Fanjaro/Genomics-Vis-Workshop/tree/master/Part_1/artemis/img/artemis_orf6.png)