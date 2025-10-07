# Form Events

## Example

```html
<form id="myForm" action="/action">
  <input type="text" name="username" placeholder="Username" required />
  <input type="password" name="password" placeholder="Password" required />
  <button type="submit">Submit</button>
</form>
```

```javascript
const form = document.querySelector("#myForm");

form.addEventListener("submit", (event) => {
  event.preventDefault(); // Prevents the default form submission behavior
  const formData = new FormData(form);
  const username = formData.get("username");
  const password = formData.get("password");
  console.log(`Username: ${username}, Password: ${password}`);
  // You can add further processing here, like sending data to a server
});
```
