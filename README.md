The Metropolitan Transportation Authority of New York City
================

<!--*Source file*
<a href='data:text/x-markdown;base64,LS0tCnRpdGxlOiAiVGhlIE1ldHJvcG9saXRhbiBUcmFuc3BvcnRhdGlvbiBBdXRob3JpdHkgb2YgTmV3IFlvcmsgQ2l0eSIKI2F1dGhvcjogQW50aG9ueSBKb3N1ZSBSb21hbgpvdXRwdXQ6IGdpdGh1Yl9kb2N1bWVudAotLS0KCmBgYHtyIHNldHVwLCBpbmNsdWRlPUZBTFNFfQprbml0cjo6b3B0c19jaHVuayRzZXQoZWNobyA9IFRSVUUpCmBgYAoKYGBge3IgaW5jbHVkZT1GQUxTRX0KIyBEb24ndCBkZWxldGUgdGhpcyBjaHVuayBpZiB5b3UgYXJlIHVzaW5nIHRoZSBEYXRhQ29tcHV0aW5nIHBhY2thZ2UKbGlicmFyeShEYXRhQ29tcHV0aW5nKQpsaWJyYXJ5KG1vc2FpYykKbGlicmFyeShtb3NhaWNEYXRhKQpsaWJyYXJ5KGRwbHlyKQpsaWJyYXJ5KGdncGxvdDIpCmBgYAoKPCEtLSpTb3VyY2UgZmlsZSoKYGBge3IsIHJlc3VsdHM9J2FzaXMnLCBlY2hvPUZBTFNFfQppbmNsdWRlU291cmNlRG9jdW1lbnRzKCkKYGBgCi0tPgoKSSB3aWxsIGJlZ2luIGFuYWx5c2luZyB0aGUgZGF0YSBwcm92aWRlZCBmcm9tIE5ldyBZb3JrIENpdHkncyB0cmFuc3BvcnRhdGlvbiBhdXRob3JpdHksIGFsc28ga25vd24gYXMgdGhlIE1UQS4gVGhlIGZvbGxvd2luZyBkYXRhIHVzZWQgd2lsbCBpbmNsdWRlIHN1Y2Nlc3MgYW5kIGZhaWx1cmUgcmF0ZXMgZm9yIGVhY2ggZGVwYXJ0bWVudC4gIApJbiBvcmRlciB0byB1c2UgdGhpcyBkYXRhLCBJIGhhZCB0byBhcHBseSB0aHJvdWdoIGl0cyB3ZWJzaXRlIGluIG9yZGVyIHRvIG9idGFpbiB0aGlzIGRhdGEuIFRoZSBnaXZlbiBkYXRhIHdpbGwgYmUgcHJvdmlkZWQgYWxvbmcgd2l0aCB0aGlzIGZpbGUsIGFuZCBpbiB0aGUgd2Vic2l0ZS4gSW4gb3JkZXIgdG8gbWFrZSB0aGlzIGRhdGEgZWFzaWVyIHRvIHJlYWQsIHRoZXJlIHdlcmUgY3N2IGZpbGVzIGNyZWF0ZWQgaW4gb3JkZXIgdG8geWllbGQgYSB2aWFibGUgZ3JhcGggYW5kIGZvciBkYXRhIHdyYW5nbGluZyBwdXJwb3Nlcy4KCmBgYHtyLCBlY2hvPVRSVUUsIG1lc3NhZ2U9RkFMU0UsIHdhcm5pbmc9RkFMU0V9CmJ1c3RyaXBkYXRhIDwtIHJlYWQuY3N2KCJidXN0cmlwLmNzdiIpCmJ1c3RyaXBkYXRhICU+JSAKICBnZ3Bsb3QoYWVzKHg9UEVSSU9EX1lFQVIseT1jb3VudCxjb2xvcj10eXBlKSkgKwogIHN0YXRfc21vb3RoKCkgKwogIGdlb21fcG9pbnQoKSArIAogIHhsYWIoIlllYXIiKSArIAogIHlsYWIoIiUgb2YgQ29tcGxldGVkIFRyaXBzIikKYGBg' target='_blank' title='User  at /Users/Anthony' download='README.Rmd'> &#8658; README.Rmd</a>  
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

![](README_files/figure-markdown_github/unnamed-chunk-3-1.png)
