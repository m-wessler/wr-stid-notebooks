**Synoptic API Account and Token Creation and Usage**

_NWS WR STID Updated 4/23/2025_

_Contact:_ [_michael.wessler@noaa.gov_](mailto:michael.wessler@noaa.gov)

1. **Create your Synoptic API Account**  
    [**Sign up here:** https://customer.synopticdata.com/](https://customer.synopticdata.com/)  
    <br/>It is important that you sign up using your official @noaa.gov email address in order to have access to limited services from Synoptic Data.  
    <br/>The best way to ensure the account is linked is to select “_Continue with Google_” on the login screen and sign in with your @noaa.gov account. The first time, it will prompt you to create the account. In the future, sign in the same way.  
    <br/>It is possible to create an independent Synoptic API account without signing in via google, but be sure to use the correct email address.  

2. **Manage Data Credentials** Upon a successful login to Synoptic, navigate from the home page to the Data Credentials Page using the top nav bar:  
    <br/><br/><br/><br/>A **private key** should exist upon creating your account, but you can use “Create a Key” to do so if none exists. These keys are generally irrelevant for our own needs, but one needs to exist in order to create a **public token**, which is used to access the API**.  

3. **Applying the Public Token in Colab Code** All scripts that access the Synoptic API will require you enter your own Synoptic API token. These are primarily set up as a text entry box at the top of the google form in CoLab. _If not,_ it will be defined as a variable within the python code, and may be easily found using CTRL+F (Win) or CMD+F (Mac) within your browser window and searching the phrase ‘token’.  

Future iterations of Colab scripts will streamline the request for a Synoptic API token, prompting the user to enter their own public token when first running a script.  

4. **Troubleshooting**
    1. **_Synoptic API public token will not allow access_** If you receive an error message along the lines of:  
        <br/>"RESPONSE_MESSAGE":"Account associated with this token does not have access to the precipitation service. Please see our Enterprise Service options”  
        <br/>It is possible that your account is still too new and has not been automatically registered as an enterprise service account with Synoptic. This usually takes on the order of a few hours. If there are continued issues, email [account@synopticdata.com](mailto:account@synopticdata.com) and provide your @noaa.gov email, as well as your **public token** and they will be able to appropriately set up access.  

    2. **Data Query Too Large** It is possible that Synoptic API changes their data query limits, or a certain configuration of a colab script generates too large of a query (too long of a time period over too large of an area, e.g. one year of data over all of western region).  
        <br/>In this case, first attempt to downsize the query by choosing a shorter date range, or querying a single CWA rather than western region as a whole. If issues with query size continue, contact STID through Michael Wessler at [michael.wessler@noaa.gov](mailto:michael.wessler@noaa.gov)