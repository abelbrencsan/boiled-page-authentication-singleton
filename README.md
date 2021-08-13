# Boiled Page authentication singleton

Authentication SCSS singleton for Boiled Page frontend framework. It is intended to create sign in, register and password reset pages.

## Install

Place `_authentication.scss` file to `/assets/css/singletons` directory, and add its path to singleton block in `assets/css/app.scss` file. You will also need to add form component to make form inputs working properly.

- Form component: <https://www.github.com/abelbrencsan/boiled-page-form-component>

## Usage

### Classes

Class name | Description | Example
---------- | ----------- | -------
`authentication` | Applies authentication. | `<main class="authentication"></main>`
`authentication` | Applies a list of links inside authentication. Use grid component for alignment. | `<ul class="authentication-link-list grid"></ul>`

### Examples

#### Example 1

The following example shows a sign-in form as main content. Do not forget to add `main` id when skiplink is used.

```html
<main class="authentication">
  <div class="container container--half">
    <header class="header">
      <h1>Sign in to website</h1>
      <p>Dolores reiciendis molestias optio quos</p>
    </header>
    <div class="box">
      <form class="form" method="post" action="">
        <div class="grid grid--gutter grid--gutter--half grid--uniform">
          <div class="grid-col grid-col--full">
            <div class="form-item">
              <label class="form-label" for="email">E-mail</label>
              <input name="email" id="email" class="form-input" type="text" />
            </div>
          </div>
          <div class="grid-col grid-col--full">
            <div class="form-item">
              <label class="form-label" for="password">Password</label>
              <input name="password" id="password" class="form-input" type="password" />
            </div>
          </div>
          <div class="grid-col grid-col--full">
            <button class="button button--fit" type="submit">Sign in</button>
          </div>
        </div>
      </form>
      <ul class="authentication-link-list grid grid--center grid--gutter grid--gutter--half grid--uniform">
        <li class="grid-col">
          <a href="#">Forgot password</a>
        </li>
        <li class="grid-col">
          <a href="#">Create account</a>
        </li>
      </ul>
    </div>
  </div>
</main>
```
