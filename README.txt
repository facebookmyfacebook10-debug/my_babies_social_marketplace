MY BABIES COMMUNITY & MARKETPLACE
=================================

A responsive Facebook-inspired customer community and product catalogue built
around the 78 product photographs supplied in the original project. This is an
independent My Babies website and is not operated by or affiliated with Meta.

RUN LOCALLY IN GOOGLE CHROME
----------------------------
1. Extract the ZIP file to a folder.
2. Open the extracted folder.
3. Double-click index.html to open it in Chrome.

For best local development, you may also run a simple static server:
  Python 3:  python -m http.server 8000
Then open http://localhost:8000

WHAT WORKS IN THIS PROJECT
--------------------------
- Responsive desktop, tablet and mobile layouts.
- Home feed, business profile, marketplace, Watch/video-ready page, groups,
  saved products, notifications preview and messaging/contact page.
- All 78 supplied product photos retained in assets/images/.
- Product number search and product details modal.
- WhatsApp enquiry links with product-specific prefilled text.
- Visit Facebook link opens https://www.facebook.com/ in a new tab.
- Optional actual Facebook business page link configuration.
- Local preview post creation, likes, comments, saved products and group joins.
  These are saved in this browser only with localStorage; they are NOT shared
  with other customers and are NOT a production social backend.
- Clear messaging that video files were not present in the supplied ZIP.

CONFIGURATION BEFORE PUBLISHING
-------------------------------
1. Open index.html in a text editor.
2. Find:
     const WHATSAPP_NUMBER = "";
   Set this to the verified business WhatsApp number in international format,
   with digits only. South African example format: 27821234567.
3. Optional: find:
     const FACEBOOK_PAGE_URL = "";
   Paste the actual public My Babies Facebook page URL if available.
4. Verify the supplied business address and all business details before launch.
5. Product names, prices, stock, specifications, variants and reviews were not
   supplied. Product cards intentionally say "Price on request"; do not publish
   prices or claims until the business confirms them.
6. No video files were found in the source ZIP. Add actual licensed video files
   and thumbnails before claiming videos are available.

PUBLISHING A STATIC PREVIEW
---------------------------
GitHub Pages, Netlify or Cloudflare Pages can host this static website:
- Upload the full project, including index.html, style.css and assets/.
- Configure the host to publish the project root.
- Test the live site on desktop and mobile.
A static deployment can demonstrate the UI and WhatsApp contact links, but does
not enable shared multi-customer functionality.

REQUIRED FOR A REAL MULTI-USER PRODUCTION PLATFORM
-------------------------------------------------
This package is a front-end preview, not a complete production backend. Before
inviting real customers to create accounts or exchange private information,
connect and test services for:

- Authentication, account recovery, session security and account deletion.
- Shared database for profiles, posts, comments, reactions, follows, groups,
  product catalogue, saved items and notifications.
- Object/media storage for image and video uploads, thumbnails and streaming.
- Private real-time messaging and delivery/read states.
- Admin-only dashboard, role-based access controls and audit records.
- Server-side upload validation, file-size/type limits, abuse reporting,
  moderation tools, spam/rate limiting and privacy controls.
- Backups, monitoring, HTTPS, privacy policy, terms and data-retention rules.

Recommended implementation choices include a managed backend such as Supabase
(Postgres + Auth + Storage + row-level security) or an equivalent secure stack.
Configure credentials only in server-side environment variables; never place
service-role secrets in frontend code. The current localStorage preview is not
a substitute for a shared database and must not be represented as live customer
activity.

VIDEO SECTION
-------------
No MP4, WebM or MOV videos were found in the supplied project. The Watch page
therefore shows a labelled empty-state and categories ready for real video
content. For production, store actual video files in a media service and use
proper thumbnails, lazy loading and adaptive streaming where appropriate.

PROJECT FILES
-------------
index.html                 Main responsive app and demo interactions
style.css                  Responsive design system and layouts
assets/images/             The 78 supplied product photographs
assets/original-filenames.txt
                           Original names mapped to the catalogue images
README.txt                 This guide
WHATSAPP-SETUP.txt         WhatsApp configuration reminder

Please test every configured link and business detail before publishing.
