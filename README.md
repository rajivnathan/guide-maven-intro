### Note: This branch is specifically for testing the fix for https://github.com/OpenLiberty/open-liberty-tools/issues/348

*PR: https://github.com/OpenLiberty/open-liberty-tools/pull/382*

## Projects to demonstrate the fix

Project | liberty-maven-plugin version | mvn goal used by tools 
--- | --- | ---
archetypeGen/ServletSample | 2.0 | liberty:install-apps
finish | 3.2 | liberty:deploy

## Instructions to test
1. Import the project as an existing maven project
2. Use Run As -> Maven Install to trigger the full build
3. Once the build completes you may be prompted to have a server automatically created for you. Select Yes.
4. You should see a Liberty server created in the `Servers` view. Start it and verify the app is working correctly.
5. Make a change to the `HelloServlet.java` file.
6. Once you save the file it should trigger a republish of the app that makes use of the appropriate liberty maven goal according to the table above.
7. Verify the update worked
