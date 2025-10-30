Medanior MedLedger: Jaringan Rekam Medis Semua Rumah
Sakit

Medanior MedLedger adalah infrastruktur buku besar terdistribusi
yang dirancang untuk revolusi RME (Rekam Medis Elektronik) di
Indonesia. Dibangun di atas private Solana cluster yang sangat
cepat, tujuan utamanya adalah memastikan semua rumah sakit dalam
jaringan dapat mengakses jejak rekam medis dan tindakan pasien
secara instan, menghilangkan kebutuhan akan proses manual dan
tanda tangan fisik yang menghambat kasus darurat.
Integritas tindakan klinis dijamin oleh tanda tangan
kriptografis non-repudiable dari DID praktisi, yang dicatat
on-chain.

Koin Jaringan: MEDAR (Medical Audit & Reward Token).
Quickstart: Menjalankan Demo Lokal
Prasyarat: Rust, Solana Tool Suite, Anchor Framework (avm
install/use), Node.js, Docker, Terraform, Helm.

1. Clone & Konfigurasi:
Bash
git clone <url-repositori-ini>
cd smart-contracts/anchor
# Pastikan Anchor.toml dikonfigurasi dengan ID program lokal

2. Bangun & Deploy Smart Contracts:
Bash
anchor build
# Memulai localnet dan deploy 4 program inti
anchor deploy --provider.cluster localhost

3. Jalankan Infrastruktur Pendukung:
Bash
# Skrip ini menjalankan validator lokal, database off-chain
(Prisma/Postgres)
./scripts/run-full-stack.sh

4. **Jalankan Backend API (Akses Universal):**bash
cd../../api
npm install
npm run dev # API berjalan di http://localhost:3000 (titik akses
FHIR/DID)
```
Visi Inti
● Akses Instan: Semua tindakan medis terhubung dan dapat
diakses real-time oleh seluruh RS konsorsium.
● Zero-Signature Workflow: Tanda tangan fisik diganti dengan
bukti kriptografis on-chain (non-repudiable).
● Zero-PII On-Chain: Data medis sensitif tidak pernah menyentuh
ledger untuk kepatuhan UU PDP.
~Medanior
