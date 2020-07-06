# HTML Forms

A form collects different information and then process it with the backend application based on the logic.

## The ```<form>``` Element

The "form" element is a block level element, to initialize a form we use the "form" element with some attribute i.e. "action" and "method". The action attribute contains a URL to which the collected information from the form will send for further processing by the server. The method attribute contains HTTP methods that the browser uses to submit the data.

```
<form action="/login" method="post">
    <!-- Form elements like input, textarea etc. -->
  </form>
```

## Text and Textarea Fields

To collect single line data we use "input" and to collect multiple lines data we use "textarea" element.

### Text Fields(input)

The input fields are one of the primary elements of the form to collect the single-line text-based information from the users and it is a self-contained inline-level element. For example, if we want to collect the user's name, email, password, or any search query, etc. This element comes with some i.e. "type", "name" etc. The "type" attribute accepts many values i.e. "email", "password", "search" etc., one of the most popular values for the type attribute is text mostly used to collect the user's name. The "name" attribute is necessary for the backend part .

```
<input type="text" name="username">
<input type="email" name="email-address">
<input type="password" name="password">
<input type="search" name="search">
<input type="date" name="birthday">
<input type="time" name="session-time">
```
These are the few examples of a type of attribute value that you usually see within the input element. Apart from these, there is a list of input types that may find on a page.

- color
- date
- datetime
- email
- month
- number
- range
- search
- tel
- time
- URL
- week

### Textarea Field

Whenever we need multi-line text-based information from users the textarea element is used. For example for any messages or any query related information. The textarea element doesn't accept the type attribute because there is just one type. But the name attribute is needed. The textarea element accepts the other two attribute col and rows that size of the textarea element. The col attribute is the width in terms of characters and the row attribute is height in terms of several lines.

```
<textarea name="message" col="30" rows="10">
    Your Message...
  </textarea>
```

## The Radio Button, Checkbox Control and Drop Down Lists

The radio button and checkbox and select(Drop Down Lists) within the HTML form allow users to select data using multiple choices. It can bethink as multiple-choice questions.

### The Radio Button

The radio buttons are used when users need to select one option out of multiple options. Radio buttons are created using the input element with a type attribute value of radio. All the radio button type attributes must have the same value so that they will be within a group correspond to one another. The radio button accepts the value attribute to set the specific value for each input element. There is checked boolean attribute to preselect any option.

```
<input type="radio" name="language" value="HTML" checked> HTML
<input type="radio" name="language" value="CSS"> CSS
<input type="radio" name="language" value="JavaScript"> JavaScript
```

### The Checkbox Control

Using radio button input a user can select one option out of multiple options. But many times there can a need of selecting multiple options. To provide the ability to select multiple options input element is used with type attribute value of checkbox. The rest of the attribute value remains the same similar to the radio button.

```
<input type="checkbox" name="language" value="HTML" checked> HTML
<input type="checkbox" name="language" value="CSS"> CSS
<input type="checkbox" name="language" value="JavaScript"> JavaScript
```

### Drop Down Lists

To create a drop down list we use ```<select>``` and ```<option>``` elements . The ```<select>``` elements wraps ```<option>``` elements to markup all the option within the list. The option elements come with the value attribute which corresponds to the name attribute on the select element. All the visible content will reside inside the option element, based on which user will select the option. If an option you would like to show the user preselected, we can apply selected boolean attribute on the option element.

```
<select name="language">
  <option value="HTML" selected>HTML</option>
  <option value="CSS">CSS</option>
  <option value="JavaScript">JavaScript</option>
  <option value="Ruby" selected>Ruby</option>
  <option value="Python">Python</option>
  <option value="PHP">PHP</option>
</select>
```

> Multiple Selections
>
  Applying multiple boolean attribute provide ability to users to select multiple options from a drop-down list. To select multiple options the user will have hold the Shift key while clicking the options. Using selected boolean attribute on more than one options will show the user preselected multiple options.

```
<select name="language" multiple>
   <option value="HTML" selected>HTML</option>
   <option value="CSS">CSS</option>
   <option value="JavaScript" selected>JavaScript</option>
   <option value="Ruby" selected>Ruby</option>
   <option value="Python">Python</option>
   <option value="PHP">PHP</option>
 </select>
```

##  Other Inputs

There are few other types of inputs like "hidden" and "file".

### Hidden Input

The hidden type of input is created using the hidden value for the type attribute within an input element which are not displayed on the page but can be found while viewing the source code of the page. The hidden inputs are typically used to track-codes or other pieces of information which are not relevant to users, but helpful in processing the form data.

```
<input type="hidden" name="tracking-code" value="abc-123">
```

### File Input

The file input allows users to add files to a form. To create file input use file value for the type attribute within an input element.

```
<input type="file" name="file">
```

## Buttons

We can make buttons using input element and with button element also.

### Submit Input Button

To create the input button use submit value for the type attribute within the input element.

```
<input type="submit" name="submit" value="send">
```

### Submit Button Element

The button element provides more control over the style of the input element. The button element comes with an opening and closing tag that may wrap other elements. Sometime you may wrap an icon inside the button element, for better style and design of the button.

```
<button name="submit">
    <strong>Send</strong> Message
  </button>
```

## Organizing Form Elements

There is some other elements to organize the form.

### The ```<label>``` element

This tag works as a heading or label for any form element . The ```<label>``` element is a inline-level element . The label element may include for attribute The value of the attribute must be the same as the id attribute value on the form element. Keeping the for attribute and id attribute value tie them together. That allows users to click on the label and bring focus on the connected form element.

```
<label for="username">Username</label>
 <input type="text" name="username" id="username">
```

Sometime label element may wrap the input element with a type of radio or checkbox, doing so you can omit the for and id attribute.

```
<label>
    <input type="radio" name="language" value="HTML" checked> HTML
  </label>
  <label>
    <input type="radio" name="language" value="CSS"> CSS
  </label>
  <label>
    <input type="radio" name="language" value="JavaScript"> JavaScript
  </label>
```

### The ```<fieldset>``` element

The ```<fieldset>``` is a block-level element. It allows us to group the different form controls and labels into organized sections. The <fieldset> element by default comes with a border outline that may be modified using CSS.

```
<fieldset>
    <label>
      Username
      <input type="text" name="username">
    </label>
    <label>
      Password
      <input type="password" name="password">
    </label>
  </fieldset>
```

### The ```<legend>``` element

The <legend> element used to provide a caption or heading to a form. That helps users to understand what type of is.

```
<fieldset>
    <legend>Login</legend>
    <label>
      Username
      <input type="text" name="username">
    </label>
    <label>
      Password
      <input type="password" name="password">
    </label>
  </fieldset>
```

## Additional Attribute

In addition to all the attributes that we have seen above, there are other attributes also with different functionality.

### The Disable Attribute

This boolean  attribute  turns off any form of control. Doing so the users won't be able to interact with the elements, but it will display on the page. The disabled element won't send any information to the server for the form processing.

```
<label>
  Username
  <input type="text" name="username" disabled />
</label>
```

### The Placeholder Attribute

The placeholder value will appear on the page inside the form control but once you focus or click on the element the placeholder value disappears. It works like a hint how the form  input should be filled.

```
<label>
  Email Address
  <input type="email" name="email-address" placeholder="xyz@example.com" />
</label>
```

### The Required Attribute

If a form element contains required boolean attribute means that field must not be left blank. That field must contain a value before submitting the form to the server. If the field is left blank the form will through an error message.

```
<label>
  Email Address
  <input type="email" name="email-address" required />
</label>
```
