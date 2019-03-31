# JS-Webshop-Simu




Although JavaScript doesn't seem to be the key technology for Webshops, it is a very interesting task to do so in terms of objectorientated programming (articles of the webshop with different features) and the usage of cookies for moving parameters to a another site.

The Files are also online: <a href="http://www.littleorange.de/garage/JS-Webshop-Simulation" target="_blank">www.littleorange.de/garage/JS-Webshop-Simulation</a>.
To check the functionality "live" please follow the link or download the files alternatively on your computer and **open the file in this case with the Microsoft Internet Explorer** (Chrome will not work, because cookies are only on uploaded html-documents allowed). For view the code, you can use the same files in this repository.

## Structure

Here you see the structure and the steps to use the webshop

<table>
  <tr>
    <td align='center' width='8'><b>Step</b></td><td align='center' width='15'><b>Site</b></td><td align='center' width='*'><b>Purpose</b></td><td align='center' width='*'><b>Short Code Description</b></td>
  </tr>
  <tr>
    <td align='center' valign='top'>
      1
    </td>
    <td align='justify' valign='top'>
    <a href='http://www.littleorange.de/garage/JS-Webshop-Simulation/sele_kat.html' target='_blank'>sele_kat.html</a>
    </td>
    <td align='justify' valign='top'>
      First select a Productkategory
    </td>
    <td align='justify' valign='top'>
      The kategory is submitted by the function *bake* (script on sele_kat.html) which creates the cookie "kat" (document.cookie). Before this, the cookie kat is generated with past expire date, for deleting the "old" kat cookie, if it has been setted before.
    </td>
  </tr>
<tr>
    <td align='center' valign='top'>
      2
    </td>
    <td align='justify' valign='top'>
    <a href='http://www.littleorange.de/garage/JS-Webshop-Simulation/sele_prod.html' target='_blank'>sele_prod.html</a>
    </td>
    <td align='justify' valign='top'>
      Select a product of the choosen product kategory by clicking on "In den Einkaufswagen". You can also increase the ammount of the   former or another product after that. For finishing the ordering / switch to shopping cart view click on "Zum Warenkorb" in the beginning section of the site. You can also switch the category and return to sele_kat.html to choose further cars.
    </td>
    <td align='justify' valign='top'>
      The function <i>t_cookie_readout</i> (Skript:<a href='http://www.littleorange.de/garage/JS-Webshop-Simulation/sele_prod.html' target='_blank'>sele_prod.html`</a>) reads out the in sele_kat.html settet Cookie, named (Kat). The related products are attributes, respresented by the array fzg_list of the object the selected kat. The cars itself also have difference attributes, like description, price or picture, which are readed out. The implementation of the information of the html-site is carried out by html-code, which is dynamically is getting integrated by the DOM-Model via the method <i>inner HTML</i>. Through this, also the link is generated to add the car in the shopping-cart (Function <b>add_item2</b> in articel_content.js,"In den Einkaufswagen"). The ordered amount of each car is also an attribute of the object of the car, an gets increased by one, if the link is clicked. Simultaneously a cookie to save the amount is generated, the name is the object-name of the car with the ending "_anzahl". Before this, the current amount is determined by a readout and check of all cookies concerning the described name. If no cookie exists the amount is setted as 1.
</td>
  
  </tr>
<tr>
    <td align='center' valign='top'>
      3
    </td>
    <td align='justify' valign='top'>
    <a href='http://www.littleorange.de/garage/JS-Webshop-Simulation/warenkorb_versenden.html' target='_blank'>warenkorb_versenden.html</a>
    </td>
    <td align='justify' valign='top'>
      The whole order is displayed. You can in-/ decrease the ammount (actually with "bug" of possible negative amount, is planned to be solved). It is also planned that you can delete items.
    </td>
    <td align='justify' valign='top'>
      Again, all cookies are red out using the onLoad event in the body tag, which calls the function <b>warenkorb_load()</b>(function in warenkorb_versenden.html).If the cookies name has the ending "_anzahl" (see also previous point 2) it is a saved, ordered car-type. Also orders of previous sessions are displayed. The display of the table with the ordered data is realised again with the document.getElementById(..).<b>innerHTML</b> method.The stringvariable therefor gets added the order data - embedded in HTML-code - of each car-type line by line +=operator. By in- or decreasing the ordered amount, the concerning cookie will be updated set. After this, the site gets reloaded with the <b>location.reload()</b> -Method to display the changed amount. Using the variable cur_total the total_ammount of each ordered car-type is derived (amount multiplicated with price, while this both attributes are numbers). To Format the price properly, the number is converted in string version, where you can easily add the Thousand-Point. This Formating is also planned for the total sum. It is also planned to display a <b>total_sum</b> of all orderings, a delete function, and a datatransfer possibility, probably via mail.
</td>
  
  </tr>











</table>

    


## Issues / Bugs

_No fixed order_

- [x] Create a category all, to display all available cartypes 
- [x] Integrate a drop down list for selecting categories
- [ ] Script Merging: All scripts should be in articel_content.js
- [ ] Implement a possibility to transfer formulardata via mailto
- [ ] Standardization of the cookie-readout-function, which is used on several steps on the orderprocess
- [x] Numberformating: price, amount and totalsums using Stringconversation and addings of points and comma
- [x] Deleteoption in shoppingcart
- [x] Deleteall option in shoppingcart
- [x] Delete item if current amount is zero
- [x] Solve the "Bug" that negative amounts can be submitted
- [ ] Implement Textfield in shopping cart for changing ammounts directly
- [x] Functionality i.t.o Cookies and Chrome, when webshopsimulation is online
- [ ] Use only english language in sitecontent and naming of files to make a consistent appearance
- [ ] Improving layouts by using CSS
- [x] Adding a total sum in shopping_cart
- [ ] Zoom In Car-picture by simultaneous mouseover the picture







