# Registration and Login dummy app

You will create a dummy app where the user can "register" and "login". But not for real yet, you will just save everything in a database :). The app will have the following screens:

1. **Login screen** which has the following elements:

  * `Username` and `Password` fileds and a `Login` button. Use EditTexts with TextInputLayouts for the fields. You should do some initial validation and show errors if the name length is less than 4 characters and password length - less than 6 and more (>=) than 128 chars for both. When the user clicks the `Login` button you should check if such user exist in the database. If yes - continue to "Users list" screen. Else show a error dialog that the user doesn't exist.

  * `Register` button which opens the Registration screen

2. **Registration screen** with the following elements:

  * `Username` field with the following validation - length >= 4 symbols and < 128 chars, only alphanumeric characters. Both upper and lowercase letters are acceptable and should be treated as different characters. Show the respective error using the TextInputLayout - e.g. when username is less than 4 symbols show "Username less should be more than 4 symbols" and so on.

  * `Password` field with the following validation - length >= 6 symbols and < 128 chars, alphanumeric and the following special chars are accepted: `` !"#$%&'()*+,-./:;<=>?@[\]^_`{|}~``. Password is of course not shown (EditText has a way of hiding it).

  * `Verify Password` field where the user enters again the chosen password. Same validation as above but also checks if the two passwords match.

  * `Email` field - validates only valid emails of the form `[something]@[something-else].[domain]`.

  * `First name` field - only letter, should start with a capital one

  * `Last name` field - only letters and spaces

  * `Age` field - number between 12 and 112.

  * `Register` button - when tapped all the information is checked if valid and if yes it's written in the [database](https://developer.android.com/training/data-storage/room/index.html). Then the user is returned to the Login screen.

3. **Users list** screen - once the user is logged in he/she can see the information of the other users that have registered (which should never happen in a real app :D). You should display a RecyclerView with rows showing username, email, first name, last name and age.
You should be able to search by any field [TODO - should have a ActionBar]