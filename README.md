# Diet Feast

Website for Diet Feast, a local ultra-low-calorie meal prep service in Worcester, MA: 120 to 165 calorie shirataki-noodle meals, halal-friendly, delivered or picked up.

The site covers the meals, plans, how it works and the market, and has an order section with a multi-item cart, a meal builder, and a delivery-fee estimate based on distance.

## Stack

A single `index.html` with inline CSS and JavaScript, plus images in `assets/images/`. No framework, no build step. The delivery estimate geocodes the customer's address with OpenStreetMap Nominatim and computes straight-line distance in the browser.

## Run it

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

## Before taking real orders

**Place Order does not send the order anywhere.** It shows a confirmation on the page and clears the cart. Connect the form to email, a form service or a database before publishing. Payment is cash on delivery; no online payment is collected.

## Other files

- `project_details/DIET_FEAST_STARTUP_DESCRIPTION.md`: business plan and pricing assumptions
- `project_details/recipes.md`: recipes
- `project_details/DIET_FEAST_PITCH_WEBSITE.html`: earlier pitch page
- `project_details/WEBSITE_CUSTOMIZATION_GUIDE.md`: notes on editing the pitch page
