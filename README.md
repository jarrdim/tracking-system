# tracking-system
PROGRESS


To forward a document from a student to a supervisor, administrator, and dean of faculty in PHP, you can follow these steps:

Define the database structure:

        Create a table, such as "documents," with columns to store
        relevant information about the document,
        such as ID, title, content, status, sender ID (student), supervisor ID, 
        administrator ID, dean ID, etc.

Fetch the document from the database:

        Retrieve the document from the database based on its ID or any other identifier.

Perform validation:

        Validate if the document exists and if the student has the authority to 
        forward the document to the supervisor.

Update the document's status and receiver:

        1. If the student wants to forward the document to the supervisor,
            update the status to "Pending" and assign the supervisor ID to the document.
            
        2. If the supervisor approves the document, update the status to "Approved" 
            and assign the administrator ID to the document.
            
        3. If the supervisor rejects the document, update the status to "Rejected" 
            and assign the student ID back to the document.
            
        4. If the administrator approves the document,
            update the status to "Approved" and assign the dean ID to the document.
            
        5. If the administrator rejects the document,
            update the status to "Rejected" and assign the student ID back to the document.
            
        6. If the dean approves the document,
            update the status to "Approved" and mark it as the final approval.

Save changes to the database:

        Update the corresponding record in the "documents"
        table with the new status and receiver ID.

Send notifications:

        Notify the respective receivers (supervisor, administrator, dean) via email
