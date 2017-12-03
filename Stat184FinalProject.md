The Metropolitan Transportation Authority of New York City
================

<!--*Source file*
<a href='data:text/x-markdown;base64,LS0tCnRpdGxlOiAiVGhlIE1ldHJvcG9saXRhbiBUcmFuc3BvcnRhdGlvbiBBdXRob3JpdHkgb2YgTmV3IFlvcmsgQ2l0eSIKI2F1dGhvcjogQW50aG9ueSBKb3N1ZSBSb21hbgpvdXRwdXQ6IGdpdGh1Yl9kb2N1bWVudAotLS0KCmBgYHtyIHNldHVwLCBpbmNsdWRlPUZBTFNFfQprbml0cjo6b3B0c19jaHVuayRzZXQoZWNobyA9IFRSVUUpCmBgYAoKYGBge3IgaW5jbHVkZT1GQUxTRX0KIyBEb24ndCBkZWxldGUgdGhpcyBjaHVuayBpZiB5b3UgYXJlIHVzaW5nIHRoZSBEYXRhQ29tcHV0aW5nIHBhY2thZ2UKbGlicmFyeShEYXRhQ29tcHV0aW5nKQpsaWJyYXJ5KG1vc2FpYykKbGlicmFyeShtb3NhaWNEYXRhKQpsaWJyYXJ5KGRwbHlyKQpsaWJyYXJ5KGdncGxvdDIpCmBgYAoKPCEtLSpTb3VyY2UgZmlsZSoKYGBge3IsIHJlc3VsdHM9J2FzaXMnLCBlY2hvPUZBTFNFfQppbmNsdWRlU291cmNlRG9jdW1lbnRzKCkKYGBgCi0tPgoKSSB3aWxsIGJlZ2luIGFuYWx5c2luZyB0aGUgZGF0YSBwcm92aWRlZCBmcm9tIE5ldyBZb3JrIENpdHkncyB0cmFuc3BvcnRhdGlvbiBhdXRob3JpdHksIGFsc28ga25vd24gYXMgdGhlIE1UQS4gVGhlIGZvbGxvd2luZyBkYXRhIHVzZWQgd2lsbCBpbmNsdWRlIHN1Y2Nlc3MgYW5kIGZhaWx1cmUgcmF0ZXMgZm9yIGVhY2ggZGVwYXJ0bWVudC4gIApJbiBvcmRlciB0byB1c2UgdGhpcyBkYXRhLCBJIGhhZCB0byBhcHBseSB0aHJvdWdoIGl0cyB3ZWJzaXRlIGluIG9yZGVyIHRvIG9idGFpbiB0aGlzIGRhdGEuIFRoZSBnaXZlbiBkYXRhIHdpbGwgYmUgcHJvdmlkZWQgYWxvbmcgd2l0aCB0aGlzIGZpbGUsIGFuZCBpbiB0aGUgd2Vic2l0ZS4gSW4gb3JkZXIgdG8gbWFrZSB0aGlzIGRhdGEgZWFzaWVyIHRvIHJlYWQsIHRoZXJlIHdlcmUgY3N2IGZpbGVzIGNyZWF0ZWQgaW4gb3JkZXIgdG8geWllbGQgYSB2aWFibGUgZ3JhcGggYW5kIGZvciBkYXRhIHdyYW5nbGluZyBwdXJwb3Nlcy4KCmBgYHtyLCBtZXNzYWdlPUZBTFNFLCB3YXJuaW5nPUZBTFNFfQpidXN0cmlwZGF0YSA8LSByZWFkLmNzdigiYnVzdHJpcC5jc3YiKQpidXN0cmlwZGF0YSAlPiUgCiAgZ2dwbG90KGFlcyh4PVBFUklPRF9ZRUFSLHk9Y291bnQsY29sb3I9dHlwZSkpICsKICBzdGF0X3Ntb290aCgpICsKICBnZW9tX3BvaW50KCkgKyAKICB4bGFiKCJZZWFyIikgKyAKICB5bGFiKCIlIG9mIENvbXBsZXRlZCBUcmlwcyIpCmBgYA==' target='_blank' title='User  at /Users/Anthony' download='Stat184FinalProject.Rmd'> &#8658; Stat184FinalProject.Rmd</a>  
-->
I will begin analysing the data provided from New York City's transportation authority, also known as the MTA. The following data used will include success and failure rates for each department.
In order to use this data, I had to apply through its website in order to obtain this data. The given data will be provided along with this file, and in the website. In order to make this data easier to read, there were csv files created in order to yield a viable graph and for data wrangling purposes.

``` r
bustripdata <- read.csv("bustrip.csv")
bustripdata %>% 
  ggplot(aes(x=PERIOD_YEAR,y=count,color=type)) +
  stat_smooth() +
  geom_point() + 
  xlab("Year") + 
  ylab("% of Completed Trips")
```

![](Stat184FinalProject_files/figure-markdown_github/unnamed-chunk-3-1.png)
