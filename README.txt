NANUS KWASU V4 — MAIN WEBSITE + CMS FOUNDATION

1. index.html = main public website.
2. election.html = integrated election portal.
3. admin.html = Supabase login + basic news/events dashboard.
4. config.js = put ONLY Supabase URL + anon/publishable key here.
5. cms_schema.sql = content tables + RLS policies.

Important:
- Never put the Supabase service_role/secret key in browser files.
- The CMS policies in this starter allow any authenticated user to manage content they own. Before giving accounts to multiple people, replace them with a dedicated admin/role system.
- The election database/RPC from V2 should remain separate and more restricted than normal content management.
- Real election activation should be done only by the authorized Electoral Committee.

Setup:
A) Create/configure your Supabase project.
B) Run cms_schema.sql in Supabase SQL Editor.
C) Create an admin user in Supabase Authentication.
D) Put the project URL and anon/publishable key in config.js.
E) Open admin.html and sign in.
F) Add a published news post or event; refresh the public index.html to see it.
