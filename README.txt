## ------------------------------------------------------
##        Name: Helen Danielson and Kate Spencer
##    Filename: README.txt
##     Section: L03 / L04
##        Date: 4/28/19
##  References: graphics.py documentation
##              https://www.google.com/url?sa=i&source=images&cd=&cad=rja&uact=8&ved=2ahUKEwja-_PgzPHhAhViQt8KHWedBdcQjRx6BAgBEAU&url=https%3A%2F%2Fwww.wilsontrollope.com%2Fproducts%2Fsoireepochettenude&psig=AOvVaw0TaAy9HfTwH0ZE1VZD_W7E&ust=1556500070455525
##				https://realpython.com/lessons/advanced-csv-reader-parameters/
##              https://docs.python.org/3/library/csv.html#csv.DictReader
##				https://www2.hm.com/en_us/customer-service/sizeguide/ladies.html
##              https://www.asos.com/infopages/SizeGuide/pgesizechart.aspx
##              http://www.zara.com/webapp/wcs/stores/servlet/ProductGuideSizeAjaxView?langId=-1&productId=1794608&storeId=11719
##              https://oldnavy.gap.com/products/size-chart.jsp#Wtops
## ------------------------------------------------------

####Files needed to run project:
graphics.py
final.py
store.py
ui.py
asos.csv
hnm.csv
oldnavy.csv
zara.csv
measurement.gif

####Explanation of how to run project:
After making sure all the files are in the same folder, run final.py.
Enter the measurements the program prompts the user for in inches (with decimals if measurement includes fractions of inches), without units. Use the diagram to know where to measure each parameter.
Click “Get Sizes” when all measurements are entered.
If you know your size in ASOS or Zara, click “Figure out your measurements”
Enter the size at one of the two stores prompted for, click “done”
If you wish to save your size calculation enter a label for the saved file of these sizes in the box, click “save”
Find the saved search in yourSizes.txt, which is created in the same folder the program was run from.

####Description of the project
This project allows users to enter their measurements and returns an estimate of what size clothing would fit them at the 
stores H&M, ASOS, Zara, and Old Navy. It also allows users to enter their known size at ASOS or Zara and returns an estimate
of their sizes at all of the other stores. 
The target audience is college-aged persons who want to wear women’s clothing, but don’t want to try items on in a store or 
are ordering clothing online.

####Description of architecture structure

we have three main files, store.py, ui.py, and final.py
first store.py, which contains the super class Store, as well as the classes HnM, Asos, Zara, and
OldNavy, all of which represent stores which the users sizes can be generated from. The Store classes store the
retailer size charts as dictionaries, and can find, print, and return the users size.

in ui.py, the user interface is generated. it takes in the Store items passes to it by final.py and generates a user interface
using graphics.py. From the opened window the user can input their measurements, or use the program to approximate their sizes
based on their sizes at either ASOS or Zara.

ui.py has three main functions: home, reverse, and sizes. Each of these functions is responsible for opening one of the windows,
first the home screen where the user has the choice to directly enter their size or try and approximate it based on their
size at either asos or zara, then the size screen that displays the users size based on their inputed measurements, and
finally reverse, which "reverse engineers" the user's size at all the available stores based on their size at ASOS or Zara.

in final.py the Classes are instantiated, and ui.py is called to open the window for user interaction. final.py also contains a
saveAS function which saves the outputted sizes as a .txt file in the same folder as the program (the file will be called
yourSizes.txt and will be created if none exists).

####Discussion of major challenge
A major challenge we overcame in the early stages of our project was working the size charts from the stores,
which we stored in csv files, into our program. The problem we were having was getting the csv files to correctly be 
imported into our store.py program, and then to split each line to put the sizes and measurements in dictionaries. A large
part of the challenge with this was that we weren’t super familiar with how csv files worked or were implemented in py 
programs, and how we could access the numbers we wanted once they were imported to the store.py file. We were able to solve
the majority of these issues by using the provided notes and sources on the course website and doing our own research into 
more of the syntax and documentation for csv files. 

