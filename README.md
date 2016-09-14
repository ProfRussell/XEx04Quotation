CSD 3354 Assignment 1

1) Open Visual Studio
2) Clone the starting files 
3) Repository URL: https://github.com/ProfRussell/XEx04Quotation.git
4) Work from There
5) Use the dropbox to submit you final zipped assignment
6) Use the naming convention assign01-c06XXXXX.zip


Enhance the the Quotation application

The application for this exercise is an enhanced version of the one for exercise 3-1. First, 
the Quotation has a confirm button to the right of the Calculate button. Second, the
Confirm button redirects to a Confirmation page.

_Open the web application for this exercise and start enhancing its pages
1. Open the web application named XEx04Quotation in your exercises_extra folder. It
includes the aspx and code-behind files for the pages shown above, but the first page
doesn’t have the code for the Confirm button and the second page doesn’t have the7 Extra exercises for Murach’s ASP.NET 4.6 with C# 2015
code for either of the buttons that are shown. And neither page has the code for the
label with the message that’s displayed below the buttons.

2. Add the Confirm button to the Quotation page right after the Calculate button, and set
its CssClass property to the btn and btn-primary classes.

3. Add the Send Quotation and Return buttons to the Confirmation page, and set the
appropriate CssClass values. Also, set the properties for the Return button so it goes
back to the Quotation page and doesn’t cause validation.

4. On each page, add a label control below the buttons. For each label, set the ID to
lblMessage, the CssClass to text-info, and the Text as shown above.

5. Test the application to see how it’s going, and make any adjustments.

_Add the C# code that makes the application work
6. Create a Click event handler for the Confirm button of the Quotation page. This
button should redirect to the Confirmation page, which will display the quotation that
is being confirmed by getting the data from session state.

7. To make this work, the Click event handler for the Calculate button of the Quotation
page should save the sales price, discount amount, and total price in session state.
Now, add that code to that event handler.

8. When the user clicks the Confirm button on the Quotation page to go to the
Confirmation page, the Load event handler for the Confirmation page should get the
data from session state and display it as shown above. Now, add that code to the
Load event handler.

9. Add an event handler for the Click event of the Send Quotation button. If the entries
for this form are valid, this handler should use the data entered by the user to display
a message below the buttons that says: “Quotation sent to <name> at <email>.” It
should also set the values in session state to null.

_Test and refine the operation of the application.
10. Code and test what you have so far. At this point, all four buttons should work,
although you may be able to find errors by trying different sequences of button
clicks. If, for example, the user clicks on the Confirm button on the Quotation page
before clicking on the Calculate button, the application may blow up because there
isn’t any data in session state.

11. To fix errors like that, add code to the Click event handler for the Confirm button on
the Quotation page that tests whether the value for the sales price in session state is
null. If it is, this message should be displayed in the label below the buttons: “Click
the Calculate button before you confirm.” If it isn’t, the handler should redirect to the
Confirmation page.

12. Do the same test in the Load event handler for the Confirmation page. If the sales
price in session state is null, don’t display the values on the page. If it isn’t, get the
values from session state and display them.

_Make any final adjustments
13. Take a final look at the application, and make any adjustments for improving the look
of the application, the operation of the application, or the clarity and logic of the
code.
