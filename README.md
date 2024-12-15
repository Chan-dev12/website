# Ex.07 Restaurant Website
# Date:15/11/2024
# AIM:
To develop a static Restaurant website to display the food items and services provided by them.

# DESIGN STEPS:
## Step 1:
Requirement collection.

## Step 2:
Creating the layout using HTML and CSS.

## Step 3:
Updating the sample content.

## Step 4:
Choose the appropriate style and color scheme.

## Step 5:
Validate the layout in various browsers.

## Step 6:
Validate the HTML code.

## Step 7:
Publish the website in the given URL.

# PROGRAM:

```
index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pizza Delight</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f8f8;
            color: #333;
        }
        header {
            background-color: #e74c3c;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }
        nav {
            margin: 15px 0;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        h1 {
            font-size: 2.5em;
        }
        .pizza-gallery {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
        }
        .pizza-item {
            text-align: center;
        }
        .pizza-item img {
            width: 100%;
            border-radius: 8px;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #e74c3c;
            color: white;
            /* position: absolute;
            bottom: 0; */
            width: 100%;
        }
        .btn {
            background-color: #e74c3c;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
        }
        .btn:hover {
            background-color: #c0392b;
        }
    </style>
</head>
<body>
    <header>
        <h1>Pizza Delight</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="order.html">Order Now</a>
            <a href="signin.html">Sign In</a>
            <a href="contact.html">Contact Us</a>
        </nav>
    </header>

    <div class="container">
        <div class="content-section">
            <h2>Welcome to Pizza Delight!</h2>
            <p>Delicious pizza, made with love, delivered to your door!</p>
            <!-- <a href="order.html" class="btn">Order Now</a> -->
        </div>

        <h2>Our Pizza Varieties</h2>
        <div class="pizza-gallery">
            <div class="pizza-item">
                {% load static %}
                <img src="{% static 'Margherita pizza.jpg' %}" alt="Margherita Pizza" style="height: 200px;">
                <p>Margherita Pizza</p>
            </div>
            <div class="pizza-item">
                <img src="{% static 'Pepperoni pizza.jpeg' %}" alt="Pepperoni Pizza" style="height: 200px;">
                <p>Pepperoni Pizza</p>
            </div>
            <div class="pizza-item">
                <img src="{% static 'Veggie pizza.jpg' %}" alt="Veggie Pizza" style="height: 200px;">
                <p>Veggie Pizza</p>
            </div>
            <div class="pizza-item">
                <img src="{% static 'BBQ Chicken pizza.jpg' %}" alt="BBQ Chicken Pizza"style="height: 200px;">
                <p>BBQ Chicken Pizza</p>
            </div>
            <div class="pizza-item">
                <img src="{% static 'Four Cheese pizza.jpeg' %}" alt="Four Cheese Pizza" style="height: 200px;">
                <p>Four Cheese Pizza</p>
            </div>
            <div class="pizza-item">
                <img src="{% static 'Hawaiian pizza.jpg' %}" alt="Hawaiian Pizza" style="height: 200px;">
                <p>Hawaiian Pizza</p>
            </div>
            <div class="pizza-item">
                <img src="{% static 'Meat Lovers pizza.jpeg' %}" alt="Meat Lovers Pizza" style="height: 200px;">
                <p>Meat Lovers Pizza</p>
            </div>
            <div class="pizza-item">
                <img src="{% static 'Spicy Paneer pizza.jpeg' %}" alt="Spicy Paneer Pizza" style="height: 200px;">
                <p>Spicy Paneer Pizza</p>
            </div>
        </div>
    </div>

    <footer>
        &copy; 2024 Pizza Delight. All Rights Reserved.
    </footer>
</body>
</html>


order.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Order Now - Pizza Delight</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f8f8;
            color: #333;
        }
        header {
            background-color: #e74c3c;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        h1 {
            font-size: 2em;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #e74c3c;
            color: white;
            
            bottom: 0;
            width: 100%;
        }
        .pizza-gallery {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }
        .pizza-item {
            text-align: center;
        }
        .pizza-item img {
            width: 100%;
            border-radius: 8px;
        }
        .order-form {
            margin-top: 30px;
        }
        form input, form select, form textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            box-sizing: border-box;
        }
        form input[type="submit"] {
            background-color: #e74c3c;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
        }
        form input[type="submit"]:hover {
            background-color: #c0392b;
        }
    </style>
</head>
<body>
    <header>
        <h1>Pizza Delight</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="order.html">Order Now</a>
            <a href="signin.html">Sign In</a>
            <a href="contact.html">Contact Us</a>
        </nav>
    </header>

    <div class="container">
        <h1>Order Your Favorite Pizza</h1>

        <div class="order-form">
            <h2>Order Now</h2>
            <form>
                <label for="pizza">Select Pizza Type:</label>
                <select id="pizza" name="pizza">
                    <option value="margherita">Margherita</option>
                    <option value="pepperoni">Pepperoni</option>
                    <option value="veggie">Veggie</option>
                    <option value="Supreme Pizza">Supreme Pizza</option>
                    <option value="Buffalo Chicken Pizza">Buffalo Chicken Pizza</option>
                    <option value="Spicy Paneer Pizza">Spicy Paneer Pizza</option>
                    <option value="Meat Lovers Pizza">Meat Lovers Pizza</option>

                </select><br><br>
    
                <label for="size">Size:</label>
                <select id="size" name="size">
                    <option value="small">Small</option>
                    <option value="medium">Medium</option>
                    <option value="large">Large</option>
                </select><br><br>
    
                <label for="address">Delivery Address:</label><br>
                <textarea id="address" name="address" rows="4" cols="50"></textarea><br><br>
    
                <input type="submit" value="Place Order">
            </form>
        </div>
    
        <footer>
            &copy; 2024 Pizza Delight. All Rights Reserved.
        </footer>
    </body>
    </html>
signin.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sign In - Pizza Delight</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f8f8;
            color: #333;
        }
        header {
            background-color: #e74c3c;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        h1 {
            font-size: 2em;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #e74c3c;
            color: white;
            position: absolute;
            bottom: 0;
            width: 100%;
        }
        form input[type="text"], form input[type="password"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            box-sizing: border-box;
        }
        form input[type="submit"] {
            background-color: #e74c3c;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
        }
        form input[type="submit"]:hover {
            background-color: #c0392b;
        }
    </style>
</head>
<body>
    <header>
        <h1>Pizza Delight</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="order.html">Order Now</a>
            <a href="signin.html">Sign In</a>
            <a href="contact.html">Contact Us</a>
        </nav>
    </header>

    <div class="container">
        <h1>Sign In</h1>
        <form>
            <label for="username">Username:</label><br>
            <input type="text" id="username" name="username"><br><br>

            <label for="password">Password:</label><br>
            <input type="password" id="password" name="password"><br><br>

            <input type="submit" value="Sign In">
        </form>
    </div>

    <footer>
        &copy; 2024 Pizza Delight. All Rights Reserved.
    </footer>
</body>
</html>
contactus.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact Us - Pizza Delight</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f8f8;
            color: #333;
        }
        header {
            background-color: #e74c3c;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
            font-weight: bold;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        h1 {
            font-size: 2em;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #e74c3c;
            color: white;
            position: absolute;
            bottom: 0;
            width: 100%;
        }
        form input[type="text"], form input[type="email"], form input[type="tel"], form textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            box-sizing: border-box;
        }
        form input[type="submit"] {
            background-color: #e74c3c;
            color: white;
            padding: 10px 20px;
            border: none;
            cursor: pointer;
        }
        form input[type="submit"]:hover {
            background-color: #c0392b;
        }
    </style>
</head>
<body>
    <header>
        <h1>Pizza Delight</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="order.html">Order Now</a>
            <a href="signin.html">Sign In</a>
            <a href="contact.html">Contact Us</a>
        </nav>
    </header>

    <div class="container">
        <h1>Contact Us</h1>
        <form>
            <label for="name">Name:</label><br>
            <input type="text" id="name" name="name" placeholder="Enter your full name" required><br><br>

            <label for="phone">Phone Number:</label><br>
            <input type="tel" id="phone" name="phone" placeholder="Enter your phone number" required><br><br>

            <label for="email">Email ID:</label><br>
            <input type="email" id="email" name="email" placeholder="Enter your email address" required><br><br>

            <label for="message">Message:</label><br>
            <textarea id="message" name="message" rows="4" placeholder="Enter your message here" required></textarea><br><br>

            <input type="submit" value="Submit">
        </form>
    </div>

    <footer>
        &copy; 2024 Pizza Delight. All Rights Reserved.
    </footer>
</body>
</html>

admin.html
<html>

<head>
    <title>Pizza Delight</title>
    <link rel="stylesheet" href="style.css">
</head>
<style>
    img{
        height: 300px;
        width: 250px;
    }
</style>

<!-- <body>
    <nav>
        <h3>Opening time : 11.00 am - 11.00 pm</h3>
        <h1 style="font-size: 80px;">Aswitha Restaurant</h1>
        <h5 style="display: inline;">&lpar;NONVEG&rpar;</h5>
        <img src="WhatsApp Image 2024-10-17 at 10.06.30_b221dd09.jpg" width="200px" height="170px"
            style="margin-left: 85px;">
        <ul>
            <li><a href="menu.html">MENU</a> |</li>
            <li><a href="admin.html">Administration</a> |</li>
            <li>COUPON |</li>
        </ul>
        <a class="box" href="C:\Users\admin\Desktop\HTML\Sub Codes\ordernow code.html">ORDER NOW!!!</a>
    </nav><br>

    <hr><br>
    <div class="searchbar">
        <input placeholder="Search">
    </div> -->

    <center>
    <h1> Our Administrators</h1>
    <div class="admin">
        {% load static %}

        <img src="{% static 'chan photo.jpg' %}" alt="">
        <img src="{% static 'priyesh.jpg' %}" alt="">
        <img src="{% static 'karthi.jpg' %}" alt="">
        <img src="{% static 'ashwin.jpg' %}" alt="">
        <img src="{% static 'gowthan.jpg' %}" alt="">
        <img src="{% static 'venkat.jpg' %}" alt="">
    </div>
    </center>
    <hr>
    <center>
    <footer>

        <div class="a">
            <p>Contact us: More information<br> </p>
        </div>
        <div class="info">
            +91 9939959945<br>
            www.pizzadelight@gmail.com<br>
            123,anna nagar,chennai
        </div>
        <p>
            Thank You Visit Again
        </p>

    </footer>
    </center>
</body>

</html>

views.py

from django.shortcuts import render
def rest(request):
    return render(request,'index 3.html')

urls.py
from django.contrib import admin 
from django.urls import path 
from restuarant import views
urlpatterns = [ 
    path('admin/', admin.site.urls), 
    path('restu/',views.rest)
]
```


# OUTPUT:
![Screenshot 2024-12-13 105042](https://github.com/user-attachments/assets/5231ba1a-789d-478c-83cc-1f4cc3ebb809)
![Screenshot 2024-12-13 110204](https://github.com/user-attachments/assets/b216361f-942c-4e22-9eed-e915638c6652)
![Screenshot 2024-12-13 111957](https://github.com/user-attachments/assets/3a376e75-dac5-44f7-81be-b26af56d90a0)
![Screenshot 2024-12-13 112146](https://github.com/user-attachments/assets/236ac29e-f2f5-489a-94bd-9d9278fcdb51)
![Screenshot 2024-12-16 011103](https://github.com/user-attachments/assets/058930d2-be63-4dde-b5d1-4513536960f1)




# RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
