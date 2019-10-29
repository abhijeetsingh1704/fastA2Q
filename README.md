# fastA2Q

* A simple and convenient program to convert fasta sequences to fastq sequences, in casava 1.8 header format version. 

## An example of fastq header output with fastA2Q

#### @LSM:213:VGKE2RP:2:1971:12668:04830 2:N:66:CGGACGTA+GTTCACGT

```
where
@         - fastq header initial
LSM       - unique instrument name
213       - run id
VGKE2RP   - flowcell id
2         - flowcell lane
1971      - tile number within the flowcell lane
12668     - 'x'-coordinate of the cluster within the tile
04830     - 'y'-coordinate of the cluster within the tile
2         - member of a pair, 1 or 2 (paired-end or mate-pair reads only)
N         - Y if the read is filtered, N otherwise
66        - 0 when none of the control bits are on, otherwise it is an even number
CGGACGTA  - index 1 sequence
+         - connection between indexes
GTTCACGT  - index 2 sequence
```

## Usage

#### Add execution permision

```
chmod +x fastA2Q
```
### Running the program
```
fastA2Q -i /path/input_file.fasta -o /path/output_file.fastq
```
