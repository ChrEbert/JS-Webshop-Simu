# JS-Webshop-Simu




Although JavaScript doesn't seem to be the key technology for Webshops, it is a very interesting task to do so in terms of objectorientated programming (articles of the webshop with different features) and the usage of cookies for moving parameters to a another site.

The Files are also online: <a href="http://www.littleorange.de/garage/JS-Webshop-Simulation" target="blank">
www.littleorange.de/garage/JS-Webshop-Simulation</a>. To check the functionality "live" please follow the link or download the files alternatively on your computer and * open the file in this case with the Microsoft Edge Browser * (Chrome will not work, because cookies are only on uploaded html-documents allowed). For view the code, you can use the same files in this repository.

## Structure

Here you see the structure and the steps to use the webshop

| Step | Site |     Purpose      |          Short Code Description           |
|------|------|------------------|-------------------------------------------|
|   1  | sele_kat.html | First select a Productkategory | The kategory is submitted by the function _bake_ which creates the cookie "kat" (document.cookie). Before the cookie _kat_ is generated with past expire date, for deleting the "old" kat cookie, if it has been setted before. | 
|   2  |sele_prod.html| Select a product of the choosen product kategory by clicking on "In den Einkaufswagen". You can also increase the ammount of the former or another product after that. For finishing the ordering / switch to shopping cart view click on "Zum Warenkorb" in the beginning section of the site. You can also switch the category and return to sele_kat.html to choose further cars. |
|   3  | warenkorb_versenden.html | The whole order is displayed. You can in-/ decrease the ammount (actually with "bug" of possible negative ammounts, is planned to be solved). It is also planned that you can delete items. | 


