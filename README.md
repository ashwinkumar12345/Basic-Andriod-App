# Building an Andriod Application

After you have a basic understanding of Andriod Studio and have it installed and running on your computer, you can use it to build UI elements, connect it to backend code, and test your app on it's emulator. 
This Andriod app takes input text from the user and outputs the same text onto the screen.

> ## Contents

**[Building UI in XML files](#UI)**<br>
**[Connecting UI to backend code with variables and methods](#Connect)**<br>
**[Implementing backend functionality](#Implement)**<br>
**[Testing on an emulator](#Testing)**<br>

<a name="UI"></a>
> ## Building UI in XML Files

You can build the UI using XML text:

1. Open the `activity_main.xml` file.
2. The `TextView` element is setup by default. 
3. Copy the `EditText`, `Button`, and `TextView` elements from the `activity_main.xml` file.
4. Copy the string and color resources from the `strings` and `color` files, respectively.

<a name="Connect"></a>
> ## Connecting UI to backend code with variables and methods

You need to gain access to the `EditText` and `TextView` elements from the UI.

1. Open the `MainActivity.java` file.
2. Declare the UI elements variables:

```
EditText editText;
TextView textView;
```
The import statements are automatically added.

2. Initialize these variables in the `OnCreate` method:

```
editText = findViewById(R.id.edit_text);
textView = findViewById(R.id.text_view);
```

You can now use these elements as variables.

3. Create the method framework for defining the button functionality:

```
public void displayResults(View view) {
	//TODO: Implement the functionality
    }
```
 
 <a name="Implement"></a>
> ## Implementing backend functionality

The backend functionality code is as follows:

```
public void displayResults(View view) {
        String inputText = editText.getText().toString(); //Any text entered in the EditText element is stored in inputText
        if (inputText.equals("")){
            return; //If no text is entered break out of the function
        }
        textView.setText(inputText); //Set the TextView element to the input text 
    }
```

<a name="Testing"></a>
> ## Testing on an emulator

Load up an emulator using the AVD manager and run the program:

<img src="https://user-images.githubusercontent.com/4720428/53188456-3de33380-35ba-11e9-98c5-1f96424a2dbf.png" alt="alt text" width="350" height="600">









