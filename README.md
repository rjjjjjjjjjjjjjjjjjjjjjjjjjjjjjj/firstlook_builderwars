# FirstLook
### Understand your health. Find affordable care.

**AI-Powered Health Screening | Healthcare Accessibility | AWS**

🌐 **Live Website:** https://firstlook-health.lovable.app

## About the Project

Healthcare is expensive, even with insurance. Sometimes, a simple rash or minor injury can leave someone wondering whether they need to visit a doctor and how much that visit might cost.

We created **FirstLook** to make healthcare less stressful, more accessible, and more affordable.

FirstLook allows users to upload pictures of injuries, wounds, or skin concerns and describe their symptoms. AI analyzes the information and provides possible explanations, warning signs, and recommendations for seeking medical attention.

Our goal isn't to replace doctors. It's to help people understand their concerns and make informed decisions without unnecessary panic or unexpected medical expenses.

## Key Features

- **AI Injury Screening:** Upload an image and describe symptoms to receive a preliminary assessment.
- **Personal Health Dashboard:** Manage health concerns in one organized place.
- **Injury Logs:** Save previous screenings and track changes over time.
- **Find Care:** Search for nearby specialists based on medical concerns.
- **Insurance Cost Estimator:** Explore potential expenses using deductibles, copays, and coinsurance.
- **AWS Integration:** Store synthetic screening images and records using AWS cloud services.

## Technology Stack

| Technology | Purpose |
|---|---|
| React & TypeScript | Website development |
| Tailwind CSS | User interface |
| Lovable AI | Image and symptom analysis |
| AWS Lambda | Serverless storage processing |
| Amazon S3 | Test image storage |
| Amazon DynamoDB | Test screening records |
| Python | AWS backend |

## How It Works

**Upload an injury photo → Describe symptoms → Receive AI guidance → Explore affordable care options**

Users can save their results, monitor concerns over time, and use the insurance cost estimator to understand possible expenses.

The main screening uses Lovable AI. AWS Lambda, S3, and DynamoDB are integrated through a separate, working synthetic-data storage workflow.

## Challenges & What We Learned

One of our biggest challenges was integrating AI screening with AWS. We initially explored Amazon Bedrock but encountered account restrictions that prevented model inference.

We adapted by using Lovable AI for image analysis and AWS for cloud-based test storage.

We also learned how complicated healthcare pricing can be, especially when insurance deductibles, provider networks, and out-of-pocket expenses are involved.

## What's Next?

We plan to expand FirstLook with verified insurance-network information, provider-specific cost comparisons, wearable health-device integration, and improved injury monitoring.

## Built For

**BuilderWars Hackathon — AWS: Most Impactful AI Architecture**

**AI Tools Used:** Lovable, Lovable AI, and ChatGPT.

---

### Our Mission

We believe people shouldn't have to choose between worrying about their health and worrying about medical bills.

**FirstLook is our step toward making healthcare easier to understand, navigate, and afford.**

*Disclaimer: FirstLook provides preliminary AI-generated health information, not medical diagnoses. Cost estimates are illustrative and not guaranteed insurance quotes.*
