# Test Case - Maximum Radio Load Exceeding 70%

## Summary
Verify that when the maximum radio load reaches 70%, new clients are not allowed to connect.

## Steps:
1. Navigate to the Venues page by clicking on the \"Venues\" link in the navigation bar.
2. Select the desired venue name and click on the \"Edit\" option. Alternatively, click on the venue name and then select \"Configure\".
3. On the Wi-Fi Configuration tab, make sure the Radio tab is displayed.
4. In the Radio tab, select the \"Client Admission Control\" sub-tab.
5. Set the maximum radio load to 70%.
6. Save the settings.
7. Simulate a scenario where the radio load exceeds the maximum limit.
8. Attempt to connect a new client to the network.
9. Verify that the new client is not allowed to connect.

## Expected Results:
- The new client should not be able to connect when the maximum radio load exceeds 70%.
- An appropriate error message or indication should be displayed, indicating that the maximum radio load has been reached and new connections are not allowed.