# forestTrends
This R package contains functions that use non-parametric bootstrapping to assess temporal trends for mixed models. 
This package can be installed using `pak::pkg_install('doi-nps/forestTrends')`. Previous archived 
versions of this R package can be found at <a href="www.github.com/katemmiller/forestTrends">
www.github.com/katemmiller/forestTrends</a>.

This package includes the following functions:
<ul>
<li><b>Top-level analysis functions:</b></li>
  <ul>
  <li><ins>case_boot_lmer:</ins> runs case bootstrap for lmer model with random effects and returns model output.</li>
  <li><ins>case_boot_loess:</ins> runs case bootstrap for loess smoother and return model output.   
  This is intended to be a quick and dirty check for potential trends only.</li>
  <li><ins>power_sim:</ins> calculates power to detect trends for a range of effect sizes, sample sizes, and length 
  of monitoring for mixed models using simulations and case bootstrap.</li>
  </ul>  
<li><b>Internal analysis functions:</b></li>
  <ul>
  <li><ins>case_boot_power:</ins> performs non-parametric power analyses that sample original data and 
  simulate trends over a range of effect and sample sizes using QA/QC data to estimate error where available.
  Used by power_sim.</li>
  <li><ins>case_boot_sample:</ins> resampling with replacement function used by case_boot_lmer and case_boot_loess.</li>
  <li><ins>trend_lmer:</ins> fits random effects model with lmer and return results of interest.</li>
  <li><ins>trend_loess:</ins> fits a loess model to specified data and returns results of interest.</li>
  </ul>
<li><b>Plotting functions:</b></li>
  <ul>
  <li><ins>plot_slopes:</ins> plot slopes and 95% confidence intervals from case_boot_lmer output.</li>
  <li><ins>plot_trend_response:</ins> plots response with 95% confidence intervals using output from case_boot_lmer/loess.</li>
</ul>
</ul>
