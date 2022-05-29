# pythonTaskV2
Internship task


# Task 1
https://colab.research.google.com/drive/12oMsqrAr-IxjDbgbsx522iu6mb39wgv1?usp=sharing

* I have used Beautiful Soup for this task
* At first I loaded the .csv file and stored it in a dataframe, and extracted the country and asin lists from it.
* Since several links were from other countries, they had to be translated, therefore is used the google translator on the extracted texts from the links.
* I hve used a try-except approach from getting the information from the links.
* Title, from the span tag with attribute, id = 'productTitle'
* Price, from the span tag with class attributes, 'a-price-whole' and 'a-price-fraction'
* Rating, from the i tag with class attributes, 'a-icon a-icon-star a-star-4-5' or 'a-icon-alt'
* Review, from the span tag with id attribute, 'acrCustomerReviewText'
* Since the Product image was set differently in differently URLs, i decided to scrate all image 'src' source tags on a URL.
* Availability, from the div and span tag, with id attribute 'availability'
* With appropriate headers from all browsers, a loop is executed for all 1000 urls and a counter k is installed to get the time of execution after everyy 100 iterations.
* Everytime, a get request is sent to a URL, to get it's HTML content, an error possibility is checked. If 404 ERROR is found, proper message is delivered.
* During execution, it was found that at several instances of executing the code, several URLs were sometimes responsive, sometimes not.
* As a precautioary against blank data, products whose title could not be scraped were skipped. The data.json file uploaded here, is the one with the maximum scraping of data.
* Individual URL data is stored in a dictionary and at the end of each iteration, appended to a list.
* As a result, in the end we are left with a list of dictionaries, where each entry gives us the details of a particular product in the corresponding URL.
* The data is then saved in a JSON file and displayed.


# Bonus Task (Included in both the .ipynb files)
https://colab.research.google.com/drive/1ipAsgzb_AQhGjm7y8ggyZ-cYZU72Oi6Y?usp=sharing

* Using requests and Beautiful soup, the captcha website URL is scraped, as all img 'src' source links are scraped.
* Upon inspection of the page source, it was deduced, that the first source link, that has been scraped, contains the image of the CAPTCHA
* This image is then sent through a simple OCR program, which reads the image and maps indovidual letters to it's matching English character, and displayed.
* A GET request is sent to the URL to get the details of the form.
* Subsequently, a POST request is sent with the payload as the interpreted CAPTCHA text and the form is submitted.
