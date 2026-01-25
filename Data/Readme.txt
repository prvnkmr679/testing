My Approach and observations:


1. I am not using UI Element ACtivties to complete the project as this is like dynamic sheets and workflows that needs to created in the Smartsheet Application. I need to use Computer vision in case if i need to go with UI automation since selectors are not stable.

2. I explored API option where API requires Enterprise plan and cost involved.

3. I Found official smartsheet library in UiPath but that was older version and cant use in latest version.

4. so i used integration services in UiPath, where activities in integration service may take sometime to understand the variable type for using in my development, so i used API request activity which is available in Integration service. I got API endpoint with document from this link "https://developers.smartsheet.com/api/smartsheet/openapi/rows/rows-addtosheet"

5. I build using Reframe work and Queue item, and added dispatcher workflow in Init state. finally creating reporting part and send mail activity in end process in RE framework. Handled API call errors using throw activity in if condition for any failures and RE framework will handle it by default(i did not create specific Business error for now, which can be modified).

6. I am using Gmail since i dont have outlook personal account.

P.S: I even had a thought of creating form from smarsheet connected with sheet(Grid) but since you have requested to create sheet, i felt API would be better option for creating and neglected using Form to add rows.