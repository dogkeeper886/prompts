---
Test Case - Maximum Radio Load Exceeding 70%
---
## Summary
Verify that new clients are not able to connect when the Maximum radio load exceeds 70%.

## Steps:
1. Navigate to the Venues page on the navigation bar.
2. Select the desired Venue Name and click Edit or click on Venue Name followed by Configure.
3. Select the Wi-Fi Configuration tab.
4. On the Radio tab, select the Client Admission Control sub-tab.
5. Verify that the Client Admission Control sub-tab is correctly displayed.
6. Set the Maximum radio load to 70%.
7. Simulate a scenario where the radio load exceeds 70% by connecting multiple clients to the network.
8. Verify that the network is able to handle the load below 70% and all clients are able to connect successfully.
9. Add additional clients to the network to exceed the 70% maximum radio load.
10. Verify that new clients are not able to connect, and instead receive an error or are unable to establish a connection.
11. Confirm that the system does not allow new clients to connect until the radio load decreases below 70%.
12. Adjust the radio load below 70% by disconnecting some clients.
13. Verify that the network allows new clients to connect after the radio load is below 70%.
14. Save the settings.

## Expected Result:
- Clients can connect successfully when the radio load is below 70%, and new clients are not allowed to connect when the radio load exceeds 70%.
