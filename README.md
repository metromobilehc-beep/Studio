# Metro Training Studio

Browser-based screen recording tool for clinical staff training.
Stores videos in Supabase Storage, metadata in Supabase DB.

## Setup

### 1. Run SQL in Supabase
Go to supabase.com → your project → SQL Editor → paste contents of `supabase-setup.sql` → Run.

### 2. Supabase Storage Bucket
- Go to Storage → New Bucket
- Name: `training-videos`
- Set to **Public**

### 3. Deploy to GitHub Pages
```
git init
git add .
git commit -m "Metro Training Studio"
gh repo create metro-training-studio --public
git push -u origin main
```
Then in repo Settings → Pages → Source: main branch / root.

## Usage

1. Open the tool URL
2. Click **Record** tab
3. Click **Start** → HIPAA checklist appears → confirm → screen share dialog opens
4. Draw blur zones over any PHI areas before/after recording
5. Fill in title, category, description
6. Click **Generate Script & Save** → uploads to Supabase, appears in Library instantly

## Supabase Config
- Project: zxserlkhwkfoqiepurdr
- Bucket: training-videos
- Tables: training_videos, hipaa_checklist_log
