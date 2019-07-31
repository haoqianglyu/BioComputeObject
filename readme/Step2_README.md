# Step 2: Find a proper pipeline to run the data from the previous step on Galaxy
* Reference for the mentioned pipeline is [here](https://www.melbournebioinformatics.org.au/tutorials/tutorials/variant_calling_galaxy_1/variant_calling_galaxy_1/).
## 1. Login in the [Galaxy Platform](https://usegalaxy.org). Create a work history, then click the Get Data -> Upload File on the left menu bar, set the data type to fastqsanger.
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-30+at+17.10.21.png)

## 2. Search for "fastqc" on the left, it is a tool for evaluating the quality of the raw sequence data. The input FASTQ file will be selected by default. Keep the other defaults and click execute.


## 3. I will map (align) the reads with the BWA tool to the human reference genome. Here, I use Human reference genome 19 (hg19). Search for Map with BWA-MEM.
* Will you selection a reference genome...: Use a built-in genome index
* Using reference genome: set to hg19
* Single or Paired-end reads: set to Single
* Make sure your fastq file is the input file.
* Keep other options as default and click execute.

![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-31+at+14.32.44.png)

## 4. Sort the BAM file: from the Galaxy tools panel, search for "SortSam" 
* Set the input file to be the output BAM file from the previous step.
* Sort by: set to Coordinate
* Keep other options as default and click execute
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-31+at+14.33.45.png)

## 5. Examine the alignment
To examine the output sorted BAM file, we need to first convert it into readable SAM format. From the Galaxy tools panel, search for "BAM-to-SAM" 
* BAM File to Convert: select your sorted BAM file
* Keep all options as default and click execute

## 6. Assess the alignment data
We can generate some mapping statistics from the BAM file to assess the quality of our alignment.
* Run IdxStats. From the Galaxy tools panel, search for the tool "IdxStats"
* Select the sorted BAM file as input.
* Keep other options as default and click execute.
* IdxStats generates a tab-delimited output with four columns. Each line consists of a reference sequence name (e.g. a chromosome), reference sequence length, number of mapped reads and number of placed but unmapped reads.

## 7. Run Flagstat. From the Galaxy tools panel, search for "Flagstat"
* Select the sorted BAM file as input.
* Keep other options as default and click execute.



