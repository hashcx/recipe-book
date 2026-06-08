## Requirements

### A Google spreadsheet with a sheet named "Sheet1" that has data starting at row 2 with following columns:

- A -> Date (date the recipe was recorded to the sheet)
- B -> Recipe Name
- C -> Source URL (the recipe source)
- D -> Ingredients + Steps (each cell starts with the [INGREDIENTS] tag followed by one ingredient per line followed by [STEPS] tage followed by one step per line)
- E -> Tags (seperated by commas)
- F -> Image URL (to use as a cover for the recipe)


### Allow the app to access the Google Spreadsheet as follows:

1. Go to https://console.cloud.google.com/
2. Create new project and select it
3. Open left menu -> select "API & Services" -> select "Enable API & Services" -> Click "+ Enable APIs and servies" -> search for "Google Sheets API" or just "sheets" -> select the shown result -> click "Enable"
4. From the shown screen -> from the left menu, click "Credentials" -> click "Create credentials" -> click "OAuth client ID" -> click "Eonfigure consent screen" -> click "Get started" -> in the "App Information" section, for the "App name", enter "Recipe Book" and for the "User support email", select from the dropdown meuu -> click 
Next" for the "Audience" section to show -> select "External" -> click "Next" for the "Contact Infomration" to show -> enter "Email addresses" -> click "Next" for the "Finish" section to show -> agree to the user policy -> click "Continue" -> click "Create" -> click "Create OAuth client ID" -> from the Application type, select "Web application" -> enter name for the web client, eg, "GitHub Webapp" -> under thee "Authorized JavaScript origions, enter "URIs" from which the request will come, which are the localhost (http://localhost) and where the web app will be hosted (https://hashcx.github.io in my case) -> copy the "Client ID" and replace the one in the index.html file (the "Client secret" is now needed) -> click "OK"
5. From the left menu, select "Audience" -> uner the "Test users" section, click "Add users" -> enter the email address that has full access to the sheet containing the recipes
