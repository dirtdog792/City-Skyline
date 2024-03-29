Step 1
Welcome to the CSS Variables Skyline project! Start by adding the !DOCTYPE html declaration at the top of the document so the browser knows what type of document it's reading.
Step 2
Add opening and closing html tags below the DOCTYPE so you have a place to start putting some code. Be sure to set the language to English.
Step 3
Next, add opening and closing head and body tags within the html element.
Step 4
Within the head, nest a meta element with a charset of UTF-8, a title element with a title of City Skyline, and a link element that links your styles.css file.
Step 5
In CSS, you can target everything with an asterisk. Add a border to everything by using the * selector, and giving it a border of 1px solid black. This is a trick that helps visualize where elements are and their size. You will remove this later.
Step 6
Also add a box-sizing of border-box to everything. This will make it so the border you added doesn't add any size to your elements.
Step 7
You can see the body (it's the inner-most box on your page); the box around it is the html element. Make your body fill the whole viewport by giving it a height of 100vh. Remove the default margin from the body by setting the margin to 0. Finally, set the overflow property to hidden to hide any scroll bars that appear when something extends past the viewport.
Step 8
Create a div element in the body with a class of background-buildings. This will be a container for a group of buildings.
Give your .background-buildings element a width and height of 100% to make it the full width and height of its parent, the body.
Step 9Passed
Give your .background-buildings element a width and height of 100% to make it the full width and height of its parent, the body.
Step 10
Nest a div with a class of bb1 in the background buildings container. Open your styles.css file, and give .bb1 a width of 10% and height of 70%. "bb" stands for "background building", this will be your first building.
Step 11
Nest four div elements in the .bb1 container. Give them the classes bb1a, bb1b, bb1c, and bb1d in that order. This building will have four sections.
Step 12
Give the parts of your building width and height properties with these values: 70% and 10% to .bb1a, 80% and 10% to .bb1b, 90% and 10% to .bb1c, and 100% and 70% to .bb1d. Remember that these percentages are relative to the parent and note that the heights will add up to 100% - vertically filling the container.
Step 13
Center the parts of your building by turning the .bb1 element into a flexbox parent. Use the flex-direction and align-items properties to center the children.
Step 14
Now you have something that is resembling a building. You are ready to create your first variable. Variable declarations begin with two dashes (-) and are given a name and a value like this: --variable-name: value;. In the rule for the bb1 class, create a variable named --building-color1 and give it a value of #999.
Step 15
To use a variable, put the variable name in parentheses with var in front of them like this: var(--variable-name). Whatever value you gave the variable will be applied to whatever property you use it on.

Add the variable --building-color1 you created in the previous step as the value of the background-color property of the .bb1a class.
Step 16
Use the same variable as the background-color of the .bb1b, .bb1c, and .bb1d classes to fill in the rest of the building.
Step 17
Change the value of your variable from #999 to #aa80ff and you can see how it gets applied everywhere you used the variable. This is the main advantage of using variables, being able to quickly change many values in your stylesheet by just changing the value of a variable.
Step 18
Your first building looks pretty good now. Nest three new div elements in the .background-buildings container and give them the classes of bb2, bb3, and bb4 in that order. These will be three more buildings for the background.
Step 19
Give the new buildings width and height properties of: 10% and 50% for .bb2, 10% and 55% for .bb3, and 11% and 58% for .bb4. You will be using almost all percent based units and some flexbox for this project, so everything will be completely responsive.
Step 20
The buildings are currently stacked on top of each other. Align the buildings by turning the .background-buildings element into a flexbox parent. Use the align-items and justify-content properties to evenly space the buildings across the bottom of the element.
Step 21
The buildings are too spaced out. Squeeze them together by adding two empty div elements to the top of the .background-buildings element, two more at the bottom of it, and one more in between .bb3 and .bb4. These will be added as evenly-spaced elements across the container, effectively moving the buildings closer to the center.
Step 22
Create a new variable below your --building-color1 variable. Name your new variable --building-color2 and give it a value of #66cc99. Then set it as the background-color of .bb2.
Step 23
That didn't work. You should add a fallback value to a variable by putting it as the second value of where you use the variable like this: var(--variable-name, fallback-value). The property will use the fallback value when there's a problem with the variable. Add a fallback value of green to the background-color of .bb2.
Step 24
Create a new variable below the other ones named --building-color3 and give it a value of #cc6699. Then use it as the background-color of the .bb3 class and give it a fallback value of pink.
Step 25
That didn't work, because the variables you declared in .bb1 do not cascade to the .bb2 and .bb3 sibling elements. That's just how CSS works. Because of this, variables are often declared in the :root selector. This is the highest level selector in CSS; putting your variables there will make them usable everywhere. Add the :root selector to the top of your stylesheet, and move all your variable declarations there.
Step 26
Now that you've worked the bugs out and the buildings are the right colors, you can remove the fallback values in the two places they were used. Go ahead and do that now.
Step 27
Create another variable named --building-color4 and give it a value of #538cc6. Make sure it's in the :root selector this time. Then use it to fill in the last building.
Step 28
The background buildings are starting to look pretty good. Create a new div below the .background-buildings element and give it a class of foreground-buildings. This will be another container for more buildings.
Step 29
You want the .foreground-buildings container to sit directly on top of the .background-buildings element. Give it a width and height of 100%, set the position to absolute, and the top to 0. This will make it the same size as the body and move the start of it to the top left corner.
Step 30
Nest six div elements within .foreground-buildings and give them the classes of fb1 through fb6 in that order. "fb" stands for "foreground building". These will be six more buildings for the foreground.
Step 31
Give the six new elements these width and height values: 10% and 60% to .fb1, 10% and 40% to .fb2, 10% and 35% to .fb3, 8% and 45% to .fb4, 10% and 33% to .fb5, and 9% and 38% to .fb6.
Step 32
Add the same display, align-items, and justify-content properties and values to .foreground-buildings that you used on .background-buildings. Again, this will use Flexbox to evenly space the buildings across the bottom of their container.
Step 33
You should optimize your code. Move the position and top properties and values from .foreground-buildings to .background-buildings. Then select both .background-buildings and .foreground-buildings there, effectively applying those styles to both of the elements. You can use a comma (,) to separate selectors like this: selector1, selector2.
Step 34
Now that you did that, you can delete the old .foreground-buildings declaration and all of its properties since they aren't needed anymore.
Step 35
The skyline is coming together. Fill in the background-color property of the foreground buildings. Use your --building-color1 variable to fill in .fb3 and .fb4, --building-color2 for .fb5, --building-color3 for .fb2 and .fb6, and --building-color4 for .fb1.
Step 36
Squeeze the buildings together again by adding two empty div elements within both the top and bottom of the .foreground-buildings element, and one more in between .fb2 and .fb3.
Step 37
Move the position of .fb4 relative to where it is now by adding a position of relative and left of 10% to it. Do the same for .fb5 but use right instead of left. This will cover up the remaining white space in between the buildings.
Step 38
Your code is starting to get quite long. Add a comment above the .fb1 class that says FOREGROUND BUILDINGS - "fb" stands for "foreground building" to help people understand your code. Above the .bb1 class add another comment that says BACKGROUND BUILDINGS - "bb" stands for "background building". If you don't remember, comments in CSS look like this: /* Comment here */.
