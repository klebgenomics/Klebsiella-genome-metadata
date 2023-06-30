# Klebsiella-genome-metadata

_Klebsiella_ genome metadata scheme, plus guidance, examples and submission template.  
  
This is a community-driven data curation effort to facilitate use and reuse of public genome collections for maximum knowledge gain. These efforts are focussed on _Klebsiella pneumoniae_ and closely related organisms in the _K. pneumoniae_ Species Complex (KpSC) and are coordinated by the [KlebNET-GSP](https://klebnet.org/) project team. The data willl be collated and made publicaly available via this repository and the [PathogenWatch](https://pathogen.watch/) website, which hosts public KpSC genome collections and reports associated genotypes.

The scheme includes two types of data fields:  
  
**1. Isolate meta-data** fields capture information about the individual KpSC isolates and their associated genome sequences, as well as the sample sources and/or hosts from which the isolates were collected.  
  
**2. Purpose of sampling** fields capture information about how and why isolates were collected and/or chosen for sequencing. These data are essential to understand the underlying biases in genome collections and to make descisions about the inclusion or exclusion of isolates for comparative and aggregate analyses.

The submission template is available [here](https://docs.google.com/spreadsheets/d/1B1G6akgdNItXsk85QsX3TZvumM1ROZZfYnt-h3FzUoA/edit?usp=sharing). Detailed instructions and guidance for data submssion can be found below. 

## Contents
[1. Data submission](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/README.md#data-submission)  
[2. Isolate metadata fields](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/README.md#isolate-metadata-fields)  
[3. Purpose of sampling fields](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/README.md#purpose-of-sampling)  
[4. Queries and suggestions](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/README.md#queries-and-suggestions)  
[5. License](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/README.md#license)  



## Data submission

The data submission template is available [here](https://docs.google.com/spreadsheets/d/1B1G6akgdNItXsk85QsX3TZvumM1ROZZfYnt-h3FzUoA/edit?usp=sharing). Please DO NOT enter data directly into this version. Please MAKE A COPY to add your own data. Once completed email or share your copy to XXXXX. 


## Isolate metadata fields

Data entries describe individual bacterial isolates and their associated sequence data. Please complete one row per isolate.  

Data fields and guidance are shown in the table below.  



| Status                               | Variable                     | Guidance                                                                                                                                                                                                                                   | Value format                                                                                                                                                                  |
| ------------------------------------ | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| REQUIRED if published                | References                   | PubMed ID for associated publication reporting genome data, DOI is acceptable for preprints only. Multiple references can be provided as a list (comma-separated). If no associated publications leave blank.                              | {text}                                                                                                                                                                        |
| REQUIRED                             | Run accession                | Sequence archive run accession; SRRxxx, ERRxxx. If multiple sequences for same ISOLATE, a list of accessions can be given (comma-seperated).                                                                                               | {text}                                                                                                                                                                        |
| REQUIRED                             | Rtudy accession              | Sequence archive study accession; PRJxxx. If multiple projects for same ISOLATE, a list of accessions can be given (comma-seperated).                                                                                                      | {text}                                                                                                                                                                        |
| REQUIRED                             | Sample accession             | NCBI Biosample;SAMNxxx, SAMExxx                                                                                                                                                                                                            | {text}                                                                                                                                                                        |
| REQUIRED                             | Experiment accession         | Sequence archive experiment accession; SRXxxx, ERXxxx. If multiple experiments for same ISOLATE, a list of accessions can be given here (comma-seperated).                                                                                 | {text}                                                                                                                                                                        |
| optional                             | Secondary sample accession   | NCBI Biosample; ERSxxx                                                                                                                                                                                                                     | {text}                                                                                                                                                                        |
| optional                             | Assembly accession           | GenBank assembly accession; GCA_xxx. The accession for the entire assembly, including chromosome and plasmids.                                                                                                                             | {text}                                                                                                                                                                        |
| optional                             | Secondary assembly accession | Genbank WGS master record accession                                                                                                                                                                                                        | {text}                                                                                                                                                                        |
| REQUIRED                             | isolate WGS                  | Indicate if the sequence represents a single cultured isolate genome or is derived from a mixed sequence / metagenome assembled genome (MAG)                                                                                               | Isolate WGS | MAG                                                                                                                                                             |
| REQUIRED                             | isolate name                 | A name that you choose for the isolate. It can have any format, but we suggest that you make it concise, unique and consistent within your lab, and as informative as possible. Every Isolate name from a single Submitter must be unique. | {text}                                                                                                                                                                        |
| REQUIRED                             | Collection year              | The year that the isolate was collected; YYYY                                                                                                                                                                                              | {int}                                                                                                                                                                         |
| REQUIRED                             | Collection month             | The month that the isolate was collected; MM                                                                                                                                                                                               | {int}                                                                                                                                                                         |
| REQUIRED                             | Collection day               | The day that the isolate was collected within the month specified in 'Collection Month'; DD                                                                                                                                                | {int}                                                                                                                                                                         |
| REQUIRED                             | Country                      | Country of isolate collection. Controlled vocabulary, choose from the list of values as defined at https://www.insdc.org/submitting-standards/country-qualifier-vocabulary/                                                                | {term}                                                                                                                                                                        |
| REQUIRED                             | Source type                  | Controlled vocabulary describing the source of the isolate. Choose the best fit term from the list.                                                                                                                                        | human | animal | food | environmental | other | missing | not applicable | not collected | not provided | restricted access                                                   |
| REQUIRED                             | Host                         | Scientific name of the host from which the isolate was collected. If not host associated, specify 'not host associated'. Controlled vocabulary as defined at https://www.ncbi.nlm.nih.gov/taxonomy                                         | {term}                                                                                                                                                                        |
| RECOMMENDED unless lat/long given    | City or region               | City or region of isolate collection                                                                                                                                                                                                       | {text}                                                                                                                                                                        |
| RECOMMENDED unless city/region given | lat_lon                      | The geographical coordinates of the location where the sample was collected. Specify as degrees latitude and longitude in format "d[d.dddd] N|S d[dd.dddd] W|E", eg, 38.98 N 77.11 W                                                       | {float}{float}                                                                                                                                                                |
| optional                             | Isolate alias                | Other IDs associated with this isolate. Multiple IDs can be given (comma-separated).                                                                                                                                                       | {text}                                                                                                                                                                        |
| optional                             | Travel associated            | For isolates collected from human hosts, indicate if associated with recent travel. Leave blank if travel status is unknown.                                                                                                               | travel associated | NOT travel associated                                                                                                                                     |
| optional                             | Travel country               | If travel associated, indicate the travel country by chossing from the list of values as defined at https://www.insdc.org/submitting-standards/country-qualifier-vocabulary/. Leave blank if unknown.                                      | {term}                                                                                                                                                                        |
| REQUIRED if host-associated          | Host tissue sampled          | Name of body site or specimen type from which the sample was obtained, such as a specific organ, tissue or clinical specimen. Choose from the list. If none of the values are appropriate, enter free text.                                | blood | cerebrospinal fluid (CSF) | urine | sputum | brochoalveolar lavage (BAL) | other respiratory | wound | skin | feces | rectal swab | throat swab | cecal swab | {text} |
| REQUIRED if host-associated          | Infection                    | For host-associated isolates, indicate if infecting or colonising isolate, or if the infection status is unknown.                                                                                                                          | infection | colonisation | unknown                                                                                                                                            |
| REQUIRED if infection                | Host disease                 | For host-associated infecting isolates, provide the name of the relevant disease e.g. pneumonia, bacteremia. Controlled vovabulary as defined at https://meshb.nlm.nih.gov/treeView                                                        | {term}                                                                                                                                                                        |
| optional                             | Infection outcome            | For host-associated and infecting isolates, indicate the broad infection outcome at 28 days post-infection.                                                                                                                                | death within 28 days | alive at 28 days | unknown                                                                                                                             |
| optional                             | Infection severity           | Indicate type of infection severity information available. If none available leave blank.                                                                                                                                                  | {text}                                                                                                                                                                        |
| optional                             | Host age group               | For human-associated isolates, indicate the age range of the host                                                                                                                                                                          | 0-30 days | 1-12 months | 1-5 years | 5-18 years | 18-60 years | >60 years | not collected | not applicable | missing                                                         |
| optional                             | Host sex                     | For host-associated isolates, indicate the biological sex of the host                                                                                                                                                                      | male | female | not collected | not applicable | missing                                                                                                                      |
| REQUIRED                             | Repeat isolate               | if other ISOLATES are sequenced from the same host infection or colonisation episode, and this entry is NOT the primary isolate in the series, indicate the primary isolate (isolate name), otherwise leave blank                          | {text}                                                                                                                                                                        |
| REQUIRED                             | Duplicate sequence           | if multiple ASSEMBLIES of the same isolate, and this entry is NOT the primary sequence in the series, indicate the primary isolate (isolate name), otherwise leave blank                                                                   | {text}                                                                                                                                                                        |
| REQUIRED                             | Collected by                 | Name of persons or institute who collected the sample                                                                                                                                                                                      | {text}                                                                                                                                                                        |
| REQUIRED                             | Lab contact                  | Contact email address for the person providing metadata. This infomration will be made available only to the KlebNET-GSP team.                                                                                                             | {text}                                                                                                                                                                        |

## Purpose of sampling

Data entries describe the purpose of sampling and the sampling strategy for the collection from which the isolate is derived. Please complete one row per isolate.  

Data fields and guidance are summarised in the table. Definitions and detailed examples are shown below.  
  
| Status                                                                                                                         | Variable                       | Guidance                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Value format                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| REQUIRED                                                                                                                       | purpose of sampling            | What was the primary purpose for the collection and sequencing of these isolates? Choose from the list. If none of the values are appropriate, enter free text. Definitions and further guidance are available at https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/README.md#purpose-of-sampling.                                                                                                                                                                                                                                    | Routine diagnostics and / or infection control | Routine surveillance | Outbreak investigation / outbreak-initiated surveillance | Research | {text}                                                                                                                                                                                                                                                       |
| REQUIRED                                                                                                                       | study population               | Give details about the host population represented in the sample. This information is essential to inform the inclusion and exclusion of studies for aggregate or comparative epidemiological analyses. Choose common values from the list, or if none of the values are appropriate, enter free text. Multiple values can be specified (comma-separated).<br><br>                                                                                                                                                                                       | Hospital patients | Intensive Care Unit patients | Primary care patients | Healthy community participants | Neonates | Clinical environment: sinks and drains | Clinical environment: surfaces | Medical devices | Hospital wastewater | Wastewater (not hospital) | Fresh water | Seawater | Soil | Rhizosphere | Plants | Livestock | Companion animals | Captive animals | Wild animals | Food | {text} |
| REQUIRED                                                                                                                       | target epi                     | Indicate the broad epidemiological category of the study. This is information is useful to inform aggregate or comparative analyses of disease-associated vs non-disease associated isolates. Choose from the list, or if none of the values are appropriate, enter free text.                                                                                                                                                                                                                                                                           | Host infection | Host colonisation | Environmental | Host infection & colonisation | Host infection, colonisation & environmental | {text}                                                                                                                                                                                                                                                                 |
| REQUIRED                                                                                                                       | selected by organism phenotype | Indicate if samples were selected for inclusion on the basis of a microbial phenotype (e.g. specific drug resistance or serotype) or if no selection was applied. This information is essential to inform studies aiming to estimate the prevalence of microbial phenotypes by study populations, geographies etc e.g. to estimate national prevalence of ceftriaxone or carbaoenem resistant isolates. The specific phenotype used for selection can be indicated in the 'selected organism phenotype' field.                                           | selected by organism phenotype | NOT selected by organism phenotype                                                                                                                                                                                                                                                                                                                                        |
| REQUIRED if selected by organism phenotype = 'selected by organism phenotype'                                                  | selected organism phenotype    | Indicate the specific microbial phenotype that was used to select isolates for collection and/or sequencing. Choose common values form the list, or if none of the values are appropriate, enter free text. Multiple values can be specified (comma-separated).                                                                                                                                                                                                                                                                                          | ceftriaxone resistance | carbapenem resistance | drug resistance (not ceftriaxone or carbapenem) | ESBL producers | carbapenemase producers | OXA producers | NDM producers | KPC producers | string-test positive | hypervirulent pathotype | serotype | {text}                                                                                                                                           |
| REQUIRED if target epi = 'Host infection' or 'Host infection & colonisation' or 'Host infection, colonisation & environmental' | selected by clinical phenotype | Indicate whether isolates were selected for inclusion on the basis of host clinical phenotype (e.g. blood stream infection, liver abcess, severe infection) or if no selection was applied. This information is essential to inform studies focussed on specific infection types or disease severity e.g. to determine serotype distributions among invasive infection isolates or compare rates of drug resistance among blood stream infections. The specific phenotype used for slection can be indicated in the 'selected clinical phenotype' field. | selected by clinical phenotype | NOT selected by clinical phenotype                                                                                                                                                                                                                                                                                                                                        |
| REQUIRED if selected by clinical phenotype = 'selected by clinical phenotype'                                                  | selected clinical phenotype    | Indicate the specific clinical phenotype that was used to select samples for collection and/or sequencing. Choose common values from the list, or if none of the values are appropriate, enter free text. Multiple values can be specified (comma-separated).                                                                                                                                                                                                                                                                                            | liver abscess | invasive infection | blood stream infection | respiratory infection | urinary tract infection | respiratory carriage | gut carriage | skin carriage | hospital acquired infection | community acquired infection | severe disease | {text}                                                                                                                                                 |
| RECOMMENDED                                                                                                                    | sampling period start          | Indicate when the sample collection began (YYYY, or YYYY-MM or YYYY-MM-DD). This information is useful for understanding the temporal coverage of data to inform trend analysis.                                                                                                                                                                                                                                                                                                                                                                         | {ISO format}                                                                                                                                                                                                                                                                                                                                                                                               |
| RECOMMENDED                                                                                                                    | sampling period end            | Indicate when the sample collection ended (YYYY, or YYYY-MM or YYYY-MM-DD). This information is useful for understanding the temporal coverage of data to inform trend analysis. If collection and sequencing are on-going, leave blank.                                                                                                                                                                                                                                                                                                                 | {ISO format}                                                                                                                                                                                                                                                                                                                                                                                               |
  

### Purpose of sampling definitions

#### Routine diagnostics and / or infection control
Samples collected through the **routine** and **ongoing** activities of clinical or veterinary microbiology laboratories for the purposes of **clinical diagnosis and/or infection control**. May include isolates confirmed as infecting agents and/or those considered as asymptomatic or environmental colonisers e.g. isolates identified from hospital sinks or patient screening swabs as part of routine infection prevention and control procedures.
 
#### Routine surveillance
Samples collected through the **routine** and **ongoing** activities of other laboratories (not clinical or veterinary microbiology laboratories) and/or collected **for purposes other than clinical diagnostics and infection control** e.g. laboratories processing samples from non-healthcare environmental sources or food products. 
 
#### Outbreak investigation / outbreak-initiated surveillance
Samples collected as part of a **response to a specific outbreak** e.g. within a hospital or other healthcare setting (human or veterinary). May include isolates confirmed as infecting agents and/or those considered as asymptomatic colonisers (e.g. from screening swabs) and/or those from environmental sources (e.g. hospital sinks, drains etc.)
 
#### Research
Samples collected for **specific research** purposes (excluding outbreak investigation / outbreak-initiated surveillance) that would **not have otherwise been collected** via routine diagnostics, infection control or surveillance activities as described above.

### Examples

## Queries and suggestions

We welcome queries and suggestions from the community on any aspect of the scheme. In particular, please tell us if you think we have missed key data fields or options, or if the guidance is unclear. You can contact us via the [issue tracker](https://github.com/klebgenomics/Klebsiella-genome-metadata/issues).

## License

These resources are freely available for reuse and adapatation under [GNU general public license v3](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/LICENSE). We encourage the development of similar schemes for other organisms.
