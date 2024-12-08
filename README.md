# NextAuth session check always fails

This repository demonstrates a common issue when using NextAuth.js for authentication in Next.js API routes. The problem is that the session check always fails, even when the user is logged in.

## Problem

The provided `api/protected.js` code uses `unstable_getServerSession` to check if a user is authenticated. However, it might always return `null`, even if the user is logged in. This might happen due to several reasons, including incorrect configuration or missing middleware.

## Solution

The solution, found in `api/protected.solution.js`, addresses this issue by ensuring that the API route is properly configured and the `unstable_getServerSession` is used correctly.