## Overview

**Purpose:** Describe the lifecycle of data in HUNT cloud and how this should be planned. All datasets on HUNT Cloud should have a lifecycle plan. <br>
**Scope:** This guide covers how to set up a lifecycle plan for ingesting and off-loading data.<br>
**Audience:** Lab coordinators and project leaders responsible for a dataset.

## Lifecycle plan for data
!!! warning "**All datasets on HUNT Cloud should have a lifecycle plan**"

A lifecycle plan is a plan that documents how that data is stored at various phases of the project/dataset. 

## Rationale
The datasets we collect can be rather large. Storing data on HUNT cloud incurs a yearly cost which will keep increasing as we amass more data on the cloud. However, cheaper storage options are offered and other storage options are available. This guide seeks to set up guiding principles for creating a data lifecycle plan, a plan that describes where data is stored during the various phases of a projects lifecycle. The guide assumes a moderately sized dataset (500GB - 4TB), but suggested modifications for particularly large or smaller datasets are covered at the end of the document.

## Suggested phases
Below are the suggested phases and storage scheme in each phase. The primary criteria for these phases are if data is currently being acquired and if that data is currently in use. The designation relates to whether the data is instantly available, typically as a copy on HUNT Cloud machine, compared to needing to be reuploaded from another storage media or reacquired from hospital backups.

!!! tip "**Acquisition phase**"
    **Description:** Data is still being acquired. <br>
    **Designation:** Hot<br>
    **Storage:** stored with back-up on HUNT Cloud<br>
    **Three copies available:** If data if available at the hospital<br>

!!! example  "**Post-acquisition phase/working phase**"
    **Description:** We are no longer acquiring new data, but the data is still being worked on actively.<br>
    **Designation:** Hot<br>
    **Storage:** stored on HUNT Cloud without back-up. Backed up to tape with redundant copy.<br>
    **Three copies available:** If data if available at the hospital<br>

!!! success "**Cold phase**"
    **Description:** Dataset is finished and no projects are currently using the data. We still need to store the data for regulatory compliance.<br>
    **Designation:** Hot/Cold<br>
    **Storage:** Stored on HUNT Cloud without back-up and backed up to tape, or completely backed up to tape.<br>
    **Three copies available:** If data if available at the hospital.<br>

!!! abstract "**Regulatory compliance**"
    **Description:** Dataset is finished and no projects are currently using the data. We still need to store the data for regulatory compliance.<br>
    **Designation:** Cold<br>
    **Storage:** Backed up to tape and/or available at the hospital.<br>
    **Three copies available:** Depends.<br>

## Criteria influencing storage strategy 
In addition to the criteria mentioned above, a couple additional may criteria influence how we chose to store out data. A core principle when storing data is the 3-2-1 rule. This states that ideally we should have 3 copies of the data, on 2 different media types where at least on copy is offsite. If the dataset can be acquired from hospital back-ups, for example from the hospital image archive system in the case of imaging, we can allow a higher risk tolerance for the data the data we store in HUNT Cloud by for example only keeping copies on tape in the cold and regulatory compliance phases.

Dataset size is another factor that may influence our decisions. For smaller datasets, offloading data to tape as a cost saving measure is not as important for larger datasets. Simpler phases can be considered for these datasets where that data is for example only offloaded to tape int he regulatory compliance phase. For larger dataset we can consider being a bit more granular in terms of the phases. Below are some examples of lifecycle plans.


!!! warning "Work in progress" 
### Examples

### Lifecycle template
[test.txt](static/test.txt){:download="test.txt"}
