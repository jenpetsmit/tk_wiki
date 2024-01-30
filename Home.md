# Welcome to the SRA Toolkit Wiki
## Mission 
Part of the mission of NCBI is to facilitate new discoveries through data analysis. SRA Toolkit supports that mission by enabling users to download and analyze sequence data.  

## What is SRA Toolkit? 
The SRA Toolkit is a set of programs, also called Tools,  you install on your local computer or Cloud-based computer used for data  dumping. Data dumping is a technology term for extracting and copying data from one system to another.  

The SRA Toolkit offers a set of custom-designed commands that users run in a command line terminal. The commands have names that refer to their purpose: 
- **Tool**: A generic name for a command in the SRA Toolkit 
- **Dumpers**: SRA Toolkit Tools that download and/or transform data 
Users primarily use dumpers for two goals: 
- Download data  
- Transform data from .sra or .sralite format to another format 
Toolkit cannot dump original submitted files. Instead, use the Cloud Data Delivery Service. 

## What Is an Accession? 
An accession is a permanent alphanumeric reference code used to locate an NCBI database record.  An accession is a permanent alphanumeric reference code used to locate an NCBI database record. A run accession represents a set of reads submitted to SRA.  

## How Do I Search for the Accessions I Need? 
Some users start with a general search for a specific organism and a specific library type in one of our search options: 
- NCBI Search 
- GCP BigQuery 
- AWS Athena 
 
Users can create a list of accessions using the Search options shown above and can use the [SRA Run Selector](https://github.com/NCBI-Hackathons/ncbi-cloud-tutorials/blob/master/SRA tutorials/tutorial_SRA_run_selector.md) to further narrow the search. Then they can use the many Toolkit tools to download accessions, convert formats, and evaluate the data

# Options to Download Sequence Data 
Before you download Toolkit, learn about the different options to download sequence data: 
- Toolkit using Prefetch Tool and/or other Dumper Tools  
- Run Browser 
- Cloud Data Delivery Service (CDDS) 

## Toolkit Prefetch Tool 
When you are downloading many runs, best practice is to run the prefetch tool, which downloads the data in .sra or .sralite format.   
Prefetch Tool Benefits 
- Downloads all the information needed to transform the data to the format needed.  
  - Once downloaded to your local computer or VM, use Toolkit tools to convert the accessions from .sra or .sralite to the desired format.  
- If network connectivity is interrupted, prefetch resumes the download rather than starting over. 

## Toolkit Dumper Tools 
Dumper Tools are commands that either:  
- Convert data that has been prefetched or 
- Download and convert data in one step or  
For large amounts of data, to download and convert in one step: 
- May be slower  
- May download more data than needed 
- Will have to restart the download if there is a network interruption 

## Run Browser 
Run Browser is a browser-based tool often used to quickly view sequences from NCBI Search Bar. Use Run Browser to download one run at a time that contains less than 5 Gbases of sequence in fasta or fastq format. 

## Cloud Data Delivery Service (CDDS)  
SRA data is available on the Google Cloud Platform (GCP) and Amazon Web Services (AWS) clouds. All publicly available, unassembled read data and authorized-access human data, including original submitted formats, are available for access and compute through these cloud providers. The SRA Team created CDDS to enable downloading to these Cloud locations.  

Toolkit cannot download accessions in their originally submitted format or transform to original submitted format. To download data in Original Source format, use Cloud Data Delivery Service (CDDS). 

## Data Download Costs 
### Toolkit 
Using Toolkit, you can download SRA data without egress charges from the following options: 
- The NCBI Cloud to your Cloud storage (use CDDS)
- NCBI to your local computer

### CDDS – Cloud Data Deliver Service 
For Cloud users use CDDS to download all SRA files, including source files and Covid files (which are the Original Submitted files) from the NCBI Cloud to your Cloud storage for free. If you  download from your Cloud storage to your local computer, you will incur egress charges from your Cloud Service Provider. See NCBI’s blog post on CDDS Charges. 
The CDDS service limits downloads to 5TB per 30 days. 
![SRA End User Access Costs](../images/home/datadownloadcosts.png)

For more information on the Cloud, see SRA in the Cloud on the NCBI website and Install Toolkit in the Cloud later in this Wiki. 
