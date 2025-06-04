# 🌍 WattWise – Smart Energy Estimator 🔌

**WattWise** is a cloud-based system that helps homeowners, office managers, and building owners estimate and understand their monthly electricity usage — without connecting any hardware.

The platform enables users to simulate their energy consumption based on appliance data, electricity source, and charging needs, and receive actionable suggestions to lower their bills.

---

## 💡 Why WattWise?

Most people don’t know how much electricity each device in their home or office consumes — and what their energy bill is really made of.  
**WattWise** solves this by providing a **smart, serverless cloud system** for visualizing and optimizing energy consumption — no smart plugs or meters needed.

---

## 🧩 Key Features

- 🏘️ Add multiple **properties** – homes, apartments, or office buildings  
- 🧰 Select devices per property from a built-in database (residential + commercial)  
- ⚡ Specify your **electricity source**:
  - National electricity supplier (e.g. grid)
  - Solar panel system
  - Combination of both
- 🚗 Add **electric vehicle charging** data to calculate its energy cost  
- 📊 Get **monthly cost estimates** for each device and total usage  
- 🗂️ Organize by rooms or office zones (e.g., kitchen, living room, server room)  
- 🔐 Secure user accounts with AWS Cognito  
- 💡 View **alternative products** and tips for saving electricity  
- 🌎 Multi-language & international-ready  

---

## ⚙️ Tech Stack

### ☁️ Backend (AWS Serverless)
- **AWS Lambda** – Compute logic for calculations  
- **Amazon API Gateway** – REST API layer  
- **Amazon DynamoDB** – NoSQL storage for user data and device selections  
- **Amazon Cognito** – User authentication and account management  
- **AWS S3** – Static content (optional)  
- **CloudWatch Logs** – For monitoring and debugging  

### 💻 Frontend
- **React** (or Next.js)  
- **AWS Amplify** – Hosting + CI/CD integration  

---

## 🏗️ Project Structure

```

wattwise/
├── frontend/                # React frontend (with Amplify)
├── backend/                 # Lambda functions + API
├── infrastructure/          # Infra-as-code (e.g., CDK or Terraform)
├── data/
│   ├── home\_devices.json    # Appliances for homes
│   ├── office\_devices.json  # Equipment for offices
│   └── energy\_sources.json  # List of energy providers/types
└── README.md

````

---

## 🧮 Example Device Data

### Home Appliance
```json
{
  "name": "Refrigerator (Standard)",
  "category": "Kitchen",
  "avg_kw_per_hour": 0.15,
  "avg_hours_per_day": 24
}
````

### EV Charging

```json
{
  "name": "Tesla Model 3 Charger",
  "avg_kw_per_hour": 7.2,
  "avg_hours_per_day": 2
}
```

### Energy Source

```json
{
  "source": "Grid",
  "cost_per_kwh": 0.18
},
{
  "source": "Solar",
  "cost_per_kwh": 0.05
},
{
  "source": "Hybrid",
  "grid_percentage": 60,
  "solar_percentage": 40
}
```

---

## 📌 Use Cases

* 🏡 **Homeowners** – Understand electricity use per room/device + solar vs. grid
* 🚘 **EV Owners** – Estimate car charging impact on monthly bill
* 🏢 **Office Managers** – Analyze energy use per floor/room/device
* 🧑‍🔧 **Building Owners** – Estimate consumption across tenants
* 💼 **Energy Consultants** – Use as a simulation tool for client analysis

---

## 🗺️ Roadmap

* [x] Create base appliance database (residential + commercial)
* [x] Add electricity source selector (Grid / Solar / Hybrid)
* [x] Add EV charging component
* [ ] Build frontend with React and AWS Amplify
* [ ] Develop Lambda functions for usage calculations
* [ ] Set up user management with Cognito
* [ ] Build dashboard for results & tips
* [ ] Add recommendation engine for energy-efficient products
* [ ] Enable multiple language/localization support

---

## 🛠️ Getting Started (coming soon)

You will need:

* AWS account
* Node.js + Amplify CLI
* (Optional) Terraform or AWS CDK for deploying infrastructure

Setup steps will be added in the next phase of the project.

---

## 🤝 Contributing

Pull requests and suggestions are welcome!
If you’d like to contribute to frontend, backend logic, or appliance database – feel free to open an issue.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🌟 Stay WattWise

Electricity is invisible. WattWise makes it visible, understandable, and manageable –
so people and businesses around the world can **take control of their energy use**.

> Built as part of a personal journey into cloud architecture and AWS serverless technologies.

