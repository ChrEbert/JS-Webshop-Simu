# JS-Webshop-Simu




Although JavaScript doesn't seem to be the key technology for Webshops, it is a very interesting task to do so in terms of objectorientated programming (articles of the webshop with different features) and the usage of cookies for moving parameters to a another site.

The Files are also online: <a href="http://www.littleorange.de/garage/JS-Webshop-Simulation" target="_blank">www.littleorange.de/garage/JS-Webshop-Simulation</a>.
To check the functionality "live" please follow the link or download the files alternatively on your computer and **open the file in this case with the Microsoft Internet Explorer** (Chrome will not work, because cookies are only on uploaded html-documents allowed). For view the code, you can use the same files in this repository.

## Structure

Here you see the structure and the steps to use the webshop

<table>
  <tr>
    <td align='center'><b>Step</b></td><td align='center'><b>Site</b></td><td align='center'><b>Purpose</b></td><td align='center'><b>Short Code Description</b></td>
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







