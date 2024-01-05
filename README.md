

# vue-cookie-consent

A simple Vue.js / tailwind component to help your site comply with the EU cookie law

All sites owned by EU citizens or targeted towards EU citizens must comply with EU law. This law requires a dialog to be displayed to inform the users when you are using tracking cookies. You can read more info on the legislation on the site of [the European Commission](https://commission.europa.eu/resources-partners/europa-web-guide/design-content-and-development/privacy-security-and-legal-notices/cookies-and-similar-technologies_en). Be aware using cookies for a site/web app that is not used for tracking (for example: session cookies) do not fall under this obligation.

This component is a quick and simple way to display the required dialog in your Vue.js application. It sets a cookie when a user agrees with the cookie policy. The component will not be rendered once the cookie has been set.

quote:

	Cookies and similar technologies requiring consent

	Cookies and similar technologies that generally DO need consent

    Social plug-in tracking mechanisms
    Third party advertising cookies
    Analytics cookies (except for the exemption described further below)

	Cookies and similar technologies that generally do NOT need consent

    User entrada cookies, for the duration of a session
    Authentication cookies, for the duration of a session
    User centric security cookies, used to detect authentication abuses and linked to the functionality explicitly requested by the user, for a limited persistent duration
    Multimedia content player session cookies, such as flash player cookies, for the duration of a session
    Load balancing session cookies, for the duration of a session
    User interface customisation cookies, for a browser session or a pocos hours, unless additional information in a prominent location is provided (e.g. “uses cookies” written next to the customisation feature)


## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Support](#support)
- [Contributing](#contributing)

## Installation

Add the CookieConsent.vue file from this package to your component library.

## Usage

Add this component anywhere you'd like it to appear. (We recommend your app layout)

`import CookieConsent from '{component-library-directory}/CookieConsent.vue'`

Place the component

`<CookieConsent/>`

Feel free to update the CookieConsent.vue file to meet your apps requirements.


## Support

Please [open an issue](https://github.com/CodeSuite/laravel-cookie-consent/issues/new) for support.

## Contributing

Please contribute using [Github Flow](https://guides.github.com/introduction/flow/). Create a branch, add commits, and [open a pull request](https://github.com/CodeSuite/laravel-cookie-consent/compare/).
