# Airbnb Clone — Features & Functionalities

This folder documents the backend features and functions required for the Airbnb Clone backend and includes a diagram (features-overview.png) that visualizes component interactions.

---

## 1. User Management
- *Register*: Create user accounts with email validation.
- *Login/Logout*: Secure authentication (JWT).
- *Profile management*: Update user details (name, phone, photo).
- *Roles*: Guest, Host, Admin.
- *Account lifecycle*: soft-delete or deactivate accounts.

## 2. Property Management
- *CRUD for listings*: Hosts can create, read, update, delete properties.
- *Property attributes*: title, description, location, amenities, price per night, images.
- *Search & filter*: location, price range, availability, rating, amenities.
- *Image upload*: stored in cloud (e.g., S3) with links in DB.

## 3. Booking System
- *Create booking*: check availability, reserve dates.
- *Modify / Cancel bookings*: policy-based rules.
- *Booking statuses*: pending, confirmed, canceled, completed.
- *Booking history*: for guests and hosts.
- *Price calculation*: nightly rate × nights + fees/taxes.

## 4. Payment Processing
- *Payment integration*: Stripe / PayPal / others.
- *Payment flow*: tokenization, charge, store transaction record.
- *Refunds*: support refund logic and reversal.
- *Security*: PCI-compliant handling (delegate to provider).

## 5. Reviews & Ratings
- *Post-review*: post-review after completed booking.
- *Aggregated rating*: compute average rating per property.
- *Moderation*: ability to flag or remove abusive content.

## 6. Messaging System
- *Direct messaging*: between guests and hosts.
- *Notifications*: email/push for new messages and booking updates.
- *Conversation history*: stored in DB.

## 7. Admin Panel
- *User management*: suspend/activate users.
- *Content moderation*: remove listings or reviews.
- *Reporting*: system usage and financial reports.

## 8. Security & Compliance
- *Authentication*: JWT, refresh tokens.
- *Authorization*: role-based access controls (RBAC).
- *Input validation*: server-side validation.
- *Rate limiting & DDoS protection*.
- *Encryption*: TLS in transit; encrypted secrets.

## Diagram
See features-diagram.png for the visual component map showing interactions between Users, Properties, Bookings, Payments, Messaging, and Admin services.
