## 18 Numbers Project
[Project]()
<img width="1277" height="636" alt="Screenshot 2025-09-08 at 4 23 29 AM" src="https://github.com/user-attachments/assets/f46603ca-3e74-4bde-bf53-17107cf2d56f" />


#### Structure (HTML)

- section
  - article
    - span.number data-value="value" (0)
    - p (text)

#### Logic (JS)

- select all span's with .number
- iterate over and log each span
- create updateCount function
- accept el as argument
- invoke and pass each span el in iteration

```js
const updateCount = (el) => {
  const value = parseInt(el.dataset.value);
  const increment = Math.ceil(value / 1000);
  let initialValue = 0;
};
```

```js
const updateCount = (el) => {
  const value = parseInt(el.dataset.value);
  const increment = Math.ceil(value / 1000);
  let initialValue = 0;

  const increaseCount = setInterval(() => {
    initialValue += increment;

    if (initialValue > value) {
      el.textContent = `${value}+`;
      clearInterval(increaseCount);
      return;
    }
    el.textContent = `${initialValue}+`;
  }, 1);
};
```
