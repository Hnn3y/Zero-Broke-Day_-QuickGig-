# Zero-Broke-Day_-QuickGig-


zero-broke-days/
├─ README.md
├─ .env.example
├─ package.json           # workspace root
├─ pnpm-workspace.yaml    # or yarn/npm - update scripts accordingly
├─ apps/
│  ├─ api/                # Express + Mongoose backend
│  │  ├─ package.json
│  │  ├─ src/
│  │  │  ├─ index.js
│  │  │  ├─ server.js
│  │  │  ├─ config/
│  │  │  │  ├─ env.js
│  │  │  │  └─ logger.js
│  │  │  ├─ db/
│  │  │  │  └─ connect.js
│  │  │  ├─ middleware/
│  │  │  │  ├─ auth.js
│  │  │  │  ├─ error.js
│  │  │  │  └─ roles.js
│  │  │  ├─ models/
│  │  │  │  ├─ User.js
│  │  │  │  ├─ Gig.js
│  │  │  │  ├─ Escrow.js
│  │  │  │  ├─ Transaction.js
│  │  │  │  ├─ Dispute.js
│  │  │  │  └─ Kyc.js
│  │  │  ├─ routes/
│  │  │  │  ├─ auth.routes.js
│  │  │  │  ├─ gigs.routes.js
│  │  │  │  ├─ escrow.routes.js
│  │  │  │  ├─ wallet.routes.js
│  │  │  │  ├─ kyc.routes.js
│  │  │  │  └─ admin.routes.js
│  │  │  ├─ controllers/
│  │  │  │  ├─ auth.controller.js
│  │  │  │  ├─ gigs.controller.js
│  │  │  │  ├─ escrow.controller.js
│  │  │  │  ├─ wallet.controller.js
│  │  │  │  ├─ kyc.controller.js
│  │  │  │  └─ admin.controller.js
│  │  │  ├─ services/
│  │  │  │  ├─ payment.js          # adapter pattern (mock: paystack/flutterwave/stripe)
│  │  │  │  ├─ sms.js              # stub for SMS/USSD alerts
│  │  │  │  └─ ai.js               # skill matching stub
│  │  │  ├─ utils/
│  │  │  │  ├─ crypto.js
│  │  │  │  └─ response.js
│  │  │  └─ upload/
│  │  │     └─ multer.js
│  │  └─ jsconfig.json
│  └─ web/                # React.js + Vite + Tailwind frontend
│     ├─ package.json
│     ├─ index.html
│     └─ src/
│        ├─ main.jsx
│        ├─ App.jsx
│        ├─ lib/api.js
│        ├─ lib/auth.js
│        ├─ lib/store.js
│        ├─ components/
│        │  ├─ Nav.jsx
│        │  ├─ Protected.jsx
│        │  ├─ GigCard.jsx
│        │  ├─ WalletWidget.jsx
│        │  └─ Rating.jsx
│        ├─ pages/
│        │  ├─ Landing.jsx
│        │  ├─ Register.jsx
│        │  ├─ Login.jsx
│        │  ├─ Feed.jsx
│        │  ├─ GigDetails.jsx
│        │  ├─ PostGig.jsx
│        │  ├─ Wallet.jsx
│        │  ├─ Kyc.jsx
│        │  ├─ Disputes.jsx
│        │  └─ Admin.jsx
│        ├─ styles/index.css
│        └─ vite-env.d.ts
└─ docs/
   └─ api.http           # REST examples for VSCode REST Client