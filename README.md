# Stochos Engineering & Projects Limited

Company website for Stochos Engineering & Projects Limited, serving industrial and infrastructure projects in Ghana and the wider West African region, in collaboration with Tenaro Global EPC and the Dehu Group.

The site is plain HTML and CSS, with no JavaScript and no build step. The mobile menu is CSS-only, and the contact form is delivered by [FormSubmit](https://formsubmit.co).

## Run locally

Pages use clean folder URLs (`/about/`, `/capabilities/`, …), so serve the folder with any static web server rather than opening the files directly:

```sh
python3 -m http.server 8000
```

Then visit `http://localhost:8000/`.

## Project layout

```text
index.html                Home
about/index.html          About, approach and group credentials
capabilities/index.html   Capabilities, standards and industries
products/index.html       Product range, mining applications and support services
network/index.html        Tenaro / Dehu ecosystem and global network
contact/index.html        Enquiry form
css/styles.css            Global and responsive site styles
images/                   Website photographs and partner logos
images/products/          Product photos from Dehu Engineering (dehu.in)
```

The Stochos logo is built into each page: the "S" mark is an inline SVG (`#stochos-mark`) and the name is set as text, so it stays sharp at any size and switches to a light version in the footer. `images/Stochoslogo.jpeg` is the original logo file and `images/favicon.svg` is the browser tab icon. The brand colours come from the logo: blue `#043577` and charcoal `#313131`.

The header and footer are repeated in each HTML page, so edit all six pages when changing navigation or footer content. Links between pages are relative (`../about/`), so the site also works when hosted in a sub-folder.

## Configuration notes

- The contact form in `contact/index.html` sends enquiries to info@stochosengg.com through FormSubmit. FormSubmit sends a one-time activation email to that address on the first submission; confirm it and later enquiries arrive as emails, including any attached file.
- Update the copyright year in the footer of each page when it changes.
- Add the published email and phone number in the `contact-details` block of `contact/index.html` before launch.
