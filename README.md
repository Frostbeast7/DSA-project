1. Class: Person
1.1 __init__(self, name, phone, email=&quot;&quot;)
Purpose:
Constructor that initializes the core attributes of a person: name, phone, and email.
DSA Relevance:
Simple assignment operations.
Time Complexity: O(1)

1.2 get_info(self)
Purpose:
Returns a formatted string containing all attributes of the Person object.
DSA Relevance:
String concatenation; no complex data structure operations.
Time Complexity: O(1)

1.3 display(self)
Purpose:
Prints the person’s data to the console.
DSA Relevance:
Constant-time output operation.
Time Complexity: O(1)

2. Class: Contact (Inherits from Person)
2.1 __init__(self, name, phone, email=&quot;&quot;, address=&quot;&quot;)

Purpose:
Extends Person by adding an address field.
DSA Relevance:
Constructor; initializes the object and calls parent constructor.
Time Complexity: O(1)

2.2 get_info(self)
Purpose:
Overrides the parent method to include address data.
DSA Relevance:
Method overriding; adds more fields in string return.
Time Complexity: O(1)

2.3 display(self)
Purpose:
Displays all contact attributes including address.
DSA Relevance:
Polymorphic display routine.
Time Complexity: O(1)

2.4 to_string(self)
Purpose:
Converts the contact into a comma-separated format for file saving.
DSA Relevance:
Supports serialization of data into strings for storage.
Time Complexity: O(1)

3. Class: BusinessContact (Inherits from
Contact)
3.1 __init__(self, name, phone, company, email=&quot;&quot;, address=&quot;&quot;)
Purpose:
Extends Contact by adding company information and setting contact_type = &quot;Business&quot;.
DSA Relevance:
Constructor; no complex operations.
Time Complexity: O(1)

3.2 get_info(self)
Purpose:
Overrides to include company and business type.
DSA Relevance:
Method overriding; layered string creation.
Time Complexity: O(1)

3.3 display(self)
Purpose:
Displays contact data including company name and type.
DSA Relevance:
Polymorphic behavior based on class type.
Time Complexity: O(1)

3.4 to_string(self)
Purpose:

Formats contact data with B| prefix for identification during file parsing.
DSA Relevance:
Supports efficient reconstruction of data structures when loading.
Time Complexity: O(1)

4. Class: FamilyContact (Inherits from
Contact)
4.1 __init__(self, name, phone, relationship, email=&quot;&quot;, address=&quot;&quot;)
Purpose:
Adds relationship field and sets contact_type = &quot;Family&quot;.
Time Complexity: O(1)

4.2 get_info(self)
Purpose:
Adds family relationship details to the base information.
Time Complexity: O(1)

4.3 display(self)
Purpose:
Displays all data including relationship.
Time Complexity: O(1)

4.4 to_string(self)
Purpose:

Prefixes with F| for structured file identification.
Time Complexity: O(1)

5. Class: ContactBook
This is the central class responsible for manipulating the contact list using core data structures
and algorithms.

5.1 __init__(self)
Purpose:
Initializes data structures:
 An empty list contacts
 Contact type mapping
 Loads existing contacts from file
Data Structure Used: Python List (Dynamic Array)
Time Complexity: O(n) due to file loading

5.2 create_contact(self, contact_type)
Purpose:
Creates a new contact object after:
 Input validation
 Checking for duplicate phone numbers (linear search)
Data Structure Operations:
 Search: O(n)
 Object creation: O(1)
Overall Complexity: O(n)

5.3 add_contact(self)
Purpose:
Adds a contact to the list and re-sorts the list.
Data Structure Operations:
 Append to list: O(1)
 Sorting the list: O(n log n) using Timsort
Overall Complexity: O(n log n)

5.4 view_contacts(self, filter_type=None)
Purpose:
Displays contacts, with optional filtering by type.
Data Structure Operations:
 Iteration over list: O(n)
 List comprehension for filtering: O(n)
Overall Complexity: O(n)

5.5 search_contact(self)
Purpose:
Searches contact by:
 Exact phone match
 Partial name match
Algorithm Used: Linear Search
Time Complexity: O(n)

5.6 update_contact(self)

Purpose:
1. Search contact in list (O(n))
2. Update values selectively (O(1))
3. Sort list again (O(n log n))
Overall Complexity: O(n log n)

5.7 delete_contact(self)
Purpose:
Removes a contact from the dynamic list.
Data Structure Operations:
 Search: O(n)
 Remove element from list: O(n)
Overall Complexity: O(n)

5.8 statistics(self)
Purpose:
Counts the number of contacts of each type.
Algorithm:
Linear scan + conditional checks
Time Complexity: O(n)

5.9 save_contacts(self)
Purpose:
Writes all contacts to file line-by-line.
Data Structure Operations:
Iterating through list: O(n)

5.10 load_contacts(self)
Purpose:
Parses file and reconstructs the data structure by creating objects.
Algorithm:
Sequential file parsing
Time Complexity: O(n)

5.11 run(self)
Purpose:
Main control loop.
Handles all user operations through menu-driven interaction.
Algorithmic Nature:
Loop + user-driven branching
Time Complexity:
Dependent on user actions.

6. Standalone Function
demonstrate_inheritance()
Purpose:
Demonstrates:
 Object creation
 Class hierarchy
 Polymorphic display() and get_info() methods
DSA Relevance:
Not algorithmic — used only for OOP demonstration.
