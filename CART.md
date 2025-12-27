Cart & WhatsApp Checkout

Overview
- `cart.html` reads your cart from `localStorage` key `cart`.
- Items are added to the cart via the "Add to Cart" button on `productsdetails.html`.
- The cart page allows changing quantities, removing items, clearing the cart, and "Checkout on WhatsApp".

WhatsApp Checkout
- Clicking "Checkout on WhatsApp" builds a message with:
  - Optional buyer name and phone entered on the cart page
  - Item lines with title, ref (id), optional color, qty, price and line total
  - Order total
  - A short note asking to confirm availability
- The message opens WhatsApp Web/mobile using the shop phone number configured in the file(s):
  - `productsdetails.html` (variable `phone`)
  - `cart.html` (variable `phone`)

Customisation
- To change the shop phone, edit `const phone = '254718770397';` in `cart.html` and `productsdetails.html`.
- To improve totals or currency formatting, update `formatPrice`/`formatCurrency` in `cart.html`.

Notes
- The cart is stored locally in the browser (no server-side cart). Use the cart page to review and check out.
- For production, replace the simplistic cart with a backend cart and integrate with a proper checkout flow.