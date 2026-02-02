### Question. What are the default margins that exist in CSS (Body margin), and how do we remove them?

**Answer:**

Every browser (Chrome, Firefox, Edge, Safari, etc.) ships with its own built-in CSS known as the **User Agent Stylesheet**.

This means:

- Even if you write **no CSS at all**
- The browser still applies **some default styling**

---

One of the most important default styles applied by the browser is the **body margin**.

By default, browsers add margin to the `<body>` element.

**Default value applied by the browser:**

    body {
      margin: 8px;
    }

- ✅ This CSS is **not written by you**
- ✅ This CSS is **automatically added by the browser**

---

### Why does the browser add a default body margin?

Historically, this was done to:

- Prevent text from sticking to the edges of the screen
- Improve readability on simple web pages

However, in modern layouts (navbars, dashboards, full-width UIs, web apps):

👉 This default margin becomes a **problem**.

So we usually remove the browser’s margin and start styling from scratch.

---

### How to remove the default body margin (correct way)

**Solution:**

    body {
      margin: 0;
    }

That’s it.

This removes the browser-added spacing completely.

---

### What happens visually when you remove it? (Mental model)

❌ **Without removing margin**

    ⬜ gap   [ NAVBAR ]   gap ⬜

✅ **After setting `margin: 0`**

    [ NAVBAR TOUCHES SCREEN EDGE ]

Your layout now starts exactly from the edge of the viewport.

---

### Important note (Interview + real-world detail)

- Only the **`body`** element has a default margin
- Many other elements like `h1`, `p`, `ul` also have default margins
- But **body margin** is the most **layout-breaking** default

---

### Best practice (Industry standard)

Almost every real-world project starts with:

    body {
      margin: 0;
    }

Or uses a **CSS reset / normalize stylesheet** to remove all browser defaults.
