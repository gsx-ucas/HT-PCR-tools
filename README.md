# HT-PCR-tools

## Introduction


This Shiny app is an interactive tools for **High throughput PCR library sequencing**, which performed for detectting gene editting effections. 

It is meant to provide an intuitive interface for researchers to easily **upload, analyze, visualize, and explore High throughput PCR library sequencing data** interactively with no prior programming knowledge in R.


## Features


Various **visualizations** and **output data** are included:

<div class="row">
  
   <div class="col-md-6">
    <div class="row BoxArea5">
      <ul>
         <li>
            <p><strong>Filtering</strong></p>
            <ul>
               <li>WT, SNP and Indel sequences</li>
            </ul>
         </li>
      </ul>
      <div class="col-md-2" style="width: 33%">
        <a class="pop">
            <div class="BoxArea4" style="width: 100%;max-width:300px;margin: 0 auto;display: block;">
                <img src="www/WT_sequence.png" alt="Workflow" style="width: 100%;max-width:300px;margin: 0 auto;display: block;max-height: 175px;"/>
            </div>
        </a>
      </div>
      <div class="col-md-2" style="width: 33%">
        <a class="pop">
            <div class="BoxArea4" style="width: 100%;max-width:300px;margin: 0 auto;display: block;">
                <img src="www/SNP_sequence.png" alt="Workflow" style="width: 100%;max-width:300px;margin: 0 auto;display: block;max-height: 175px;"/>
            </div>
        </a>
      </div>
      <div class="col-md-2" style="width: 33%">
        <a class="pop">
            <div class="BoxArea4" style="width: 100%;max-width:300px;margin: 0 auto;display: block;">
                <img src="www/Indel_sequence.png" alt="Workflow" style="width: 100%;max-width:300px;margin: 0 auto;display: block;max-height: 175px;"/>
            </div>
        </a>
      </div>
   </div>
  </div>
  
  
   <div class="col-md-6">
    <div class="row BoxArea5">
      <ul>
         <li>
            <p><strong>Mutations table</strong></p>
            <ul>
               <li>Total mutations & Indel mutation type table</li>
            </ul>
         </li>
      </ul>
      <div class="col-md-2" style="width: 50%">
        <a class="pop">
            <div class="BoxArea4" style="width: 100%;max-width:300px;margin: 0 auto;display: block;">
                <img src="www/Total_table.png" alt="Workflow" style="width: 100%;max-width:300px;margin: 0 auto;display: block;max-height: 175px;"/>
            </div>
        </a>
      </div>
      <div class="col-md-2" style="width: 50%">
        <a class="pop">
            <div class="BoxArea4" style="width: 100%;max-width:300px;margin: 0 auto;display: block;">
                <img src="www/Indel_table.png" alt="Workflow" style="width: 100%;max-width:300px;margin: 0 auto;display: block;max-height: 175px;"/>
            </div>
        </a>
      </div>
   </div>
  </div>
  
  
   <div class="col-md-6">
    <div class="row BoxArea4">
      <ul>
         <li>
            <p><strong>Results plot</strong> </p>
            <ul>
               <li>Barplots and Seqlogoplots</li>
            </ul>
         </li>
      </ul>
      <div class="col-md-6" style="width: 50%">
        <a class="pop">
            <div class="BoxArea4" style="width: 100%;max-width:300px;margin: 0 auto;display: block;">
                <img src="www/Barplot.png" alt="Workflow" style="width: 100%;max-width:300px;margin: 0 auto;display: block;max-height: 175px;"/>
            </div>
        </a>
      </div>
      <div class="col-md-6" style="width: 50%">
        <a class="pop">
            <div class="BoxArea4" style="width: 100%;max-width:300px;margin: 0 auto;display: block;">
                <img src="www/seqlogo_plot.png" alt="Workflow" style="width: 100%;max-width:300px;margin: 0 auto;display: block;max-height: 175px;"/>
            </div>
        </a>
      </div>
   </div>
  </div>
</div>

## Matters need attention

---
### 1. Install packages

- If you are using this software for the first time, run the **dependencies.R** script to install the package.

### 2. File name format

- A **fastq format** file that contains the **Raw sequenced reads.**

- If is **single-end sample**, names the sample as **sample1.fq.gz, sample2.fq.gz ...**.

- If is **paired-end sample**, names the R1 and R2 samples as **sample1_1.fq.gz sample1_2.fq.gz** respectively.

<div class="row"><hr style="border-style:none;"/></div>


## Input File & Analysis


### 1. Example data (Demo)

- For demo purposes, you can select "Example Data" and carry out the analysis to get familiar with the app.

- That will automatically load the file **example.fq.gz** from **./example_data** directory.


### 2. Upload your own data 

- Select the file in the local directory, waitting the data upload complete and then click the **Upload data** button.

- Waitting for one or two minutes, until the **Raw sequences** table show up.

<div class="col-md-4">
<div class="BoxArea4" style="width: 80%;margin: 0 left;display: block;">
    <img src="www/upload_data.png" alt="Sample file" style="width: 100%;"/>
</div>
</div>

<div class="col-md-8">
<div class="BoxArea6" style="width: 70%;margin: 0 left;display: block;">
    <img src="www/Raw_sequences.png" alt="Sample file" style="width: 100%;"/>
</div>
</div>


### 3. Prepare the target sequence

- Normally, the target sequence should be your **gRNA sequence + - 20bp**.

- There is a example of the **target Sequence structure** below:


<div class="col-md-4">
<div class="BoxArea6" style="width: 80%;margin: 0 auto;display: block;">
    <img src="www/E3_E5_sequences.png" alt="Sample file" style="width: 100%;"/>
</div>
<div class="BoxArea6" style="width: 80%;margin: 0 auto;display: block;">
    <img src="www/WT-input-sequences.png" alt="Sample file" style="width: 100%;"/>
</div>
</div>

<div class="col-md-8">
<div class="BoxArea6" style="width: 80%;margin: 0 auto;display: block;">
    <img src="www/Seq_structure.png" alt="Sample file" style="width: 100%;"/>
</div>
</div>

### 4. Data visualization

- The final result will be generated automatically.
- And the figures can be download in a **.png or .pdf** format.

<div class="col-md-12">
<p><strong>Statistics of mutation rate.</strong></p>
<div class="BoxArea6" style="width: 60%;margin: 0 left;display: block;">
    <img src="www/table_count.png" alt="Sample file" style="width: 100%; display: block;"/>
</div>
</div>

<div class="col-md-12">
<p><strong>Barplot for Total and Indel mutation rate.</strong></p>
<div class="BoxArea6" style="width: 60%;margin: 0 left;display: block;">
    <img src="www/Barplot.png" alt="Sample file" style="width: 100%; display: block;"/>
</div>
</div>

<div class="col-md-12">
<p><strong>Seqlogo Plot for SNP mutation rate.</strong></p>
<div class="BoxArea6" style="width: 60%;margin: 0 left;display: block;">
    <img src="www/seqlogo_plot.png" alt="Sample file" style="width: 100%; display: block;"/>
</div>
</div>

