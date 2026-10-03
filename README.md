# Data-Cleaning-and-Transformation
Data Cleaning and Transformation Answers 

1) Handling the missing values
• Check for missing values in the 'Price' column. How would you handle products with missing price information?							
Missing numeric values  can be handled by substituting the mean or median. The median is calculated as 130. In Power Query, calculate the median and substitute null with 130.
Price ($)
1000
80
130
900
70
130
30
90
500
130
950
90
120
150
250
50
160
980
150
130
700
80
150
800
130
400
60
40
130
50
100

 • If there are products with missing categories, propose a strategy to impute or deal with these missing values effectively.			
Missing categories in products are handled by substituting them with Unknown. Using  Power Query, substitute null with Unknown.
Category
Electronics
Fashion
Kitchen
Electronics
Unknown
Electronics
Fashion
Kitchen
Electronics
Outdoor
Electronics
Unknown
Unknown
Electronics
Electronics
Accessories
Electronics
Electronics
Fashion
Outdoor
Electronics
Kitchen
Unknown
Electronics
Fashion
Kitchen
Fashion
Kitchen
Electronics
Fashion
Accessories
Correcting Inconsistent Data
• Identify any inconsistent text formats present in the "Product Name" column.					

Capitalise the first letter in the "Product Name" column.
Product Name
Laptop
Sneakers
Coffee Maker
Smartphone
Backpack
Headphones
T-Shirt
Blender
Tablet
Hiking Boots
Laptop
Sneakers
Coffee Maker
Smartwatch
Headphones
Laptop Bag
Smartwatch
Laptop
Sunglasses
Camping Tent
Camera
Microwave
Fitness Tracker
Smartphone
Sunglasses
Blender
Dress
Toaster
Fitness Tracker
Jeans
Watch


• Identify any typos present in the "Category" column.			
Electroni is present in the category column; substitute by Electronics.		
Using  the find and replace function, select the match entire cell content. 
• Use the find and replace function to standardize the text formats in the "Product Name" column and fix any typos or misspellings in the "Category" column.	
The text formats in the "Product Name" column: capitalise the first letter. Misspellings in the "Category" column in the electroni it is substituted with Electronics. Using  the find and replace function, select the match entire cell content. 

Category
Electronics
Fashion
Kitchen
Electronics
Unknown
Electronics
Fashion
Kitchen
Electronics
Outdoor
Electronics
Unknown
Unknown
Electronics
Electronics
Accessories
Electronics
Electronics
Fashion
Outdoor
Electronics
Kitchen
Unknown
Electronics
Fashion
Kitchen
Fashion
Kitchen
Electronics
Fashion
Accessories


3) Removing Duplicates:									
• Identify any duplicate rows within the dataset based on the entirety of each row, and remove them if any.								
										
Duplicate rows within the dataset based on the entirety of each row are removed. In Power Query, choose Rows and select Remove Duplicates .
									
4) Splitting and Merging Data:									
	• Split the "Product ID" column into two separate columns for " Manufacturing Date" and "Country Code". Remove unnecessary characters, if any.								
Manuafacture Date	Country Code
28-01-2026	US
15-02-2026	US
03-03-2026	US
11-04-2026	US
22-05-2026	US
07-06-2026	UK
19-07-2026	UK
23-08-2026	UK
05-09-2026	UK
14-10-2026	UK
17-06-2026	IN
25-11-2026	AU
08-12-2026	DE
18-02-2026	CA
16-04-2026	ES
21-08-2026	CA
20-08-2026	CN
27-01-2026	IT
01-03-2026	UK
14-08-2026	US
14-05-2026	RU
09-01-2026	CA
19-07-2026	BR
29-09-2026	CA
03-06-2026	CA
11-07-2026	CA
07-03-2026	CA
13-04-2026	CA
24-05-2026	CA
02-12-2026	CA
09-07-2026	FR



• Merge the "Brand Name" and "Product Name" columns into one column named "Product Brand".						
=CONCATENATE([@[Product Name]]," ",[@[Brand Name]]) Column1
Laptop Dell
Sneakers Nike
Coffee Maker Keurig
Smartphone Samsung
Backpack North Face
Headphones Sony
T-Shirt Adidas
Blender Ninja
Tablet Apple
Hiking Boots Timberland
Laptop HP
Sneakers Adidas
Coffee Maker Nespresso
Smartwatch Fitbit
Headphones Bose
Laptop Bag Samsonite
Smartwatch Huawei
Laptop Asus
Sunglasses Oakley
Camping Tent Coleman
Camera Nikon
Microwave Panasonic
Fitness Tracker Xiaomi
Smartphone Google
Sunglasses Ray-Ban
Blender Vitamix
Dress Zara
Toaster Hamilton
Fitness Tracker Garmin
Jeans Levi's
Watch Casio

5) Number Formatting:					
• Format the data type of the "Price" column to currency format. 				
Select the column and changed to currency.
Price ($)
1,000.00
80.00
130.00
900.00
70.00
130.00
30.00
90.00
500.00
130.00
950.00
90.00
120.00
150.00
250.00
50.00
160.00
980.00
150.00
130.00
700.00
80.00
150.00
800.00
130.00
400.00
60.00
40.00
130.00
50.00
100.00

	• Format the "Manufacturing Date" column to display dates in the "DD-MM-YYYY " format.
Select the date by clicking on the header .

Manufacturing Date
28-01-2026
15-02-2026
03-03-2026
11-04-2026
22-05-2026
07-06-2026
19-07-2026
23-08-2026
05-09-2026
14-10-2026
17-06-2026
25-11-2026
08-12-2026
18-02-2026
16-04-2026
21-08-2026
20-08-2026
27-01-2026
01-03-2026
14-08-2026
14-05-2026
09-01-2026
19-07-2026
29-09-2026
03-06-2026
11-07-2026
07-03-2026
13-04-2026
24-05-2026
02-12-2026
09-07-2026

							
6) Conditional Formatting
• Apply data bar or color scales conditional formatting in the "Price" column.
Select the "Price" column. Select Conditional Formatting and  Data Bar

• Create a custom rule for conditional formatting in the "Category" column to highlight cells where the category is "Electronics."								
Select the "Category" column and conditional formatting format only cells containing format and fill them with  colour in the category "Electronics."


