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
│  │  │  ├─ index.ts
│  │  │  ├─ server.ts
│  │  │  ├─ config/
│  │  │  │  ├─ env.ts
│  │  │  │  └─ logger.ts
│  │  │  ├─ db/
│  │  │  │  └─ connect.ts
│  │  │  ├─ middleware/
│  │  │  │  ├─ auth.ts
│  │  │  │  ├─ error.ts
│  │  │  │  └─ roles.ts
│  │  │  ├─ models/
│  │  │  │  ├─ User.ts
│  │  │  │  ├─ Gig.ts
│  │  │  │  ├─ Escrow.ts
│  │  │  │  ├─ Transaction.ts
│  │  │  │  ├─ Dispute.ts
│  │  │  │  └─ Kyc.ts
│  │  │  ├─ routes/
│  │  │  │  ├─ auth.routes.ts
│  │  │  │  ├─ gigs.routes.ts
│  │  │  │  ├─ escrow.routes.ts
│  │  │  │  ├─ wallet.routes.ts
│  │  │  │  ├─ kyc.routes.ts
│  │  │  │  └─ admin.routes.ts
│  │  │  ├─ controllers/
│  │  │  │  ├─ auth.controller.ts
│  │  │  │  ├─ gigs.controller.ts
│  │  │  │  ├─ escrow.controller.ts
│  │  │  │  ├─ wallet.controller.ts
│  │  │  │  ├─ kyc.controller.ts
│  │  │  │  └─ admin.controller.ts
│  │  │  ├─ services/
│  │  │  │  ├─ payment.ts          # adapter pattern (mock: paystack/flutterwave/stripe)
│  │  │  │  ├─ sms.ts              # stub for SMS/USSD alerts
│  │  │  │  └─ ai.ts               # skill matching stub
│  │  │  ├─ utils/
│  │  │  │  ├─ crypto.ts
│  │  │  │  └─ response.ts
│  │  │  └─ upload/
│  │  │     └─ multer.ts
│  │  └─ tsconfig.json
│  └─ web/                # React + Vite + Tailwind front‑end
│     ├─ package.json
│     ├─ index.html
│     └─ src/
│        ├─ main.tsx
│        ├─ App.tsx
│        ├─ lib/api.ts
│        ├─ lib/auth.ts
│        ├─ lib/store.ts
│        ├─ components/
│        │  ├─ Nav.tsx
│        │  ├─ Protected.tsx
│        │  ├─ GigCard.tsx
│        │  ├─ WalletWidget.tsx
│        │  └─ Rating.tsx
│        ├─ pages/
│        │  ├─ Landing.tsx
│        │  ├─ Register.tsx
│        │  ├─ Login.tsx
│        │  ├─ Feed.tsx
│        │  ├─ GigDetails.tsx
│        │  ├─ PostGig.tsx
│        │  ├─ Wallet.tsx
│        │  ├─ Kyc.tsx
│        │  ├─ Disputes.tsx
│        │  └─ Admin.tsx
│        ├─ styles/index.css
│        └─ vite-env.d.ts
└─ docs/
   └─ api.http           # REST examples for VSCode REST Client