1. What is the difference between a StatelessWidget and a StatefulWidget? Give one example of each from this lab.
- A StatelessWidget is constant and never changes once it is displayed while a StatefulWidget can change while the app is running. An example for a StatelessWidget is from the activity 1 where the ProfileCard never changes while an example for a StatefulWidget is from the activity 2 where every click from the user changes what is displayed in the WaterTrackerPage.

2. Why is a StatefulWidget written as two classes? What does each class do?
- A StatefulWidget uses two classes to separate the widget’s configuration from its changing data. The StatefulWidget class defines the widget and creates it state object. The State class stores changing values and contains build() method that displays the interface. It uses setState() tells Flutter when the interface needs updating.

3. In Activity 2, what happened when you changed _glasses outside setState()? Why? 4. Looking at the Debug Console in Activity 2, when is build() called?
- When I tap +, I notice that the displayed number still increases, and it can go beyond the goal of 6. This happens because _glasses++ is outside the setState() function, but setState() is still being called, which tells Flutter to rebuild the widget. Since the increment is also outside the condition that checks the goal, the number can continue increasing even after reaching 6.

5. Explain the main axis and the cross axis of a Row and of a Column.
- In a Row, the main axis is horizontal, and the cross axis is vertical. In a Column, the main axis is vertical, and the cross axis is horizontal.

6. In Activity 3, what happened when you removed Expanded from a StatBox? What does Expanded do?
- When I removed Expanded from a StatBox, the layout could have problems fitting the available space and might overflow. Expanded helps the widget use the available space properly.

7. Why do we use GridView.builder for the menu instead of a Column with many children? 
- We use GridView.builder because it displays the menu items in a grid and allows the user to scroll through them. It also builds items when needed, while a Column does not scroll by itself.

8. How do Stack and Positioned create the Best seller badge in Activity 4?
- Stack allows the widgets to overlap, while Positioned places the Best seller badge in a specific location on the menu card. This makes the badge appear on top of the menu item.

9. What is the difference between customizing with ThemeData and with a style on one widget? Give  one example of each from Activity 5.
- ThemeData changes the appearance of the whole app, while styling one widget changes only that specific widget. For example, ThemeData can change the style of buttons throughout the app, while a style applied directly to one button changes only that button.

10. When you flip the dark-mode switch in Activity 5, which widget holds the state, and how does the  change reach MaterialApp?
- The _ThemeDemoAppState class holds the dark-mode state using _isDark. When I switch dark mode on or off, the setState() function updates the value, causing the app to rebuild. Then, MaterialApp uses the updated value to switch between light mode and dark mode.