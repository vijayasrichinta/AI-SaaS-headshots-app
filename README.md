# 👨‍💼 [Headshot AI](https://headshots-starter.vercel.app/) – Professional AI Headshots

Headshot AI lets you generate professional AI headshots in minutes. This open-source project is designed to help developers and makers quickly build AI-powered headshot applications.

Use it as a starting point: fork the code, modify it, and make it your own.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fleap-ai%2Fheadshots-starter%2Ftree%2Fmain)

---

## How It Works

* Generates professional AI headshots from user-provided images.
* Uses AI models to learn the style of input images.
* Supports a credit-based or optional email notification system.
* Built with Next.js, Supabase (DB & Auth), Tailwind CSS, and Vercel for deployment.

Live demo **[here](https://getheadshots.ai)**.

---

## Running Locally

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

---

### 2. Install dependencies

Using npm:

```bash
npm install
```

Or yarn:

```bash
yarn
```

---

### 3. Set up environment variables

Create a `.env.local` file and configure the following:

```text
# API Key for AI model
NEXT_PUBLIC_API_KEY=your_api_key

# Webhook secret for model training callbacks
APP_WEBHOOK_SECRET=your-webhook-secret

# Deployment URL
DEPLOYMENT_URL=https://your-hosted-url

# Optional: enable announcement bar
NEXT_PUBLIC_ANNOUNCEMENT_ENABLED=true
NEXT_PUBLIC_ANNOUNCEMENT_MESSAGE="Your announcement message here"

# Optional: email notifications
RESEND_API_KEY=your-resend-api-key

# Optional: Stripe payments for credit system
STRIPE_SECRET_KEY=your-stripe-secret-key
STRIPE_WEBHOOK_SECRET=your-stripe-webhook-secret
NEXT_PUBLIC_STRIPE_IS_ENABLED=false
```

---

### 4. Magic Link Authentication (Supabase)

1. Go to your Supabase project dashboard → Authentication → Email Templates.
2. Add the following template:

```html
<h2>Magic Link</h2>
<p>Follow this link to login:</p>
<p><a href="{{ .SiteURL }}/auth/confirm?token_hash={{ .TokenHash }}&type=email">Log In</a></p>
```

3. Make sure your **Site URL** and **Redirect URL** are correctly configured:

```
Site URL: https://your-app-url
Redirect URL: https://your-app-url/**
```

---

### 5. Start the development server

```bash
npm run dev
```

Or with yarn:

```bash
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the app running.

---

## Tips for Best Results

* Use clear, close-up images with only one person in the frame.
* Avoid sunglasses, hats, or other accessories.
* Make sure faces are centered and clearly visible.
* Use consistent aspect ratios (e.g., 512x512, 1024x1024) for input images.
* Avoid multiple people in a single image.

Following these steps ensures the AI generates high-quality headshots.

---

## Optional Features

* **Email notifications** when headshots are ready (requires Resend API key).
* **Credit-based billing** using Stripe (optional).
* Can be adapted for other AI use-cases like avatars, product shots, or illustrations.

---

## Contributing

Contributions are welcome!

* Open an issue for suggestions or improvements.
* Create a new branch and open a pull request to the `dev` branch.

---


