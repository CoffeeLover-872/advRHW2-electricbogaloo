# Plot mCPR Data and Estimates

## Description

Function plots modern contraceptive prevalence rates (mCPR) among married women from observed data and estimates.

## Usage

```r
plot_cp(dat, est, iso_code, CI = 95)
```

## Arguments

* `dat`: A tibble containing observed mCPR values. Columns: iso, year, cp, division_numeric_code & start_date/end_date and is_in_union == Y
* `est`: A tibble containing mCPR estimates. Columns: "Country or area", iso, Year, Median, U95, L95, U80, L80.
* `iso_code`: Country ISO code for filtering data.
* `CI`: Confidence intervals to be plotted, options: 95 (default), 80, or NA (no CI plotted).

## Value

A ggplot object displaying the mCPR data and estimates, with or without confidence intervals.

## Examples

```r
plot_cp(dat, est, iso_code = 4)
plot_cp(dat, est, iso_code = 404, CI = 80)
```

