
<!-- README.md is generated from README.Rmd. Please edit that file -->
dataspice-tutorial
==================

The goal of dataspice-tutorial is a practical exercise in creating metadata for an example field collected data product using package `dataspice`.

-   Understand basic metadata and why it is important
-   Understand where and how to store them
-   Understand how they can feed into more complex metadata objects.

------------------------------------------------------------------------

<br>

`dataspice`
-----------

Package [`dataspice`](https://github.com/ropenscilabs/dataspice) makes it easier for researchers to create basic, lightweight and concise metadata files for their datasets. Metadata fields are based on [schema.org](http://schema.org/Dataset)

<br>

Data source : NEON data portal
------------------------------

![](http://data.neonscience.org/neon-data-theme/images/logo--blue-neon-data.png)

### *Woody plant vegetation structure*

This data product contains the quality-controlled, native sampling resolution data from in-situ measurements of live and standing dead woody individuals and shrub groups, from all terrestrial NEON sites with qualifying woody vegetation. The **exact measurements collected per individual depend on growth form**, and these measurements are focused on:

-   enabling biomass and productivity estimation,
-   estimation of shrub volume and biomass
-   calibration / validation of multiple NEON airborne remote-sensing data products.

In general, comparatively large individuals that are visible to remote-sensing instruments are mapped, tagged and measured, and other smaller individuals are tagged and measured but not mapped. Smaller individuals may be subsampled according to a nested subplot approach in order to standardize the per plot sampling effort.

Structure and mapping data are reported **per individual per plot**; sampling metadata, such as per growth form sampling area, are reported per plot.

For additional details, see protocol:

-   **[NEON.DOC.000987vG](dataspice-tutorial/data/methods/NEON.DOC.000987vF.pdf): TOS Protocol and Procedure: Measurement of Vegetation Structure, and Science Design**

-   **[NEON.DOC.000914](https://github.com/annakrystalli/dataspice-tutorial/blob/master/data/methods/NEON.DOC.000914vA.pdf): TOS Science Design for Plant Biomass, Productivity and Leaf Area Index.**

------------------------------------------------------------------------

### `dataspice` exercise data

The data are a trimmed subset of data downladed from the [**NEON data portal**](http://data.neonscience.org/browse-data) after filtering for:

-   time periods between **`2015-06` - `2016-06`**

-   locations within NEON Domain area **`D01: Northeast`**

Filter returned data from **2 sites** from **`2015-6`** to **`2015-11`**.

<br>

### vst\_perplotperyear.csv

Plot level data

| namedLocation          | date       | siteID | plotID    | plotType | nlcdClass       |  decimalLatitude|  decimalLongitude| geodeticDatum | eventID         | treesPresent | shrubsPresent | lianasPresent |  totalSampledAreaTrees|  totalSampledAreaShrubSapling|  totalSampledAreaLiana| recordedBy                       |
|:-----------------------|:-----------|:-------|:----------|:---------|:----------------|----------------:|-----------------:|:--------------|:----------------|:-------------|:--------------|:--------------|----------------------:|-----------------------------:|----------------------:|:---------------------------------|
| BART\_042.basePlot.vst | 2015-06-06 | BART   | BART\_042 | tower    | deciduousForest |         44.06019|         -71.28805| WGS84         | vst\_BART\_2015 | NA           | NA            | NA            |                    800|                           400|                    800| wmtulGhdefWiPr5g1VRF0YnRBawgSBx1 |
| BART\_047.basePlot.vst | 2015-07-16 | BART   | BART\_047 | tower    | deciduousForest |         44.06496|         -71.29087| WGS84         | vst\_BART\_2015 | NA           | NA            | NA            |                    800|                           400|                    800| XdV86USKkiYZfb6rmwpnK/f2Yah5qnQO |
| BART\_047.basePlot.vst | 2015-07-21 | BART   | BART\_047 | tower    | deciduousForest |         44.06496|         -71.29087| WGS84         | vst\_BART\_2015 | NA           | NA            | NA            |                    800|                           400|                    800| XdV86USKkiYZfb6rmwpnK/f2Yah5qnQO |
| BART\_034.basePlot.vst | 2015-07-22 | BART   | BART\_034 | tower    | mixedForest     |         44.06428|         -71.28561| WGS84         | vst\_BART\_2015 | NA           | NA            | NA            |                    800|                           400|                    800| bWvVSKjgptV89BwHA3h10JNaeV+PHmDU |
| BART\_041.basePlot.vst | 2015-07-22 | BART   | BART\_041 | tower    | deciduousForest |         44.06534|         -71.28561| WGS84         | vst\_BART\_2015 | NA           | NA            | NA            |                    800|                           400|                    800| MRgCvwP2WueoGZahvpQXNZ+be1CYdCGm |
| BART\_033.basePlot.vst | 2015-07-22 | BART   | BART\_033 | tower    | deciduousForest |         44.06320|         -71.28367| WGS84         | vst\_BART\_2015 | NA           | NA            | NA            |                    800|                           100|                    800| XdV86USKkiYZfb6rmwpnK/f2Yah5qnQO |

<br>

### vst\_mappingandtagging.csv

Individual level data

| namedLocation          | date       | siteID | plotID    | eventID         | individualID             | taxonID | scientificName                 | recordedBy                       |
|:-----------------------|:-----------|:-------|:----------|:----------------|:-------------------------|:--------|:-------------------------------|:---------------------------------|
| BART\_051.basePlot.vst | 2015-08-04 | BART   | BART\_051 | vst\_BART\_2015 | NEON.PLA.D01.BART.04140  | TSCA    | Tsuga canadensis (L.) Carrière | 6HzkzFDdLaNgPi31AaqxNPsuI5nRHqWu |
| BART\_051.basePlot.vst | 2015-08-04 | BART   | BART\_051 | vst\_BART\_2015 | NEON.PLA.D01.BART.03804  | TSCA    | Tsuga canadensis (L.) Carrière | 6HzkzFDdLaNgPi31AaqxNPsuI5nRHqWu |
| BART\_034.basePlot.vst | 2015-07-22 | BART   | BART\_034 | vst\_BART\_2015 | NEON.PLA.D01.BART.02967  | FAGR    | Fagus grandifolia Ehrh.        | zODC+zTh3jdHKFo7lDoQcuNYRkWsGu3I |
| BART\_036.basePlot.vst | 2015-08-26 | BART   | BART\_036 | vst\_BART\_2015 | NEON.PLA.D01.BART.05106  | FAGR    | Fagus grandifolia Ehrh.        | zODC+zTh3jdHKFo7lDoQcuNYRkWsGu3I |
| BART\_051.basePlot.vst | 2015-08-04 | BART   | BART\_051 | vst\_BART\_2015 | NEON.PLA.D01.BART.04080  | PICEA   | Picea sp.                      | 6HzkzFDdLaNgPi31AaqxNPsuI5nRHqWu |
| BART\_039.basePlot.vst | 2015-08-04 | BART   | BART\_039 | vst\_BART\_2015 | NEON.PLA.D01.BART.02904A | TSCA    | Tsuga canadensis (L.) Carrière | 0uwWHUCkGoRVT9RpJxngFjI8cZrsFWgn |

------------------------------------------------------------------------

<br>

> ##### Citation
>
> National Ecological Observatory Network. 2018. Data Products: DP1.10098.001. Provisional data downloaded from <http://data.neonscience.org> on 2018-05-04. Battelle, Boulder, CO, USA
