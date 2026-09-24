<a href="https://villabellavista.rs/"><img src="media/cover.jpg" alt="Villa Bella Vista, home page on a laptop and a phone" width="100%"></a>

# Villa Bella Vista

Site for four holiday apartments on Divčibare, where each unit has its own gallery and every inquiry is saved before any email goes out.

**[villabellavista.rs](https://villabellavista.rs/)** · [Case study (in Serbian)](https://svilenkovic.com/radovi/villa-bella-vista) · [Srpski](README.sr.md)

> [!NOTE]
> Client project. The source code belongs to the client and stays in a private repository. This page describes what I built and how.

<table>
  <tr><td><b>Client</b></td><td>Villa Bella Vista</td></tr>
  <tr><td><b>Industry</b></td><td>Holiday apartment rental</td></tr>
  <tr><td><b>Location</b></td><td>Divčibare, Serbia</td></tr>
  <tr><td><b>Type</b></td><td>Multi-page website</td></tr>
  <tr><td><b>My role</b></td><td>Design, development, SEO, hosting and maintenance</td></tr>
  <tr><td><b>Stack</b></td><td>PHP 8.3, SQLite, PHPMailer, nginx, JSON-LD</td></tr>
</table>

## About the project

Villa Bella Vista rents out four apartments on Divčibare, and the owner confirms every stay herself after checking the dates. Guests need to compare the four spaces, see enough photos and send their dates without getting the impression that the booking is already confirmed. The site follows that order and leaves the final agreement to the owner.

An inquiry is first written to a SQLite database outside the public folder, and only then does the site try to email the owner. A token on each submission blocks duplicates and a rate limit protects the form. If the notification cannot go out right away, it waits in a retry queue, so no guest ever has to type the request twice.

## What I built

- A page for each apartment with its own photos, plus a comparison page for all four
- An inquiry form for dates, guests, preferred apartment and contact, stating plainly that an inquiry is not a booking
- Galleries in AVIF, WebP and JPEG at several widths, with known dimensions so the layout does not jump
- Notifications sent through PHPMailer from a queue that keeps retrying until they go out
- A guide to Divčibare for guests planning their days on the mountain
- Automated tests for the PHP code

## Results

| | Performance | Accessibility | Best practices | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Mobile | 99 | 100 | 100 | 100 |
| Desktop | 100 | 100 | 100 | 100 |

PageSpeed Insights, lab test of the live site, September 2026. Security headers: 6 of 6. HTML validator: no errors. axe accessibility check: no violations. Structured data: `LodgingBusiness`.

## Screenshots

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Villa Bella Vista, home page on a 1440 px screen"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Villa Bella Vista, home page on a phone"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="A shared page helps guests compare the four accommodation units">
<sub>A shared page helps guests compare the four accommodation units</sub>

<img src="media/inner-2.webp" alt="Each apartment has its own page, gallery and a direct path to an inquiry">
<sub>Each apartment has its own page, gallery and a direct path to an inquiry</sub>

---

<sub>Built by [D. Svilenković](https://svilenkovic.com).</sub>
