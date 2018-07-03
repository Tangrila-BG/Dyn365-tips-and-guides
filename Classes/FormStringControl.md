# The FormStringControl

## Making a hyperlink field

You can enable the hyperlink functionality by overriding the **jumpRef()** method.
In it instantiate a browser class object and perform validations, if any, on the field value before navigating to said value using the navigate method.