# Welcome to the SRA Toolkit Wiki
## Mission 
Part of the [mission of NCBI](https://www.ncbi.nlm.nih.gov/home/about/mission/) is to facilitate new discoveries through data analysis. The _SRA Toolkit_ supports that mission by enabling users to download and analyze sequence data.  

## What is SRA Toolkit? 
The _SRA Toolkit_ is a set of programs, also called _Tools_,  you install on your local computer or Cloud-based computer that are used for _data dumping_. 
_Data dumping_ is a technology term for extracting and copying data from one system to another.  

The SRA Toolkit offers a set of custom-designed commands that users run in a command line terminal. The commands have names that refer to their purpose: 
- **Tool**: A generic name for a command in the SRA Toolkit 
- **Dumpers**: SRA Toolkit tools that download and/or transform data
  
_Dumpers_ are primarily used for two goals: 
- To download data  
- To transform data from .sra or .sralite format to another format

The SRA Toolkit cannot download original submitted files. Instead, use the [Cloud Data Delivery Service](https://www.ncbi.nlm.nih.gov/sra/docs/data-delivery/). 


## How Do I Search for the Accessions I Need? 

### What Is an Accession? 
An _accession_ is a permanent alphanumeric reference code used to locate an NCBI database record. A _run accession_ represents a set of reads availble in the SRA and has the prefex SRR, e.g., SRR000001.
To learn more SRA terminology, see [A Few Things-to-Know-Prior-to-Using-Toolkit](https://github.com/jenpetsmit/tk_wiki/blob/main/A%20Few%20Things-to-Know-Prior-to-Using-Toolkit.md)

Some users start with a search for a specific organism and a specific library type in one of our search options: 
- [NCBI Search](https://www.ncbi.nlm.nih.gov/sra/docs/srasearch/) 
- [GCP BigQuery](https://www.ncbi.nlm.nih.gov/sra/docs/sra-bigquery/) 
- [AWS Athena](https://www.ncbi.nlm.nih.gov/sra/docs/sra-athena/) 
 
Using the Search options shown above, users can create a list of accessions. Users can use the [SRA Run Selector](https://www.ncbi.nlm.nih.gov/Traces/study/) to further narrow the search. Then they can use the many Toolkit tools (installed on a local or Cloud-based computer) to download accessions, convert formats, and evaluate the data.

# Options to Download Sequence Data 
Before you download Toolkit, learn about the some options to download sequence data: 
- [Toolkit's _Prefetch_ tool](#toolkits-prefetch-tool) 
- [Dumper Tools](#toolkits-dumper-tools)  
- [Run Browser](#run-browser) 
- [Cloud Data Delivery Service (CDDS)](#cloud-data-delivery-service) 

## Toolkit's Prefetch Tool 
When you are downloading many runs, best practice is to run the _Prefetch_ tool, which downloads the data in .sra or .sralite format.  

**Prefetch Tool Benefits**
- Downloads all the information needed to transform the data to the format needed.  
  - Once data is _prefetched_ to your local computer or Cloud-based computer, use Toolkit tools to convert the accessions from .sra or .sralite to the desired format.  
- If network connectivity is interrupted, the Prefetch tool resumes the download rather than starting over.
- [See List of Prefetch Tool Options](toolkit-tools-options.md#prefetch)
- [Read more here](https://github.com/ncbi/sra-tools/wiki/HowTo:-Access-SRA-Data)

## Toolkit's Dumper Tools 
_Dumper Tools_ are commands that either:  
- Convert data that has been _prefetched_ or 
- Download and convert data in one step
  
For large amounts of data, to download and convert in one step: 
  - May be slower  
  - May download more data than needed 
  - Will have to restart the download if there is a network interruption

 The most commonly used dumper tool is _fasterq-dump_.

## Run Browser 
_Run Browser_ is a browser-based option often used to quickly view sequences from [NCBI Search Bar](https://www.ncbi.nlm.nih.gov/sra/docs/srasearch/). Use Run Browser to download one run at a time that contains less than 5 Gbases of sequence in fasta or fastq format. 

## Cloud Data Delivery Service   
SRA data is available on the Google Cloud Platform (GCP) and Amazon Web Services (AWS) clouds. Almost all publicly available, unassembled read data and authorized-access human data, including original submitted formats, are available for download from these Cloud providers. The SRA Team created the Cloud Data Delivery Service (CDDS) to enable downloading to user's Cloud storage.  

For Cloud users use CDDS to download all SRA files, including source files and Covid files (which are the Original Submitted files) from the NCBI Cloud to your Cloud storage for free. If you  download from your Cloud storage to your local computer, you will incur egress charges from your Cloud Service Provider. See [NCBI’s blog post on CDDS Charges](https://ncbiinsights.ncbi.nlm.nih.gov/2021/09/23/sra-cloud-bucket/?utm_source=ncbi_insights&utm_medium=referral&utm_campaign=sra-data-distribution-20221215). 

Toolkit cannot download accessions in their originally submitted format or transform to original submitted format. To learn more about CDDS or for information on how to download data in Original Source format, see [Cloud Data Delivery Service (CDDS)](https://www.ncbi.nlm.nih.gov/sra/docs/data-delivery). 
The CDDS service limits downloads to approximately 5TB per 30 days. 

### Data Download Costs 
You can download SRA data without egress charges from the following options: 
- The NCBI Cloud to your Cloud storage (use CDDS)
- NCBI _on premises_ to your local computer

**Figure: SRA End User Access Costs**

![SRA End User Access Costs](images/wiki/datadownloadcosts.png)

For more information on the Cloud, see [SRA in the Cloud](https://www.ncbi.nlm.nih.gov/sra/docs/sra-cloud/) on the NCBI website and [Install Toolkit in the Cloud](01.-Downloading-SRA-Toolkit.md). 

