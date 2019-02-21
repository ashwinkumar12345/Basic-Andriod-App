# Building an Andriod Application

After you have a basic understanding of Andriod Studio and have it installed and running on your computer, you can use it to build the UI elements, connect it to the backend code, and test the app on the emulator. The Andriod app takes some input text from the user and outputs the same text onto the screen. The steps for building this Andriod app are as follows:

> ## Contents

**[Building UI in XML Files](#UI)**<br>
**[Connecting UI to Backend Code with Variables and Methods](#Connect)**<br>
**[Implementing Backend Functionality](#Implement)**<br>
**[Testing on Emulator](#Testing)**<br>

<a name="UI"></a>
> ## Building UI in XML Files

You can build the UI using XML text:

1. Open the *activity_main.xml* file
2. The *TextView* element is setup by default 
3. Copy the *EditText*, *Button*, and *TextView* elements from the *activity_main.xml* file
4. Copy the string resources from the *strings* file

<a name="Connect"></a>
> ## Connecting UI to Backend Code with Variables and Methods

You need to gain access to the *EditText* and *TextView* elements from the UI.

1. Open the *MainActivity.java* file.
2. Declare the UI elements variables:

```
EditText editText;
TextView textView;
```
The import statements are automatically added.

2. Initialize these variables in the *OnCreate* method:

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
> ## Implementing Backend Functionality

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
> ## Testing on Emulator

Load up an emulator using the AVD manager and run the program:











