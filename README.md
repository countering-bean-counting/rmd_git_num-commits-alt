# num_commits_alt
Exploring alternatives to the "number of commits" metric for measuring influence

## Project Structure

Larger datasets that can't be easily stored in the repository will be stored in the "downloads" directory. Datasets that can be easily stored in the are stored in the "data" directory. The "lib" directory contains common R scripts that are used to streamline data collection and tidying.

This project explores 3 areas before diving into metrics analysis. "tidy_emails" contains work to consolidate authors in the git log and to verify the method used is sufficient for studying contributor behavior patterns. "org_affiliation" determines if the organizations identified through email host names are a sufficient heuristic for estimating institional influence on a project. Each of the proposed metrics have their own folder for in depth analysis.

## Networks

The interest here is less in identifying and analyzing individuals and more looking at trends across groups. Aggregating author activity requires attributing commits to the same author. The proposed heuristic for measuring institution influence depends upon normalization and association of host names in email addresses.

### Authors

Authors are identified through a combination of name and email address provided in the public git commit history. This information is publicly available to anyone downloading this repository. The identifier used here is a cluster id determined through a network graph structure. The goal here isn't to rank individuals but to aggregate individual activity to look for patterns.

### Institutions

When authors make commits using an email address that is not associated with a known hosted email provider, it is considered an institutional affiliation. These are grouped to gauge the significance of influence through identifiable affiliations. Individual activity is only of interest as an aggregate of the affiliated institutional activity.

## Metrics

Number of commits is a snapshot in time and gives little insight into overall patterns of repo activity. The following metrics are proposed here.

### Commit Interval

Frequency of time interval (eg, months) with at least one commit. Shows consistency in involvement over time.

### Commit Variation

Commit frequency bins per interval, or frequency of commit frequency.

### Commit Sequence

Pattern of consecutive intervals commit activity was observed (gaps and islands).

### Commit Delta

Rate of change in commit frequency.

## Validation

### Institution Affiliation

Regarding institution affiliation and influence, the working hypothesis is as follows: if an organization has a strong affiliation with a Github project, then some proportion of authors will use organization resources to commit to the project, resulting in an email address with the organization domain.

To better understand the scope of this influence, projects with known affiliations are compared to the heuristics determined through the git log.

### Metric Validation

The proposed metrics above will be computed for known projects to better understand what they might indicate. These will be compared with metrics computed for unknown projects.

## Artifacts

The end goal of this project is to produce academic quality research publications. The current goal is to publish papers on the following areas: 1) A heuristic for measuring organizational influence using the git commit log; 2) Alternative metrics to number of commits for community-based projects on Github.


