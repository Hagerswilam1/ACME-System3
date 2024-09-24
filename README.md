<h1>ACME System3 Desktop Application Automation Library</h1>
<p>This UiPath library automates operations within the ACME System3 desktop application. It can launch the desktop application, log in to an ACME account, search by client ID, extract client details and account movements, and navigate through the application’s windows. This library is a reusable solution for automating tasks related to the ACME System3 desktop environment.</p>

<h2>Features</h2>
<ul>
    <li>Launches the ACME System3 desktop application</li>
    <li>Logs in to an ACME account</li>
    <li>Navigates to the "Search by ID" feature</li>
    <li>Searches for a client by ID</li>
    <li>Opens the client details window</li>
    <li>Opens the client accounts window</li>
    <li>Navigates to and displays all account movements</li>
    <li>Extracts all account movements for a given client</li>
    <li>Closes all open windows and returns to the "Search by ID" screen</li>
</ul>

<details>

<summary><h5>ACME_System3_Launch</h5></summary>
#### Description: 
Opening the ACME System 3 Desktop Application
<br/>
#### PreCondition: 
ACME System3 Path Exists 
<br/>
#### PostCondition:  
WelcomePage Exist
</details>

<details>

<summary><h5>ACME_System3_LogIn</h5></summary>
#### Description: 
Login to the ACME System 3 Desktop Application
<br/>
#### PreCondition: 
System Credentials  Exists
<br/>
#### PostCondition:  
Welcome Page Exist
</details>

<details>

<summary><h5>ACME_System3_Clients_Search</h5></summary>
#### Description: 
Access the Clients -> Search for Client by Client ID menu option in ACME System 3 .
<br/>
#### PreCondition: 
Welcome Page Exist
<br/>
#### PostCondition:  
Search For Client By ID Exists
</details>

<details>

<summary><h5>ACME_System3_Search_Form</h5></summary>
#### Description: 
Access the Clients -> Search for Client by Client ID menu option in ACME System 3, Enter Client based on the ID and double click the Client Name. Also check “Include Inactive Clients” as sometimes even active clients will not be found otherwise.
<br/>
#### PreCondition: 
Search For Client By ID Exists
<br/>
#### PostCondition:  
 Client Details Exists
</details>

<details>

<summary><h5>ACME_System3_Open_Client_Accounts</h5></summary>
#### Description: 
Open the Client Deatails for the selected client
<br/>
#### PreCondition: 
Client Details Exists.
<br/>
#### PostCondition:  
Client Account Page Exists.
</details>

<details>
    
<summary><h5>ACME_System3_Open_Client_Movement</h5></summary>
#### Description: 
Access the Clients -> Search for Client by Client ID menu option in ACME System 3, Enter Client based on the ID and double click the Client Name. Also check “Include Inactive Clients” as sometimes even active clients will not be found otherwise.
<br/>
#### PreCondition: 
Search For Client By ID Exists
<br/>
#### PostCondition:  
Client Details Exists
</details>

<details>

<summary><h5>ACME_System3_Extract_All_Account_Movements</h5></summary>
#### Description: 
  Scraping all Account transactions Movements for the specified account
<br/>
#### PreCondition: 
Account Movements page Exists
<br/>
#### PostCondition:  
Account values Exists
</details>

<details>

<summary><h5>ACME_System3_Back_To</h5></summary>
#### Description: 
Close Stacked Window in ACME System 3 Desktop Application
<br/>
#### PreCondition: 
Search for Client by ID Page Exists.
<br/>
#### PostCondition:  
Search for Client by ID Page Exists.
</details>

<h2>Prerequisites</h2>
<ul>
    <li>UiPath Studio (latest version)</li>
    <li>Download ACME System3 desktop application</li>
    <li>UiPath Desktop Automation packages</li>
    <li>Valid ACME System account credentials</li>
</ul>

<h2>Installation</h2>
<ol>
    <li>Download or clone this Library.</li>
    <li>Open UiPath Studio and load the library into your project.</li>
</ol>

<h2>Usage</h2>
<ol>
    <li>Import the Library: After downloading, import the library into your UiPath project.</li>
    <li>Setup Credentials: Ensure that your ACME System3 login credentials are stored securely, either using UiPath Orchestrator Assets or Windows Credential Manager.</li>
    <li>Use Activities: Below is the sequence of activities for automating the ACME System3 desktop application:</li>
    <ul>
        <li>Launch Application: Opens the ACME System desktop application.</li>
        <li>Login: Automates the login process using stored credentials.</li>
        <li>Search by ID: Navigates to the "Search by ID" screen and inputs the client ID.</li>
        <li>Open Client Details: Opens the client details window for the specified ID.</li>
        <li>Open Client Accounts: Navigates to the client accounts window.</li>
        <li>Show All Account Movements: Displays all account movements for the selected account.</li>
        <li>Extract Account Movements: Extracts all visible account movements.</li>
        <li>Close Windows: Closes all open windows and navigates back to the "Search by ID" screen.</li>
    </ul>
</ol>

<h2>Example Workflow</h2>
<ol>
    <li>Launch and Login: The automation starts by launching the ACME System3 application and logging in using stored credentials.</li>
    <li>Search and Navigate: After login, the automation navigates to the "Search by ID" screen and enters a client ID to search for.</li>
    <li>Client Details and Accounts: It opens the client details and client accounts windows to gather the relevant data.</li>
    <li>Extract Account Movements: The automation opens the account movements window, displays all movements, and extracts them for further processing.</li>
    <li>Cleanup: After extraction, it closes all open windows, returning to the "Search by ID" window, and the session is completed.</li>
</ol>

<h2>Customization</h2>
<ul>
    <li>Client ID Input: The client ID to be searched can be dynamically passed as an argument in the workflow.</li>
    <li>Error Handling: The library includes error handling mechanisms to retry in case of application crashes or unexpected UI changes.</li>
    <li>Window Handling: Custom logic for handling specific windows can be added based on UI changes in the ACME System3 application.</li>
</ul>

<h2>Error Handling</h2>
<p>If the ACME System3 application fails to launch, the process will retry a set number of times before exiting.</p>
<p>Proper exception handling is built into the workflow to ensure smooth navigation and data extraction.</p>


