import { authMiddleware } from "@clerk/nextjs";

export default authMiddleware({
  
  publicRoutes: [
    '/',
    '/events/:id',
    '/api/webhook/clerk',
    '/api/webhook/stripe',
    '/api/uploadthing',
    "/favicon.ico",
    "/assets/images/logo.svg",
    "/assets/icons/calendar.svg",
    "/assets/icons/dollar.svg",
    "/assets/icons/upload.svg"
  ],
  ignoredRoutes: [
    '/api/webhook/clerk',
    '/api/webhook/stripe',
    '/api/uploadthing',
    "/assets/images/hero.png",
    "/assets/images/dotted-pattern.png",
    "/assets/icons/calendar.svg",
    "/assets/icons/dollar.svg",
    "/assets/icons/upload.svg"
  ]

});

export const config = {
  matcher: ["/((?!.+.[w]+$|_next).*)", "/", "/(api|trpc)(.*)"],
};