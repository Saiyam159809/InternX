# InternX merge result

Base:
- `InternX_recruiter_feature_FIXED.zip` was used as the base because it contains the existing recruiter models, migrations, APIs and frontend.
- `InternX_recruiter_feature_COMPLETE.zip` was inspected for comparison; the fixed package was retained as the safer base.

Student/admin additions:
- Student registration/login
- Student profile
- Education, skills, projects
- Supabase resume upload/management
- Student opportunity browsing/search/filter/details
- Internal/external application tracking
- Application history/status/withdrawal
- Interview viewing
- Notifications/read state
- Admin login
- Admin user management
- Admin company management
- Admin opportunity management/moderation

Recruiter behavior was preserved except for the necessary notification side effect when a recruiter changes an application status.

Database:
- Existing recruiter migrations are retained.
- `accounts/migrations/0002_student_features.py` adds only student-side schema.
- No existing recruiter migration was rewritten.

Required environment:
- `SUPABASE_URL`
- `SUPABASE_SERVICE_ROLE_KEY`
- `SUPABASE_RESUME_BUCKET` (default: `resumes`)

Do not expose the Supabase service-role key to frontend JavaScript.
