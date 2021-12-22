# r-source_securitycheck
A Cyber Security Check of the R-source Package between two versions. This is similar to the R-source code mirror, which you can find here: https://github.com/wch/r-source/wiki/ 

## Sole Reason this Github exists:
https://community.rstudio.com/t/potential-solution-for-when-anti-virus-prevents-moving-a-temporary-installation/39576
https://community.rstudio.com/t/rstudio-viewer-not-working-failed-to-load-resource-the-server-responded-with-a-status-of-403-forbidden/64982
https://community.rstudio.com/t/anti-virus-quarantine-files-when-installing-packages/70058

The links above show there is a bit of a bug between anti-virus software and the core R package.  Its the same bug anti-randsomware software like Cylance or AWS's equivalent for Private/Public Cloud networks. Basically the anti-virus bug has resurfaced in 4.1.2, but with a whole new variant that prevents even any user (admin or not) from starting up R. This because now blocks **internet.dll** as well and does it regardless of where or how R is installed. The business problem is that prevents both the stable installation of R and **more important** the ability of IT Security from setting policies to protect R developers using R packages like notary or Rstudio's Package Manager. 

## Insights Discovered

I intent to put my insights I discover here. 

## Reproducable Steps
1) I obtained the source code from this thread: https://community.rstudio.com/t/how-can-i-compare-the-source-code-of-different-versions-of-r/124691
2) I followed the directions here to unzip the tars into the uncompress state: https://pureinfotech.com/extract-tar-gz-files-windows-10/
3) I unziped R-4.1.1.tar.gz put it in this github repository.
4) I committed as the "Repository Intialization 4.1.1"
5) I unziped R-4.1.2.tar.gz put it in this github repository
6) I committed as the "Changes from 4.1.2"
7) I then looked a internet.c file and internet folder for the differences.
