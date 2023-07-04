# Klebsiella-genome-metadata

_Klebsiella_ genome metadata scheme, plus guidance, examples and submission template.  
  
This is a community-driven data curation effort to facilitate use and reuse of public genome collections for maximum knowledge gain. These efforts are focussed on _Klebsiella pneumoniae_ and closely related organisms in the _K. pneumoniae_ Species Complex (KpSC) and are coordinated by the [KlebNET-GSP](https://klebnet.org/) project team. The data willl be collated and made publically available via this repository and the [PathogenWatch](https://pathogen.watch/) website, which hosts public KpSC genome collections and reports associated genotypes.
  
Our goal is to collect information with broad utility to research focussed on KpSC, and that can be readily harmonised for easy and effective reuse.

The scheme includes two types of data fields:  
  
**1. Isolate metadata** fields capture information about the individual KpSC isolates and their associated genome sequences, as well as the sample sources and/or hosts from which the isolates were collected.  
  
**2. Sampling** fields capture information about how and why isolates were collected and/or chosen for sequencing. These data are essential to understand the underlying biases in genome collections, and to make descisions about the inclusion or exclusion of isolates for comparative and aggregate analyses.

The submission template is available [here](https://docs.google.com/spreadsheets/d/1B1G6akgdNItXsk85QsX3TZvumM1ROZZfYnt-h3FzUoA/edit?usp=sharing). Detailed instructions and guidance for data submission can be found below. 

## Contents
[1. Data submission](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/README.md#data-submission)  
[2. Isolate metadata fields](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/README.md#isolate-metadata-fields)  
[3. Sampling fields](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/README.md#sampling-fields)<BR>
  [- Term definitions for 'purpose of sampling'](#term-definitions-for-purpose-of-sampling)<BR>
  [- Examples of how to describe study designs using the sampling fields](#examples-of-how-to-describe-study-designs-using-the-sampling-fields)<BR>
[4. Queries and suggestions](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/README.md#queries-and-suggestions)  
[5. License](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/README.md#license)  



## Data submission

The data submission template is available [here](https://docs.google.com/spreadsheets/d/1B1G6akgdNItXsk85QsX3TZvumM1ROZZfYnt-h3FzUoA/edit?usp=sharing). Please DO NOT enter data directly into this version. Please MAKE A COPY to add your own data. Once completed, email or share your copy to TBA. 

The full list of data fields, value formats and options are shown in the tables below. 

#### Fields with restricted vocabularies
Some fields have restricted vocabularies and/or require selection from a list of predefined data values. In most cases the list of possible values can be accessed and searched via a drop-down list within the submission template (also shown in the tables below, marked 'Choose from list') and only values matching those in the list will be accepted. However, in a minority of cases the possible set of values is derived from an established ontology that is too large for inclusion within the submission template. These fields are marked as, 'Controlled vocabulary,' with a link to the appropriate ontology e.g. NCBI taxonomy database or MeSH disease ontology.

#### Fields with a list of suggested values
In some cases it is desirable to have a restricted vocabulary to support data harmonisation, but there are no appropriate predefined ontologies and too many foreseeable options to create a definitive list. In these cases, we provide a list of suggested values that we expect to capture the vast majority of scenarios, but also provide the option to enter alternative values via free text. These fields are marked in the tables below as 'Choose common values from the list, or if none are appropriate, enter free text'. The submission template includes a drop-down list of the suggested values, but will allow other values to be entered (these free text entries will be marked with warnings).

## Isolate metadata

These data describe individual bacterial isolates and their associated sequence data. Please complete one row per isolate.  

Variable fields, and guidance for completing them, are shown in the table below.

For text fields, please do  not enter 'Unknown' or 'missing' etc, just leave the field blank if you don't have any data to input.


| Status                               | Variable                     | Definition; Guidance                                                                                                                                                                                                                                   | Value format                                                                                                                                                                  |
| ------------------------------------ | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| REQUIRED if published                | References                   | PubMed ID for associated publication reporting genome data; DOI is acceptable for preprints only. Multiple references can be provided as a list (comma-separated). If no associated publications leave blank.                              | {text}                                                                                                                                                                        |
| REQUIRED                             | Run accession                | Sequence archive run accession; SRRxxx, ERRxxx. If multiple sequences for same ISOLATE, a list of accessions can be given (comma-seperated).                                                                                               | {text}                                                                                                                                                                        |
| REQUIRED                             | Project accession              | BioProject accession; PRJxxx. If multiple projects for same ISOLATE, a list of accessions can be given (comma-seperated).                                                                                                      | {text}                                                                                                                                                                        |
| REQUIRED                             | Sample accession             | BioSample accession; SAMxxx                                                                                                                                                                                                            | {text}                                                                                                                                                                        |
| REQUIRED                             | Experiment accession         | Sequence archive experiment accession; SRXxxx, ERXxxx. If multiple experiments for same ISOLATE, a list of accessions can be given here (comma-separated).                                                                                 | {text}                                                                                                                                                                        |
| optional                             | Secondary sample accession   | NCBI Biosample; ERSxxx                                                                                                                                                                                                                     | {text}                                                                                                                                                                        |
| optional                             | Assembly accession           | GenBank assembly accession; GCA_xxx. The accession for the entire assembly, including chromosome and plasmids.                                                                                                                             | {text}                                                                                                                                                                        |
| optional                             | Secondary assembly accession | Genbank WGS master record accession                                                                                                                                                                                                        | {text}                                                                                                                                                                        |
| REQUIRED                             | Isolate WGS                  | Type of sequence from which this genome was derived; Indicate if the sequence represents a single cultured isolate whole genome sequence (WGS) or is derived from a mixed sequence / metagenome assembled genome (MAG). Choose from list.                                                                                               | Isolate WGS \| MAG \| unknown                                                                                                                                                       |
| REQUIRED                             | Isolate name                 | A name that you choose for the isolate. It can have any format, but we suggest that you make it concise, unique and consistent within your lab, and as informative as possible. Every Isolate name from a single Submitter must be unique. | {text}                                                                                                                                                                        |
| REQUIRED                             | Collection year              | The year that the isolate was collected; YYYY                                                                                                                                                                                              | {int}                                                                                                                                                                         |
| REQUIRED                             | Collection month             | The month that the isolate was collected; MM                                                                                                                                                                                               | {int}                                                                                                                                                                         |
| REQUIRED                             | Collection day               | The day that the isolate was collected within the month specified in 'Collection month'; DD                                                                                                                                                | {int}                                                                                                                                                                         |
| REQUIRED                             | Country                      | Country of isolate collection. Controlled vocabulary, choose from the list of values as defined at https://www.insdc.org/submitting-standards/country-qualifier-vocabulary/                                                                | {term}                                                                                                                                                                        |
| REQUIRED                             | Source type                  | Controlled vocabulary describing the source of the isolate. Choose from the list.                                                                                                                                        | human \| animal \| food \| environmental \| other \| missing \| not applicable \| not collected \| not provided \| restricted access                                                   |
| REQUIRED                             | Host                         | Scientific name of the host from which the isolate was collected. If not host associated, specify 'not host associated'. Controlled vocabulary as defined at https://www.ncbi.nlm.nih.gov/taxonomy                                         | {term}                                                                                                                                                                        |
| RECOMMENDED unless lat/long given    | City or region               | City or region of isolate collection.                                                                                                                                                                                                       | {text}                                                                                                                                                                        |
| RECOMMENDED unless city/region given | lat_lon                      | The geographical coordinates of the location where the sample was collected. Specify as degrees latitude and longitude in format "d[d.dddd] N\|S d[dd.dddd] W\|E", eg, 38.98 N 77.11 W.                                                       | {float}{float}                                                                                                                                                                |
| optional                             | Isolate alias                | Other IDs associated with this isolate. Multiple IDs can be given (comma-separated).                                                                                                                                                       | {text}                                                                                                                                                                        |
| optional                             | Travel associated            | For isolates collected from human hosts, indicate if associated with recent travel. Leave blank if travel status is unknown.                                                                                                               | travel associated \| NOT travel associated                                                                                                                                     |
| optional                             | Travel country               | If travel associated, indicate the travel country by choosing from the list of values as defined at https://www.insdc.org/submitting-standards/country-qualifier-vocabulary/. Leave blank if unknown.                                      | {term}                                                                                                                                                                        |
| REQUIRED if host-associated          | Host tissue sampled          | Name of body site or specimen type from which the sample was obtained, such as a specific organ, tissue or clinical specimen. Choose common values from the list, or if none are appropriate, enter free text.                                | blood \| cerebrospinal fluid (CSF) \| urine \| sputum \| brochoalveolar lavage (BAL) \| other respiratory \| wound \| skin \| feces \| rectal swab \| throat swab \| cecal swab \| {text} |
| REQUIRED if host-associated          | Infection                    | For host-associated isolates, indicate if infecting or colonising isolate, or if the infection status is unknown. Choose from list.                                                                                                                         | infection \| colonisation \| unknown                                                                                                                                            |
| REQUIRED if infection                | Host disease                 | For host-associated infecting isolates, provide the name of the relevant disease e.g. pneumonia, bacteremia. Controlled vovabulary as defined at https://meshb.nlm.nih.gov/treeView                                                        | {term}                                                                                                                                                                        |
| optional                             | Infection outcome            | For host-associated and infecting isolates, indicate the broad infection outcome at 28 days post-infection. Choose from list.                                                                                                                                | death within 28 days \| alive at 28 days \| unknown                                                                                                                             |
| optional                             | Infection severity           | For host-associated infecting isolates, if severity information could be made availble (upon request), indicate the type of information here. If none available or none can be shared with the community, leave blank.                                                                                                                                                  | {text}                                                                                                                                                                        |
| optional                             | Host age group               | For human-associated isolates, indicate the age range of the host. Choose from list.                                                                                                                                                                          | 0-30 days \| 1-12 months \| 1-5 years \| 5-18 years \| 18-60 years \| >60 years \| not collected \| not applicable \| missing                                                         |
| optional                             | Host sex                     | For host-associated isolates, indicate the biological sex of the host. Choose from list.                                                                                                                                                                      | male \| female \| not collected \| not applicable \| missing                                                                                                                      |
| REQUIRED                             | Repeat isolate               | If other ISOLATES are sequenced from the same host infection or colonisation episode, and this entry is NOT the primary isolate in the series, indicate the primary isolate (isolate name), otherwise leave blank.                          | {text}                                                                                                                                                                        |
| REQUIRED                             | Duplicate sequence           | If multiple ASSEMBLIES of the same isolate, and this entry is NOT the primary sequence in the series, indicate the primary isolate (isolate name), otherwise leave blank.                                                                   | {text}                                                                                                                                                                        |
| REQUIRED                             | Collected by                 | Name of persons or institute who collected the sample.                                                                                                                                                                                      | {text}                                                                                                                                                                        |
| REQUIRED                             | Lab contact                  | Contact email address for the person providing metadata. This information will be made available only to the KlebNET-GSP team.                                                                                                             | {text}                                                                                                                                                                        |



## Sampling fields

These contextual data describe the purpose of sampling, and the sampling strategy for the collection from which each isolate is derived. Please complete one row per isolate.  

Variable fields, and guidance for completing them, are summarised in the table below. [Definitions](#term-definitions-for-purpose-of-sampling) and [detailed examples](#examples-of-how-to-describe-study-designs-using-the-sampling-fields) are also shown below the table. 

| Status                                                                                                                         | Variable                       | Guidance                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Value format                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| REQUIRED                                                                                                                       | purpose of sampling            | What was the primary purpose for the collection and sequencing of these isolates? Choose from the list, or if none of the values are appropriate, enter free text. Definitions are shown below the table.                                                                                                                                                                                                                                    | Routine diagnostics and / or infection control \| Routine surveillance \| Outbreak investigation / outbreak-initiated surveillance \| Research \| {text}                                                                                                                                                                                                                                                       |
| REQUIRED                                                                                                                       | study population               | Give details about the host population represented in the sample. This information is essential to inform the inclusion and exclusion of studies for aggregate or comparative epidemiological analyses. Choose common values from the list, or if none of the values are appropriate, enter free text. Multiple values can be specified (comma-separated).<br><br>                                                                                                                                                                                       | Hospital patients \| Intensive Care Unit (ICU) patients \| Primary care patients \| Healthy community participants \| Neonates \| Clinical environment: sinks and drains \| Clinical environment: surfaces \| Medical devices \| Hospital wastewater \| Wastewater (not hospital) \| Fresh water \| Seawater \| Soil \| Rhizosphere \| Plants \| Livestock \| Companion animals \| Captive animals \| Wild animals \| Food \| {text} |
| REQUIRED                                                                                                                       | target epi                     | Indicate the broad epidemiological category of the study. This information is useful to inform aggregate or comparative analyses of disease-associated vs non-disease associated isolates. Choose from the list, or if none of the values are appropriate, enter free text.                                                                                                                                                                                                                                                                           | Host infection \| Host colonisation \| Environmental \| Host infection & colonisation \| Host infection, colonisation & environmental \| {text}                                                                                                                                                                                                                                                                 |
| REQUIRED if target epi includes 'Host infection' | selected by clinical phenotype | Indicate whether isolates were selected for inclusion on the basis of host clinical phenotype (e.g. blood stream infection, liver abscess, severe infection) or if no selection was applied. Choose from the list. This information is essential to inform studies focussed on specific infection types or disease severity e.g. to determine serotype distributions among invasive infection isolates or compare rates of drug resistance among blood stream infections. The specific phenotype used for selection can be indicated in the 'selected clinical phenotype' field. | selected by clinical phenotype \| NOT selected by clinical phenotype                                                                                                                                                                                                                                                                                                                                        |
| REQUIRED if selected by clinical phenotype = 'selected by clinical phenotype'                                                  | selected clinical phenotype    | Indicate the specific clinical phenotype that was used to select samples for collection and/or sequencing. Choose common values from the list, or if none of the values are appropriate, enter free text. Multiple values can be specified (comma-separated).                                                                                                                                                                                                                                                                                            | liver abscess \| invasive infection \| blood stream infection \| respiratory infection \| urinary tract infection \| hospital acquired infection \| community acquired infection \| severe disease \| {text}                                                                                                                                                                                                       |
| REQUIRED                                                                                                                       | selected by organism phenotype | Indicate if samples were selected for inclusion on the basis of a microbial phenotype (e.g. specific drug resistance or serotype) or if no selection was applied. Choose from the list. This information is essential to inform studies aiming to estimate the prevalence of microbial phenotypes by study populations, geographies etc e.g. to estimate national prevalence of ceftriaxone or carbapenem resistant isolates. The specific phenotype used for selection can be indicated in the 'selected organism phenotype' field.                                           | selected by organism phenotype \| NOT selected by organism phenotype                                                                                                                                                                                                                                                                                                                                        |
| REQUIRED if selected by organism phenotype = 'selected by organism phenotype'                                                  | selected organism phenotype    | Indicate the specific microbial phenotype that was used to select isolates for collection and/or sequencing. Choose common values form the list, or if none of the values are appropriate, enter free text. Multiple values can be specified (comma-separated).                                                                                                                                                                                                                                                                                          | ceftriaxone resistance \| carbapenem resistance \| drug resistance (not ceftriaxone or carbapenem) \| ESBL producers \| carbapenemase producers \| OXA producers \| NDM producers \| KPC producers \| string-test positive \| hypervirulent pathotype \| serotype \| {text}                                                                                                                                           |
| RECOMMENDED                                                                                                                    | sampling period start          | Indicate when the sample collection began (YYYY, or YYYY-MM or YYYY-MM-DD). This information is useful for understanding the temporal coverage of data to inform trend analysis.                                                                                                                                                                                                                                                                                                                                                                         | {ISO format}                                                                                                                                                                                                                                                                                                                                                                                               |
| RECOMMENDED                                                                                                                    | sampling period end            | Indicate when the sample collection ended (YYYY, or YYYY-MM or YYYY-MM-DD). This information is useful for understanding the temporal coverage of data to inform trend analysis. If collection and sequencing are on-going, leave blank.                                                                                                                                                                                                                                                                                                                 | {ISO format}                                                                                                                                                                                                                                                                                                                                                                                               |

  

### Term definitions for purpose-of-sampling

#### Routine diagnostics and / or infection control
Samples collected through the **routine** and **ongoing** activities of clinical or veterinary microbiology laboratories for the purposes of **clinical diagnosis and/or infection control**. May include isolates confirmed as infecting agents and/or those considered as asymptomatic or environmental colonisers e.g. isolates identified from hospital sinks or patient screening swabs as part of routine infection prevention and control procedures.
 
#### Routine surveillance
Samples collected through the **routine** and **ongoing** activities of other laboratories (not clinical or veterinary microbiology laboratories) and/or collected **for purposes other than clinical diagnostics and infection control** e.g. laboratories processing samples from non-healthcare environmental sources or food products. 
 
#### Outbreak investigation / outbreak-initiated surveillance
Samples collected as part of a **response to a specific outbreak** e.g. within a hospital or other healthcare setting (human or veterinary). May include isolates confirmed as infecting agents and/or those considered as asymptomatic colonisers (e.g. from screening swabs) and/or those from environmental sources (e.g. hospital sinks, drains etc.)
 
#### Research
Samples collected for **specific research** purposes (excluding outbreak investigation / outbreak-initiated surveillance) that would **not have otherwise been collected** via routine diagnostics, infection control or surveillance activities as described above.

### Examples of how to describe study designs using the sampling fields

Below we describe various hypothetical study designs and show how the **sampling** fields would be populated for each.

#### Neonatal sepsis study
_K. pneumoniae_ were isolated from the blood of neonates via routine diagnostic procedures. All isolates collected between 1 Jan 2019 and 31 Dec 2020 were stocked and subjected to whole genome sequencing.  

<p align="center">
<img src="https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/images/neonatal_sepsis_study_example.png" alt="Neonatal sepsis study flow diagram" width="70%">
</p>
  
#### Ceftriaxone-resistant infection study
_K. pneumoniae_ identified via routine diagnostic procedures from hospitalised patients in a tertiary care centre between February 2016 and February 2018 were collected. Isolates resistant to ceftriaxone were selected for sequencing.   

<p align="center">
<img src="https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/images/cef_res_infection_study_example.png" alt="Ceftriaxone resistant infection study flow diagram" width="70%">
</p>
  
#### CPE outbreak study
In May 2019 there was a sudden increase in CPE infections in the ICU of a large tertiary care centre. Enhanced infection prevention and control procedures were activated from 18 May until 31 August when the outbreak was declared contained: rectal screening swabs were collected on patient admission and every 3 days thereafter, in addition to sink and drain screening swabs. All swabs were cultured on selective media and presumptive carbapenemase-producing _K. pneumoniae_ were sequenced alongside all carbapenem-resistant _K. pneumoniae_ identified from ICU patients via routine diagnostics procedures. 

<p align="center">
<img src="https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/images/CPE_outbreak_study_example.png" alt="CPE outbreak study flow diagram" width="70%">
</p>
  
#### CR-hvKp study
Carbapenem-resistant _K. pneumoniae_ were isolated from liver abscess patients as part of the Bacterial Infections among Diabetic Elderly Patients study, between 1 June 2018 and 30 June 2020. Strains carrying _K. pneumoniae_ carbapanemase genes were detected by PCR and string test was used to determine hypermucoidy. String test positive isolates harbouring _bla_<sub>KPC</sub> were subjected to whole genome sequencing.  

<p align="center">
<img src="https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/images/CRhvKp_study_example.png" alt="CR-hvKp study flow diagram" width="70%">
</p>
  
#### Pig gut carriage study
Veterinary researchers collected 100 faecal samples from each of six pig farms in June 2017. _K. pneumoniae_ were isolated by culture on SCIA media and subjected to whole genome sequencing as part of a One Health research project. 

<p align="center">
<img src="https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/images/pig_carriage_study_example.png" alt="Pig carriage study flow diagram" width="70%">
</p>
  
#### Water surveillance study
_K. pneumoniae_ were isolated from fresh and wastewaters in a metropolitan centre as part of routine water surveillance conducted by the Environmental Protection Authority. Since 2021 all isolates have been stocked and 100 isolates have been randomly selected for sequencing each year. Sampling and sequencing is ongoing.

<p align="center">
<img src="https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/images/water_surveillance_study_example.png" alt="Water surveillance study flow diagram" width="70%">
</p>
  
## Queries and suggestions

We welcome queries and suggestions from the community on any aspect of the scheme. In particular, please tell us if you think we have missed key data fields or options, or if the guidance is unclear. You can contact us via the [issue tracker](https://github.com/klebgenomics/Klebsiella-genome-metadata/issues).

## License

These resources are freely available for reuse and adapatation under [GNU general public license v3](https://github.com/klebgenomics/Klebsiella-genome-metadata/blob/main/LICENSE). We encourage the development of similar schemes for other organisms.
