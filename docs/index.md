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

## Custom Project Drift Detection

## Dataset

  The datasets used for this project are the provided datasets with additions. The first dataset is the reference_metrics_bjean.csv file with 10 additional data lines added. The additional lines of data added were copy and pasted from the previous lines of data so as to keep the mean results the same. The second dataset is the current_metrics_bjean.csv file with 10 additional data lines added. These additional lines of data were added to track as lower than the mean average calculated with the intent of seeing the result changes.

## Signals

  Drift direction column was added to indicate upward, downward or no drift on requests, errors and latency columns.

## Experiments

  Changing the datasets to increase the odds of different drift direction result in requests column only.

## Results

  Adjusting the datasets to increase the odds of a different drift direction result affected the drift detection flag.The flag prior to changes read true, after changes indicated false as the mean change for that dataset affected the calculation of the difference between reference and current means when compared to the threshold. The drift column did successfully indicate the upward drift on both errors and latency colummns and successfully indicated the now false flag column as no drift.

## Interpretation

  It's likely to test drift direction, changing thresholds for drift may have yielded more result variation than adjusting the data itself. Also noteworthy is that changing the data one direction or the other doesn't also have the intended affect as the mean will adjust with it and by proxy, the difference between both dataset means. In presenting drift outcomes, it will be very beneficial to be able to indicate an upward or downward drift as that may be impactful to those receiving the information.
