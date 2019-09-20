

# Javascript DOM Selectors

DOM Selectors, as the name suggests is used to  **select HTML elements within a document**  using JavaScript. There are  **5**  ways in which you can select elements in a DOM using selectors.

-   getElementsByTagName()
-   getElementsByClassName()
-   getElementById()
-   querySelector()
-   querySelectorAll()

All those methods are properties of the document object. So in order to use one, we should prefix those elements with the document object as,

document.getElementsByTagName()  
document.getElementsByClassName()  
document.getElementById()  
document.querySelector()  
document.querySelectorAll()

Before we begin with those selectors, let’s first look into a sample HTML document so that all those selection operations can be done using this page.

<!-- Sample HTML Page --><!DOCTYPE html>  
<html lang="en">  
<head>  
    <title>Document Object Model</title>  
</head>  
<body>  
    <h1 class="heading">DOM Selectors</h1>  
    <ul>  
        <li id="item">getElementsByTagName</li>  
        <li class="selectors">getElementsByClassName</li>  
        <li class="selectors">getElementById</li>  
        <li id="item">querySelector</li>  
        <li id="item">querySelectorAll</li>  
    </ul>  
</body>  
</html>

The above HTML document is self explanatory as it’s very simple. And I will be using the web console to explain things better. Let’s get started.

## getElementsByTagName

This method returns all the elements that matches the specified  **Tag name**.

![](https://miro.medium.com/max/30/1*vUQGVIw8CxXETdOFabQTbQ.png?q=20)

![](https://miro.medium.com/max/1920/1*vUQGVIw8CxXETdOFabQTbQ.png)

getElementsByTagName Example

-   `document.getElementsByTagName('h1')`  returns a collection of items matching the tag name  **h1**. And since we got only one  **h1**  element, the list contains only one elements.
-   Using [0] as index, we can access the first element in the list which is  `<h1 class="heading">DOM Selectors</h1>`.
-   `document.getElementsByTagName('li')`  returns a list of 5 elements as we have five  **li**  tags in our page.
-   And any individual element can be selected by using it’s index such as  `document.getElementsByTagName('li')[0]`.

## getElementsByClassName

This method returns all the elements that matches the specified  **Class name**.

![](https://miro.medium.com/max/30/1*-zDzmZH0yfbaUS1pOiosZA.png?q=20)

![](https://miro.medium.com/max/1920/1*-zDzmZH0yfbaUS1pOiosZA.png)

getElementsByClassName Example

-   This selector is very similar to  `getElementsByTagName`  except the s**election is based on Class name and not Tag name**. You can see some examples from the image above.

## getElementById

Here, the selection is based on the  **Id name**. And this seems to be similar to Tag name & Class name selector but there’s a difference in how many elements this selector selects. In all the above selectors, a list of all matching elements is returned. But this selector  **returns only the first matched element while ignoring the remaining**.

![](https://miro.medium.com/max/30/1*SUfNkkr1j8nzT7Ism8JXgw.png?q=20)

![](https://miro.medium.com/max/1920/1*SUfNkkr1j8nzT7Ism8JXgw.png)

### getElementById Example

-   As you can see, even though we got 3  **li**  elements with the Id  **item**, we got only the first  **li**  element with the Id  **item**. Remaining all elements are ignored.

> And this is where  `getElementById`  differs from  `getElementsByTagName`  and  `getElementsByClassName`.  `getElementById`  returns the element as soon as it gets a match. Also you can notice a difference in the name of the selector, the word  **element**  is singular in  `getElementById`  while it’s plural in other selectors  `getElementsByTagName`  &  `getElementsByClassName`.

## querySelector

This one returns the  **first element that matches the specified CSS selector**  in the document.

![](https://miro.medium.com/max/30/1*riXEAD5FpASIpSCarvg7Uw.png?q=20)

![](https://miro.medium.com/max/1920/1*riXEAD5FpASIpSCarvg7Uw.png)

querySelector Example

-   `document.querySelector('li')`  returns the first element that matches the CSS selector  `li`. Remaining elements are ignored.
-   `document.querySelector('.heading')`  returns the first element that matches the CSS selector  `.heading`.
-   `document.querySelector('#item')`  returns the first element that matches the CSS selector  `#heading`.
-   As you can see, we can use all kinds of CSS selectors within the  `querySelector`  method that we will use in a normal CSS file.

> Note that you have to use CSS selectors and not normal HTML selectors as a parameter.  `document.querySelector('.className')`  is valid while  `document.querySelector('className')`  is not valid. So you have to use the format used in CSS selectors.

## querySelectorAll

This method  **returns all the elements that match the specified**  **CSS selector**  in the document.

![](https://miro.medium.com/max/30/1*B8OykGlCIsAWh4_dEtNYbA.png?q=20)

![](https://miro.medium.com/max/1920/1*B8OykGlCIsAWh4_dEtNYbA.png)

querySelectorAll Example

-   `document.querySelectorAll('.heading')`  returns a list of all elements that matches the specified CSS selector. Since we have only one element under the class name  `.heading`, the list contains one element. And it can be accessed by it’s index.
-   Similarly,  `document.querySelectorAll('#item')`  returns a list of 3 items that matches the CSS selector. Individual elements are accessed by it’s index.

> Note that,  **no two elements should have the same Id**  as a way of good practice. And I used same Id for some elements to explain things better. So, you can follow the recommended way of not using the same Id for more than one element.



