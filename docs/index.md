# Continuous Intelligence

This site provides documentation for this project.
Use the navigation to explore module-specific materials.

## How-To Guide

Many instructions are common to all our projects.

See
[⭐ **Workflow: Apply Example**](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to get these projects running on your machine.

## Project Documentation Pages (docs/)

- **Home** - this documentation landing page
- **Project Instructions** - instructions specific to this module
- **Your Files** - how to copy the example and create your version
- **Glossary** - project terms and concepts

## Additional Resources

- [Suggested Datasets](https://denisecase.github.io/pro-analytics-02/reference/datasets/cintel/)

## Custom Project

### Dataset
I used the example data from two datasets, one for a reference period and one for a current period. Each dataset included requests, errors, and total latency, which made it easy to compare how the system was performing over time.

### Signals
The original signals included average requests, errors, and latency, along with their differences and drift flags. I added an error rate signal by calculating errors divided by requests, along with a difference and drift flag to better show changes in reliability.

### Experiments
I modified the code by adding an error rate calculation to both datasets and comparing the results between the two periods. I also added a threshold and drift flag to see if the change in error rate was significant.

### Results
The results showed differences in requests, errors, latency, and error rate between the two periods. Requests and errors were still flagged as drifting, but latency was no longer considered significant after adjusting the threshold. The error rate increased and was flagged as drifting, which made it easier to see that errors were happening more often compared to the number of requests.

### Interpretation
This shows that looking at error rate gives a better picture of how the system is actually performing. Even though latency wasn’t flagged anymore, the increase in error rate shows that errors are happening more often compared to the number of requests. This helps highlight a potential reliability issue and makes it easier to decide if the system needs attention.
