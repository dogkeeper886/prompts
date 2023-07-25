# Test Case - Limitation of Client Admission Control with Enabled Load Balancing

## Summary:
Verify the limitation of client admission control when client load balancing/band balancing is enabled.

## Steps:
1. Navigate to the Venues page from the navigation bar.
2. Select a Venue Name and click Edit, or alternatively, click Venue Name > Configure and select the Wi-Fi Configuration tab. Ensure that the Radio tab is displayed.
3. In the Radio tab, check if the Client Admission Control sub-tab is displayed. 
   - If the Client Admission Control sub-tab is not displayed, proceed to step 5.
   - If the Client Admission Control sub-tab is displayed, go to step 4.
4. Configure client load balancing/band balancing settings:
   a. Enable client load balancing/band balancing.
   b. Save the settings.
5. Refresh the page or navigate back to the Venues page and select the same Venue Name.
6. Repeat steps 2 and 3 to ensure that the Client Admission Control sub-tab is still not displayed.
   - If the Client Admission Control sub-tab is not displayed, proceed to step 8.
   - If the Client Admission Control sub-tab is displayed, go to step 7.
7. Attempt to enable client admission control:
   a. Configure the required settings for the 2.4 GHz and 5 GHz bands in the Client Admission Control sub-tab.
   b. Click on the Save button.
   c. Verify that a warning message is displayed indicating that client load balancing/band balancing needs to be disabled before enabling client admission control.
8. Disable client load balancing/band balancing:
   a. Edit the client load balancing/band balancing settings.
   b. Disable client load balancing/band balancing.
   c. Save the settings.
9. Repeat steps 5 to 7 to attempt enabling client admission control again.
   - If the warning message is not displayed this time, proceed to step 10.
   - If the warning message is still displayed, the test case has failed.
10. Configure the required settings for the 2.4 GHz and 5 GHz bands in the Client Admission Control sub-tab.
11. Click on the Save button.
12. Verify that the settings are saved without any warning messages.

## Expected Results:
- Step 3: The Client Admission Control sub-tab should not be displayed.
- Step 7c: A warning message should be displayed, indicating that client load balancing/band balancing needs to be disabled before enabling client admission control.
- Step 9: The warning message should not be displayed.
- Step 12: The settings should be saved without any warning messages.
