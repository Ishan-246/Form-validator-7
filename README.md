# Form Validator App 

A simple React app that validates form inputs for **Name** and **Email**.  
Displays error messages for invalid or empty fields.

##  Built With

- React
- useState hook
- Basic form validation

##  Preview

<img width="717" height="1080" alt="Screenshot (90)" src="https://github.com/user-attachments/assets/47ddaf28-1ad5-4da8-b4c8-65eda3139808" />


##  Features

- Checks for empty `Name` or `Email`
- Validates if email contains "@"
- Displays red error message
- Alerts valid form submission


## LINE BY LINE EXPLANATION 


A)    const [name, setName] = useState('');   =

Declares a state variable name, initialized with an empty string ('').
setName is a function to update name.
Stores the user's name input.



B)     const [email, setEmail] = useState('');  =

Declares a state variable email, also initialized with an empty string.
setEmail updates the email input value.



C)     const [error, setError] = useState('');  =

Declares a state variable error, initialized as an empty string.
setError updates the error message shown to the user.


D)       const handleSubmit = (e) => {  =

Defines a function handleSubmit which triggers when the form is submitted.
Takes an event object e.


E)      e.preventDefault(); 
       & 
       if (!name || !email) {  =

Prevents the default form submission behavior (which would refresh the page).
&
Checks if either name or email is empty (falsy).


G)       if (!email.includes('@')) { =

Checks if the email does not contain an '@' character, a simple validation for email format.




H)   SetError('Enter a valid email address!'); =

If invalid, sets an error message prompting for a valid email.



I)        return;
   Exits the function early to prevent form submission.
  jsx
    setError('');
Clears any existing error messages if all validations pass.


K)          alert (Form Submitted:\nName: ${name}\nEmail: ${email}`);=

Shows an alert box displaying the submitted name and email.
jsx

setName( );
 setEmail( ); 
Resets the input fields to empty strings after successful submission.


L)        <div style={{ maxWidth: '400px', margin: '50px auto', fontFamily: 'sans-serif' }}> =

Creates a <div> container with inline styles:
maxWidth: 400px: limits the container width.
margin: 50px auto: centers the container vertically and horizontally.
fontFamily: 'sans-serif': sets a clean font style.
jsx


M)  Form Validator 
Renders a header with the text "Form Validator".


N)         <form onSubmit={handleSubmit}>  =

Defines a <form> element.
Attaches the handleSubmit function to handle form submission.


O)    <input
          type="text"
          placeholder="Enter your name"
          value={name}
          onChange={(e) => setName(e.target.value)}
          style={{ width: '100%', padding: '10px', marginBottom: '10px' }}
         =
        
 Creates a text input for the name:
type="text" specifies it's a text input.
placeholder shows placeholder text guiding the user.
value={name} binds the input value to the name state.
onChange updates the name state whenever user types, using setName(e.target.value).
Inline styles make the input full-width, padded, and spaced.



P)         <input
          type="email"
          placeholder="Enter your email"
          value={email}
          onChange={(e) => setEmail(e.target.value)}
          style={{ width: '100%', padding: '10px', marginBottom: '10px' }}
        =
        
Similar input for email:
type="email" enables some native email validation.
Binds to email state and updates via setEmail.


Q)            {error && <p style={{ color: 'red' }}>{error}</p>} =

Conditionally renders an error message paragraph:
If error has a truthy value, it displays the error text in red.   


R)          <button type="submit" style={{ padding: '10px 20px' }}>Submit</button> =

Adds a submit button with padding styling.
type="submit" makes it trigger form submission   




## WHAT I LEARN FROM THIS CODE 

-Learned the meaning and use of placeholder
-learned how to write code for form submitting





