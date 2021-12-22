# r-source_securitycheck
A Cyber Security Check of the R-source Package between two versions. This is similar to the R-source code mirror, which you can find here: https://github.com/wch/r-source/wiki/ 

## Sole Reason this Github exists:
https://community.rstudio.com/t/potential-solution-for-when-anti-virus-prevents-moving-a-temporary-installation/39576
https://community.rstudio.com/t/rstudio-viewer-not-working-failed-to-load-resource-the-server-responded-with-a-status-of-403-forbidden/64982
https://community.rstudio.com/t/anti-virus-quarantine-files-when-installing-packages/70058

The links above show there is a bit of a bug between anti-virus software and the core R package.  Its the same bug anti-randsomware software like Cylance or AWS's equivalent for Private/Public Cloud networks. Basically the anti-virus bug has resurfaced in 4.1.2, but with a whole new variant that prevents even any user (admin or not) from starting up R. This because now blocks **internet.dll** as well and does it regardless of where or how R is installed. The business problem is that prevents both the stable installation of R and **more important** the ability of IT Security from setting policies to protect R developers using R packages like notary or Rstudio's Package Manager. 

## Insights Discovered

I intent to put my insights I discover here. 
