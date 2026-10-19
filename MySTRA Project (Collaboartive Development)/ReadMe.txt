Core Functionality that i did: 

Isolated OTP System: Uses separate OTP variables (currentGeneratedOTP, currentForgotOTP, currentLegacyOTP) to prevent cross-flow state collisions.

User Registration: Features live password strength validation and two-step OTP email verification before creating Supabase Auth accounts.

Password Reset: Generates expiring OTPs stored in Supabase, verifies codes, and executes a secure RPC function (reset_user_password) with a 30-second resend cooldown.

Legacy Account Migration: Validates legacy credentials (Email, SSM, License No), verifies ownership via OTP, and automatically creates corresponding user profiles, properties, and compliance documents.

UI Utilities: Auto-advancing OTP input boxes, password visibility toggles, and async button loading states to block double submissions.

In general, i was in charge of login, register, legacy account migration, and legacy database ETL ( Extract, Transform, Load) which simulates the legacy system data being ETL into current system Mystra. 

