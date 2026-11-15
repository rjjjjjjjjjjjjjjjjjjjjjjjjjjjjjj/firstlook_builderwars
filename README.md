# FirstLook
### Understand your health. Find affordable care.

**AI-Powered Health Screening | Healthcare Accessibility | AWS**

🌐 **Live Website:** https://firstlook-photo-insights.lovable.app/

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
| React & TypeScript (built with Lovable) | Mobile-first web app |
| Tailwind CSS | Styling and responsive layout |
| Lovable Cloud (Supabase) | Sign-in, saved history, health profile, and the server-side function that calls AWS |
| Strands Agents (open source, AWS) with Claude (Anthropic) | Agent framework and AI model for photo and symptom analysis |
| AWS Lambda (Python) | Serverless backend: emergency rules, safety checks, and the AI call |
| Amazon S3 | Photo storage with automatic deletion |
| Amazon DynamoDB | Records of each check |

## How It Works

1. **Emergency check first.** Severe symptoms like heavy bleeding or trouble breathing skip the AI entirely and open a full-screen Call 911 screen.
2. **Photo, description, and symptoms (all optional).** Users can add a photo, a short description, symptoms, and risk factors, which an optional health profile can pre-fill. If they give almost nothing, FirstLook says it needs more information and does not guess.
3. **Secure handoff.** The app's backend function sends the check to AWS Lambda with a secret key, so no credentials ever reach the browser.
4. **Rules plus AI.** Lambda applies the emergency and risk rules first. Then Claude, running through the Strands agent framework, analyzes the photo and symptoms. Code rules can raise the urgency level but never lower it.
5. **Clear result.** The user sees a care level (manageable at home for now, clinic, urgent care, or emergency), a plain-language explanation, next steps, warning signs, and a rough cost comparison.
6. **Storage and history.** Photos go to S3 and a record goes to DynamoDB. The user's account and saved history stay in Lovable Cloud, where they can add follow-up photos and compare healing over time.

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
