README.md 

Carbon Footprint Estimator

A simple backend API that estimates the carbon footprint of dishes based on their ingredients.


Features
 - POST /estimate` → Estimate from dish name (mock LLM)
 - POST /estimate/image` → Estimate from uploaded image (mock Vision)
 - Static carbon dataset (`carbonValues.json`)
 - Dockerized for easy run

Setup

--bash
git clone <your-repo>
cd carbon-estimator

How to run locally:

npm install
npm run dev


Example requests:

curl -X POST http://localhost:3000/estimate -H "Content-Type: application/json" -d '{"dish":"Chicken Biryani"}'


Example response:

{
  "dish": "Chicken Biryani",
  "estimated_carbon_kg": 4.2,
  "ingredients": [...]
}
