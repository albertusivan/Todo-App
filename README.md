# To-DoList-App
1. What project have you worked about?

The project that Ive working on is completing a program regarding the ToDo application on Android, this application show you a list of todos stored in the in the locale databese. user can add or remove todos, user also can checked the todo that have been done. This application will also send notifications regarding todos that have not been done and the deadline is near. For the architecture itself, this application uses sqlite, room with three main components including entity, DAO (Data Access Object) , and database. There is also view model to store and manage UI-related data, PendingIntent for noification, and espresso for ui testing.

2. Which part is hardest?

The hardest part from the project that Ive working on, is in the ui testing section. I'm very confused, when the first time I run the test on my mobile phone, the test runs smoothly. But when I tried it again the test ran into problems. Then I tried using the Android emulator and the test ran smoothly even though I had run it many times

3. What components have been used to show a list of tasks?

Components that ive been used to show a list of tasks are recycler view with linear layout manager. The recyler view contains task item where data is retrieved based on the local database using an adapter. The item wil show you the cehck box, the task title and the deadline of the task itself.

4. How does notification reminder work?

the notification will work if the user activates the notification in the settings section of the todo application. this notification is build by using NotificationWorker. with the NotificationWorker i can schedule notifications to be shown at a specific time or after a certain amount of time has passed.in this application the notification will appear at intervals of 1 day. how does it work?, when the notification preference is on, notification worker will call getNearestActivity function from the repository. Then a notification will be displayed using a pending intent with content containing the task obtained from the previous process.

5. Why do we need a Custom View?

first of all we have to know what is a custom view in general. Custom view is a feature of Android that allows developers to create a unique view according to the needs of the application. In this project, a custom view is required when displaying the task list. If the task has been completed, the title of the task will be crossed out, or if the task has not been completed and has passed the deadline, the title of the task will turn red. This custom view conditional will be called when the adapter loads the data.

