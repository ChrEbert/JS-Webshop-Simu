# JS-Webshop-Simu




Although JavaScript doesn't seem to be the key technology for Webshops, it is a very interesting task to do so in terms of objectorientated programming (articles of the webshop with different features) and the usage of cookies for moving parameters to a another site.

The Files are also online: <a href="http://www.littleorange.de/garage/JS-Webshop-Simulation" target="_blank">www.littleorange.de/garage/JS-Webshop-Simulation</a>.
To check the functionality "live" please follow the link or download the files alternatively on your computer and **open the file in this case with the Microsoft Edge Browser** (Chrome will not work, because cookies are only on uploaded html-documents allowed). For view the code, you can use the same files in this repository.

## Structure

Here you see the structure and the steps to use the webshop

| Step | Site |     Purpose      |          Short Code Description           |
|------|------|------------------|-------------------------------------------|
|   1  | sele_kat.html | First select a Productkategory | The kategory is submitted by the function _bake_ (script on sele_kat.html) which creates the cookie "kat" (document.cookie). Before this, the cookie _kat_ is generated with past expire date, for deleting the "old" kat cookie, if it has been setted before. | 
|   2  |sele_prod.html| Select a product of the choosen product kategory by clicking on "In den Einkaufswagen". You can also increase the ammount of the former or another product after that. For finishing the ordering / switch to shopping cart view click on "Zum Warenkorb" in the beginning section of the site. You can also switch the category and return to sele_kat.html to choose further cars. | The function _t_cookie_readout_ (Skript:sele_prod.html) reads out the in sele_kat.html settet Cookie, named (Kat). The related products are attributes, respresented by the array fzg_list of the object the selected kat. The cars itself also have difference attributes, like description, price or picture, which are readed out. The implementation of the information of the html-site is carried out by html-code, which is dynamically is getting integrated by the DOM-Model via the method _inner HTML_. Through this, also the link is generated to add the car in the shopping-cart (Function **add_item2** in articel_content.js,"In den Einkaufswagen"). The ordered amount of each car is also an attribute of the object of the car, an gets increased by one, if the link is clicked. Simultaneously a cookie to save the amount is generated, the name is the object-name of the car with the ending "\_anzahl". Before this, the current amount is determined by a readout and check of all cookies concerning the described name. If no cookie exists the amount is setted as 1. |
|   3  | warenkorb_versenden.html | The whole order is displayed. You can in-/ decrease the ammount (actually with "bug" of possible negative amount, is planned to be solved). It is also planned that you can delete items. |Again, all cookies are red out using the onLoad event in the body tag, which calls the function **warenkorb_load()** (function in warenkorb_versenden.html).If the cookies name has the ending "\_anzahl" (see also previous point 2) it is a saved, ordered car-type. Also orders of previous sessions are displayed. The display of the table with the ordered data is realised again with the document.getElementById(..)**.innerHTML** method.The stringvariable therefor gets added the order data - embedded in HTML-code - of each car-type line by line **+=** operator. By in- or decreasing the ordered amount, the concerning cookie will be updated set. After this, the site gets reloaded with the **location.reload()** -Method to display the changed amount. Using the variable **cur_total** the total_ammount of each ordered car-type is derived (amount multiplicated with price, while this both attributes are numbers). To Format the price properly, the number is converted in string version, where you can easily add the Thousand-Point. This Formating is also planned for the total sum. It is also planned to display a total_sum of all orderings, a delete function, and a datatransfer possibility, probably via mail.| 

## Issues / Bugs

_No fixed order_

-[]Create a category all, to display all available cartypes





