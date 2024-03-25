# About:

Since the past couple of months, I have neen hearing a lot of cancer bein diagnosed among celebrities as well as from my mother who is a medical practitioner, and most of the people who have been diagnesed are relatively in their 30's and 40's (young adults). According to the the National Cancer Institute (NCI) the median age for cancer disgnostics is 66 (https://www.cancer.gov/about-cancer/causes-prevention/risk/age#:~:text=For%20example%2C%20the%20median%20age,be%20diagnosed%20at%20any%20age).

The posible explainations for this could be:

1. Earlier diagnoses due to increased public awareness and improved screening techniques could be creating the impression of a rise in cases.
2. There's ongoing research into a potential rise in early-onset cancers (https://news.harvard.edu/gazette/story/2022/09/researchers-report-dramatic-rise-in-early-onset-cancers/). Factors like lifestyle changes, environmental exposures, or even unidentified factors could be at play.
3. Confirmation bias.

In order to confirm this here is a visualization of the cancer data.

# Dataset:

## This project uses the latest (as of March 23 2024) the latest CI5 dataset - CI5-XIIplus

## Reference:

Bray F, Colombet M, Aitken JF, Bardot A, Eser S, Galceran J, Hagenimana M, Matsuda T, Mery L, Piñeros M, Soerjomataram I, de Vries E, Wiggins C, Won Y-J, Znaor A, Ferlay J, editors (2023). Cancer Incidence in Five Continents, Vol. XII (IARC CancerBase No. 19). Lyon: International Agency for Research on Cancer. Available from: https://ci5.iarc.who.int, accessed 03/23/2024

Link: https://ci5.iarc.fr/ci5-xii/

## Details:

The overall objective of the Cancer Incidence in Five Continents (CI5) series is to make available comparable data on cancer incidence from as wide a range of geographical locations worldwide as possible. The CI5plus database contains updated annual incidence rates for 124 selected populations from 108 cancer registries published in CI5, for the longest period available (up to 2012), for all cancers and 28 major types.

The dataset contains CSV files for each continenet. Tech continent has 3 files associates woth it e.g. for American Continent, the three files are,

1. Americas.csv:  
    Contians information about the countries in the continent like area, population, country/ region name, REGISTY (country id), continent id, data starting year, data ending year.

    Columns: contains CONTINENT, AREA, REGISTRY, NAME, YEAR1, YEAR2


2. Americas_Pops.csv:
    Contians country id (REGISTRY), the year, sex (1=Male, 2=Female), total count (countfor all age groups), P0_4 to P85+ => population underrespective age group

    Columns: REGISTRY,YEAR,SEX,TOTAL,P0_4,P5_9,P10_14,P15_19,P20_24,P25_29,P30_34,P35_39,P40_44,P45_49,P50_54,P55_59,P60_64,P65_69,P70_74,P75_79,P80_84,P85+


3. Americas_Cases.csv:
    Contians REGISTRY (country id), year of record, sex (1=Male, 2=Female), CANCER: (type of cancer) (Ref: https://ci5.iarc.who.int/ci5plus/dictionaries), sum of all age groups, N0_4 to N85+ => cases as per the respective age group, N_UNK = unknown age.

    Columns: REGISTRY,YEAR,SEX,CANCER,TOTAL,N0_4,N5_9,N10_14,N15_19,N20_24,N25_29,N30_34,N35_39,N40_44,N45_49,N50_54,N55_59,N60_64,N65_69,N70_74,N75_79,N80_84,N85+,N_UNK


  ## Steps:
    The data is loaded and preprocessed to change it onto a format suitaable for visualization.
    The major processes involved are Cleaning, Pivoting, etc.
    More details are in the data.ipynb file in  this repository.
    These files are saved anter pre-precessing is completer and imported in tableau for visualization.



