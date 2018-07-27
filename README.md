# gatsby-plugin-crisp-chat

Add [Crisp Livechat](https://crisp.chat/) to your Gatsby site.

## Install

`npm install --save gatsby-plugin-crisp-chat`

## How to use

To integrate Crisp Livechat to your Gatsby site, you need to have an account with Crisp. [Sign up](https://app.crisp.chat/initiate/signup/).

Once you sign up, you will be prompted with ways you can integrate Crisp to your site. Click the HTML option and copy your `CRISP_WEBSITE_ID`. It should be in this form: `xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx` (8-4-4-4-12chars).

> If you aren’t new to Crisp, you can get your `CRISP_WEBSITE_ID` by going to Website Settings > Integrations > HTML.

Upon obtaining your `CRISP_WEBSITE_ID`, you need to modify your `gatsby-config.js` as follows:

```js
// In your gatsby-config.js
module.exports = {
  plugins: [
    {
      resolve: 'gatsby-plugin-crisp-chat',
      options: {
        websiteId: 'YOUR_CRISP_WEBSITE_ID',
        // Optional. Disables Crisp Chat during gatsby develop. Defaults to true.
        enableDuringDevelop: false,
      },
    }
    'your',
    'other',
    'plugins',
  ],
}
```

Restart your Gatsby server for the plugin to take effect.

If you have improvements that you’d like to see, or encounter any bugs, feel free to [create an issue](https://github.com/ryanditjia/gatsby-plugin-crisp-chat/issues)!

## Changelog

Version 2 has a breaking change: configuration option that used to be named `development` has been reworded to `enableDuringDevelop` so its purpose is much clearer.
