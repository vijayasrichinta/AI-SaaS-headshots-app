# 👨‍💼 Headshot AI - Professional AI Headshots

[Live Demo](https://headshots-starter.vercel.app/)  

Headshot AI is an AI-powered app that generates professional headshots in minutes. Upload a few photos, and the app creates high-quality AI headshots automatically.  

This project is open-source and serves as a starting point for developers and makers to build AI applications quickly.

---

## 🚀 Live Demo

[![Headshot AI Demo](https://raw.githubusercontent.com/vijayasrichinta/headshots-starter-clone/main/public/new-demo.png)](https://headshots-starter.vercel.app/)

Try the app instantly without installation. Upload a few photos, then generate headshots in seconds.

---

## 🔧 How It Works

The app is powered by:

- **Next.js** – Frontend and landing page framework
- **Supabase** – Database and authentication
- **Astria API** – AI model inference
- **Resend (Optional)** – Email notifications when headshots are ready
- **Stripe (Optional)** – Billing and credits for premium usage
- **Shadcn + Tailwind CSS** – UI and styling
- **Vercel** – Deployment

---

## 📸 Example Results

**Good Results:**

[![Good Results](https://raw.githubusercontent.com/vijayasrichinta/headshots-starter-clone/main/public/good_results.png)](https://headshots-starter.vercel.app/)

**Avoid Multiple Faces in Input Images:**

[![Multiple Faces Warning](https://raw.githubusercontent.com/vijayasrichinta/headshots-starter-clone/main/public/multiple_faces.png)](https://headshots-starter.vercel.app/)

---

## ⚡ Quick Start (Local Setup)

1. **Clone your repository:**

```bash
git clone {{your-repo-name}}
cd {{your-repo-name}}
````

2. **Install dependencies:**

```bash
npm install
# or
yarn
```

3. **Configure Supabase Magic Link Auth**

In your Supabase dashboard:

* Go to Authentication → Email Templates → Magic Link
* Paste:

```html
<h2>Magic Link</h2>
<p>Follow this link to login:</p>
<p><a href="{{ .SiteURL }}/auth/confirm?token_hash={{ .TokenHash }}&type=email">Log In</a></p>
```

* Configure **Site URL** and **Redirect URLs**:

```
Site URL: https://headshots-starter.vercel.app
Redirect URL: https://headshots-starter.vercel.app/**
```

4. **Setup `.env.local`**

Add the following variables:

```text
NEXT_PUBLIC_ASTRIA_API_KEY=your_astria_api_key
APP_WEBHOOK_SECRET=any_url_friendly_secret
DEPLOYMENT_URL=https://your-deployed-url
BLOB_READ_WRITE_TOKEN=your_vercel_blob_token
NEXT_PUBLIC_ANNOUNCEMENT_ENABLED=true
NEXT_PUBLIC_ANNOUNCEMENT_MESSAGE="Your announcement here"
STRIPE_SECRET_KEY=your_stripe_secret_key
STRIPE_WEBHOOK_SECRET=your_stripe_webhook_secret
NEXT_PUBLIC_STRIPE_IS_ENABLED=false
```

5. **Start development server:**

```bash
npm run dev
# or
yarn dev
```

Visit [http://localhost:3000](http://localhost:3000) to see the running app.

---

## 💡 Tips for Best AI Results

* Use **close-up face photos** with one person per frame
* Avoid sunglasses, hats, or accessories
* Crop and center the face if necessary
* Keep all sample images **1:1 aspect ratio** (e.g., 512x512, 1024x1024)
* Add `"double torso, totem pole"` to the negative prompt to reduce distortion

---

## 🖼 Additional Use-Cases

Headshot AI can be adapted for:

* **AI Avatars**
  ![Anime Demo](https://raw.githubusercontent.com/vijayasrichinta/headshots-starter-clone/main/public/anime.png)

  * Anime portraits, stylized avatars

* **Pet Portraits**
  ![Pet Demo](https://raw.githubusercontent.com/vijayasrichinta/headshots-starter-clone/main/public/pet.png)

* **Product Shots & Icons**
  ![Product Demo](https://raw.githubusercontent.com/vijayasrichinta/headshots-starter-clone/main/public/products.png)
  ![Icon Demo](https://raw.githubusercontent.com/vijayasrichinta/headshots-starter-clone/main/public/icons.png)

& more!

---

## 📝 Contributing

Contributions are welcome!

* Open an issue for suggestions or improvements
* Create a new branch and open a pull request targeting `dev`

---

## 📚 Resources & Support

* **Support Email:** [support@example.com](mailto:support@example.com)
* **Documentation:** [Headshot AI Docs](https://headshots-starter.vercel.app/)
