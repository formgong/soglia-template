# Soglia — designer windows site with a Formgong form

**Live demo:** https://soglia.formgong.com · Download: the [latest release](https://github.com/formgong/soglia-template/releases/latest) zip.

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/formgong/soglia-template) [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fformgong%2Fsoglia-template&project-name=soglia&repository-name=soglia)

Each button copies the site to your GitHub and publishes it. Then replace `fk_your_access_key` in `index.html` of your copy with your Formgong access key (free at https://formgong.com/new) and commit: the host republishes on its own.

Шаблон сайту дизайнерських вікон з формою Formgong

A standalone template, not a Lattice variation, so it has no visible grid.

- **Home** is a single screen: paper on the left and the photo on the right. A stepped dark tab names the category and a white caption names the piece.
- **The slider** moves with the wheel or a vertical swipe (category), and with the arrows or a horizontal swipe (piece). Arrow and Page keys work too.
- **On every change** the photo wipes in and each label rolls letter by letter.
- **Autoplay** runs with a progress bar under "Discover more" and waits while the pointer or focus is on the caption.
- **Contacts** is a second view in the same file. It has ateliers in hairline rows, a dark customer-service card, the Formgong form and a light footer.
- **Transitions.** A slate curtain passes between the two views. A slate loader with rolling words plays once per tab session.

## English

**Set up the form**

1. Create a form in the Formgong dashboard and copy its access key.
2. In `index.html`, replace `fk_your_access_key` with that key.
3. Optional: put your Turnstile site key in `data-sitekey` on `<form id="fg-form">`.

The form sends `name`, `email`, `phone`, `city`, `message`, `privacy` (required) and `marketing` (optional). It shows "received" only when the server answers `success: true`.

**Edit**

- Slider categories and pieces are in the `CATS` array in the script. `img` is the index of the photo in `.stage`.
- `AUTOPLAY` is the time per slide in milliseconds; `0` turns it off. The loader words are in `LOADER_WORDS`.
- Links: `#contacts` opens the contacts view and `#contact-form` jumps to the form. `#home` returns to the slider.
- Sizes follow `--r`, which is 12px on a 1280px screen and grows with the window. Below 900px the layout switches to a phone layout.
- With `prefers-reduced-motion: reduce` there is no loader or curtain, and slides switch without wipes.

**Images.** All six were made for this template with FLUX.1 [schnell] (Apache 2.0), on the free Hugging Face Space and the AI Horde. You may use them in your own site. Replace them with photos of your own work, keeping the file names.

## Українська

Окремий шаблон, не варіація Lattice: без сітки. Головна сторінка — один екран зі слайдером:

- коліщатко або свайп угору-вниз змінює категорію;
- стрілки або свайп убік змінюють роботу;
- фото заїжджає «шторкою», підписи перекочуються по літерах.

Контакти відкриваються другою сторінкою в тому самому файлі. Там адреси ательє, темний блок сервісу, форма й світлий підвал.

**Форма:** замініть `fk_your_access_key` на ключ форми з кабінету Formgong. Форма надсилає ім'я, пошту, телефон, місто, запит, обов'язкову згоду на обробку даних і необов'язкову згоду на розсилку.

**Картинки:** усі згенеровано для цього шаблону моделлю FLUX.1 [schnell] (ліцензія Apache 2.0) через безкоштовні Hugging Face і AI Horde. Замініть їх фото своїх робіт, зберігши назви файлів.
