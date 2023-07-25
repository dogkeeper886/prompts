# Test Case - Validation of Client Admission Control Input Fields

## Summary
Validate the input fields for Client Admission Control settings.

## Steps
1. Access the application and log in.
2. On the navigation bar, click on "Venues".
3. Verify that the Venues page is displayed.
4. Select the desired venue, and click on "Edit" or "Configure" for the Venue Name.
5. The Wi-Fi Configuration tab should be displayed.
6. Select the "Radio" tab, if not already selected.
7. Verify that the "Client Admission Control" sub-tab is displayed.
8. In the "Client Admission Control" sub-tab, locate the input field for the "Minimum client count".
9. Enter a valid number within the range of 0 to 100 (inclusive).
10. Verify that the input is accepted without any error message.
11. Repeat steps 8-10 for the "Maximum radio load (%)" input field.
12. Enter a valid number within the range of 50 to 100 (inclusive).
13. Verify that the input is accepted without any error message.
14. Repeat steps 8-10 for the "Minimum client throughput (Mbps)" input field.
15. Enter a valid number within the range of 0 to 100 (inclusive).
16. Verify that the input is accepted without any error message.
17. Click on "Save".
18. Verify that the settings are saved successfully and no error message is displayed.

## Expected Results
- The Venues page is displayed.
- The Wi-Fi Configuration tab is displayed.
- The "Client Admission Control" sub-tab is displayed.
- The input for the "Minimum client count" accepts valid numbers within the range of 0 to 100.
- The input for the "Maximum radio load (%)" accepts valid numbers within the range of 50 to 100.
- The input for the "Minimum client throughput (Mbps)" accepts valid numbers within the range of 0 to 100.
- Clicking on "Save" saves the settings without any errors.