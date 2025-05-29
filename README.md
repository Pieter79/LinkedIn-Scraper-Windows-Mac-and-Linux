# LinkedIn-Scraper-Windows-Mac-and-Linux
LinkedIn scraper Windows, MAC and Linux

Using RegEx and XPath for extraction.
These settings might not be complete ;)

1
name	
Regex		
\{"@context":"http://schema.org","@type":"Organization","name":"(.*?)"

2
url	
Regex		
\{"@context":"http://schema.org","@type":"Organization","name":".*?","url":"(.*?)"

3
streetAddress	
Regex		
"streetAddress":"(.*?)"

4
addressLocality	
Regex		
"addressLocality":"(.*?)"

5
postalCode	
Regex		
"postalCode":"(.*?)"

6
addressRegion	
Regex		
"addressRegion":"(.*?)"

7
addressCountry	
Regex		
"addressCountry":"(.*?)"

8
description	
Regex		
"description":"(.*?)"

9
numberOfEmployees	
Regex		
"numberOfEmployees":[{]"value":(.*?),"@type":"QuantitativeValue"}

10
contentUrl	
Regex		
"contentUrl":"(.*?)"

11
logo description	
Regex		
"description":"(.*?)","@type":"ImageObject"},

12
slogan	
Regex		
"slogan":"(.*?)"

13
sameAs	
Regex		
"sameAs":"(.*?)"

14
isPaidOrganization	
Regex		
isPaidOrganization":(.*?)}

15
urn li organization	
Regex		
data-semaphore-content-urn="urn:li:organization:(.*?)"

16
about us website	
XPath	
Extract Text	
//div[@class='mb-2 flex papabear:mr-3 mamabear:mr-3 babybear:flex-wrap']//dd//a[@data-tracking-control-name='about_website']

17
About us description	
XPath	
Extract Text	
//div[@class='core-section-container__content break-words']//p[starts-with(@data-test-id,'about-us__description')]

18
About us industry	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//dl//div[contains(@data-test-id,'about-us__industry')]/dd)

19
About us size	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//dl//div[contains(@data-test-id,'about-us__size')]/dd)

20
About us headquarteres	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//dl//div[contains(@data-test-id,'about-us__headquarters')]/dd)

21
About us organizationType	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//dl//div[contains(@data-test-id,'about-us__organizationType')]/dd)

22
About us foundedOn	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//dl//div[contains(@data-test-id,'about-us__foundedOn')]/dd)

23
About us specialties	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//dl//div[contains(@data-test-id,'about-us__specialties')]/dd)

24
affiliated-pages	
XPath	
Extract Text	
//a[contains(@href,'affiliated-pages')]/@href

25
similar-pages	
XPath	
Extract Text	
//a[contains(@href,'similar-pages')]/@href

26
/products/	
XPath	
Extract Text	
//a[contains(@href,'/products/')]/@href

27
/school/	
XPath	
Extract Text	
//a[contains(@href,'/school/')]/@href

28
org-employees	
XPath	
Extract Text	
//a[contains(@href,'?trk=org-employees')]/@href

29
/in/	
XPath	
Extract Text	
//a[contains(@href,'linkedin.com/in/')]/@href

30
/company/	
XPath	
Extract Text	
//a[contains(@href,'linkedin.com/company/')]/@href

31
/showcase/	
XPath	
Extract Text	
//a[contains(@href,'linkedin.com/showcase/')]/@href

32
crunchbase	
XPath	
Extract Text	
//a[contains(@href,'crunchbase.com/')]/@href

33
email	
Regex		
(?i)\\[a-z][a-z0-9\.]+[a-z]@[a-z0-9][a-z0-9-]+[a-z0-9]\.[a-z]{2,}|[a-z][a-z0-9\.]+[a-z]@[a-z0-9][a-z0-9-]+[a-z0-9]\.[a-z]{2,}

34			
Employee 1 is an influencer	
XPath	
Extract Text	
//h3[1]//span[contains(@class,'sr-only')]

35
Employee 2 is an influencer	
XPath	
Extract Text	
//h3[2]//span[contains(@class,'sr-only')]

36
Employee 3 is an influencer	
XPath	
Extract Text	
//h3[3]//span[contains(@class,'sr-only')]

37
Employee 4 is an influencer	
XPath	
Extract Text	
//h3[4]//span[contains(@class,'sr-only')]
			
38
Employee 1 name	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//ul//li[1]//a[@data-tracking-control-name='org-employees']//h3)

39
Employee 2 name	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//ul//li[2]//a[@data-tracking-control-name='org-employees']//h3)

40
Employee 3 name	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//ul//li[3]//a[@data-tracking-control-name='org-employees']//h3)

41
Employee 4 name	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//ul//li[4]//a[@data-tracking-control-name='org-employees']//h3)

42			
Employee 1 LinkedIn	
XPath	
Extract Text	
//div[@class='core-section-container__content break-words']//ul//li[1]//a[@data-tracking-control-name='org-employees']/@href

43
Employee 2 LinkedIn	
XPath	
Extract Text	
//div[@class='core-section-container__content break-words']//ul//li[2]//a[@data-tracking-control-name='org-employees']/@href

44
Employee 3 LinkedIn	
XPath	
Extract Text	
//div[@class='core-section-container__content break-words']//ul//li[3]//a[@data-tracking-control-name='org-employees']/@href

45
Employee 4 LinkedIn	
XPath	
Extract Text	
//div[@class='core-section-container__content break-words']//ul//li[4]//a[@data-tracking-control-name='org-employees']/@href
			
46
Employee 1 job title	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//ul//li[1]//a[@data-tracking-control-name='org-employees']//h4)

47
Employee 2 job title	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//ul//li[2]//a[@data-tracking-control-name='org-employees']//h4)

48
Employee 3 job title	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//ul//li[3]//a[@data-tracking-control-name='org-employees']//h4)

49
Employee 4 job title	
XPath	
Function Value	
normalize-space(//div[@class='core-section-container__content break-words']//ul//li[4]//a[@data-tracking-control-name='org-employees']//h4)
			
50			
address-0	
XPath	
Function Value	
normalize-space(//*[@id="address-0"])

51
address-1	
XPath	
Function Value	
normalize-space(//*[@id="address-1"])

52			
Bing Maps address-0	
XPath	
Extract Text	
//a[contains(@aria-describedby,'address-0')]/@href

53
Bing Maps address-1	
XPath	
Extract Text	
//a[contains(@aria-describedby,'address-1')]/@href

54			
Crunchbase Total rounds
XPath	
Function Value	
normalize-space(//div[@class='aside-section-container__content break-words']//a[starts-with(@data-tracking-control-name,'funding_all-rounds')]//span[2])

55
Crunchbase all rounds	
XPath	
Extract Text	
//div[@class='aside-section-container__content break-words']//a[starts-with(@data-tracking-control-name,'funding_all-rounds')]/@href

56
Crunchbase last round	
XPath	
Extract Text	
//a[starts-with(@data-tracking-control-name,'funding_last-round')]/@href

57
Crunchbase last round of funding	
XPath	
Function Value	
normalize-space(//div[@class='my-2']//p[2])

58
Crunchbase investor	
XPath	
Extract Text	
//a[1][contains(@data-tracking-control-name,'funding_investors')]/@href

59
Crunchbase name investors	
XPath	
Function Value	
normalize-space(//div[@class='mb-2']//a[1][@data-tracking-control-name='funding_investors'])

60			
Job position description	
XPath	
Extract Text	
//div[@class='overflow-hidden self-center grow']//h2

61
Job position at company
XPath	
Extract Text	
//div[@class='overflow-hidden self-center grow']//h3

62
Job position URL	
XPath	
Extract Text	
//div[@class='rounded-md border-1 border-solid border-color-border-faint p-1']//a/@href
			
63
Posts	
XPath	
Extract Text	
//div[@class='attributed-text-segment-list__container relative mt-1 mb-1.5 babybear:mt-0 babybear:mb-0.5']//p//a/@href

64			
JSON	
XPath	
Extract Text	
//script[@type='application/ld+json']

65
Profile URL
Regex
linkedin\.com\/\w+\/[^\/"\s\,\?]+
