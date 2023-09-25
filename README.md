Step 1: Modify a Category Dropdown Component:

- Inside the CategoryDropdown component,
create a state variable to hold the value
of the new category input field.
- Implement a function to handle changes in
the input field. This function should update
the state variable as the user types in a
new category name.
- Create a function to handle the creation of
a new category. This function should be
triggered when the user clicks a "Create"
button next to the input field.
- Ensure that the function checks if the input
is not empty (i.e., a valid category name)
before creating a new category.
- Create a container div with the class
'dropdown-link create-category'.
- Inside the container div, create an input field:
Type text; Placeholder: 'Create New Category';
Value bound to newCategory; onChange event:
handleNewCategoryChange; Add class 'category-input'.
- Conditionally render a "Create" button:
Displayed only when newCategory.trim()
is not empty; onClick event: handleCreateCategory;
Class: 'category-button'.

Step 2: In your main App.js component:

- Define a function called createCategory that
takes a single argument, newCategory.
- Inside the createCategory function, use an if
statement to check if the newCategory does not
already exist in the categories array.  
- If the condition is met (i.e., newCategory is
not in categories), update the categories state
using the setCategories function.
- To update the categories state, use a
functional approach.
- In the <CategoryDropdown> component in your JSX,
make sure to pass the required props.
- Pass the updated categories array to the HabitForm
component as a prop.

Step 3: Modify the HabitForm Component

- In the HabitForm component, make sure you have
the categories prop passed to it. 
- Inside the <select> element in your form,
you should have a loop that maps through the
categories prop and generates <option> elements
for each category.
- Open your App.js component where you manage the
categories state. Remove the default categories
from the initial state of categories. Initialize
the categories state with an empty array [].
- In your HabitForm.js component, right above the
mapping loop for the categories, manually add
the default categories to the categories array
(e.g., "Read", "Drink Water", "Do Exercise").
- Make sure you add them as separate <option>
elements in the loop.
