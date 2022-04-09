## Anantomy of App Upgrade.
Let's see how the App Upgrade workflow works.

### Project
Project is a high level term used in App Upgrade. Project is a umbrella which you will be using to manage the versions for you app.
Use project for easy management. Let's say you are working on a project which has 3 apps. Go ahead and create a project and manage all the 3 apps under it.

![Project]("https://github.com/appupgrade-dev/docs/blob/main/images/project.svg")

### Creating a project
Assuming once you have done signing up and you are logged in to the app. You will be welcomed with the following screen.

![Create Project-Empty Screen]("https://github.com/appupgrade-dev/docs/blob/main/images/create_project_empty_screen.png")

Click on the `+New Project` button to create a new project. Provide a proper `Name` and `Description` for your project.

![Create Project-Form Screen]("https://github.com/appupgrade-dev/docs/blob/main/images/create_project_form_screen.png")

Click on `Submit` button and project will be created.

![Create Project-Project Screen]("https://github.com/appupgrade-dev/docs/blob/main/images/create_project_form_screen.png")

### Version
Version are the record you create to make an app marked for the upgrade. Let's say in your project you have an app `Wallpaper App`. You have lauched a new and improved version `1.0.1` with the some fixes, and now the old app `1.0.0` is now longer working because you have breaking API changes. If you had already integrated the App Upgrade solution in `1.0.0` now you can click on the project and you will be seeing an empty version page.

![Create Version-Empty Screen]("https://github.com/appupgrade-dev/docs/blob/main/images/create_version_empty_screen.png")

Click on the `+New Version` button to create a new app version marked for the upgrade. Provide the following details.
- App Name: Name of the App
- App Version: Version of the app you want to mark for update. For example: 1.0.0
- Platform: App platform example: android or iOS
- Environment: Environment in which app is running example: development, staging or production
- Message: An optional message which you want to show to the user, when user will be alerted for the force update.
- Force upgrade: Boolean flag if selected it means this is going to be force upgrade. If not selected indicates its not a force upgrade.

![Create Version-Form Screen]("https://github.com/appupgrade-dev/docs/blob/main/images/create_version_form_screen.png")

After providing the value click on `Submit` button and version will be created.

![Create Version-Version Screen]("https://github.com/appupgrade-dev/docs/blob/main/images/create_version_form_screen.png")
