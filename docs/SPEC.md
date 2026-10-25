# Rental Room Management System

## 1. Project Overview

The Rental Room Management System is a web application that helps tenants find rooms for rent and allows landlords to manage room listings and rental requests. Tenants can browse available rooms, search for rooms within their budget, submit rental requests, and track their rental status. Landlords can create, view, update, and delete room listings, manage rental requests, and track room availability.

## 2. User Roles

### Tenant

- View available rooms.
- Search and filter rooms by monthly rental price.
- Submit rental requests.
- View their own rental requests.
- Check rental request status.
- View their own rental records.

### Landlord

- Create room listings.
- View and manage their own room listings.
- Update room information and rental prices.
- Delete eligible room listings.
- View rental requests for their rooms.
- Approve or reject rental requests.
- Manage room availability and rental records.

## 3. User Stories and Acceptance Criteria

### US-01: View Available Rooms

As a tenant, I want to view available rooms so that I can find a suitable room to rent.

Acceptance criteria:

- The system displays a list of available rooms.
- Each room displays its title, address, monthly rental price, and availability status.
- Rooms marked unavailable do not appear in the available-room list.
- Selecting a room opens its details.

### US-02: Search and Filter Rooms

As a tenant, I want to search and filter rooms so that I can find rooms within my budget.

Acceptance criteria:

- The tenant can filter rooms by minimum and maximum monthly rental price.
- The system displays rooms that match the selected price range.
- The minimum price cannot be greater than the maximum price.
- The system displays a message when no rooms match the search criteria.

### US-03: Register an Account

As a new user, I want to create an account so that I can access the system.

Acceptance criteria:

- The user can enter their name, email address, and password.
- Required fields cannot be empty.
- The email address must be valid and unique.
- The password is stored as a hash rather than plain text.
- A successfully registered user is assigned a role.

### US-04: Log In to the System

As a registered user, I want to log in so that I can access features permitted for my role.

Acceptance criteria:

- The user can enter their email address and password.
- Valid credentials allow the user to log in.
- Invalid credentials display an error message.
- The system uses JWT authentication to protect restricted pages and API endpoints.
- Users cannot access features that their roles are not permitted to use.

### US-05: Create a Room Listing

As a landlord, I want to add a room listing so that tenants can find my available rooms.

Acceptance criteria:

- Only authenticated landlords can create room listings.
- The landlord can enter the room title, address, and monthly rental price.
- The title and address are required.
- The monthly rental price must be greater than zero.
- A successfully created room is saved to the database and appears in the room list.

### US-06: Update and Delete Room Listings

As a landlord, I want to update or delete my room listings so that I can keep my room information accurate.

Acceptance criteria:

- The landlord can update the details and monthly rental price of their own rooms.
- Updated information is validated before being saved.
- The landlord can delete eligible room listings.
- The system prevents unauthorized users from modifying or deleting another landlord's rooms.
- The system handles rooms with existing rental records safely.
- Changes are reflected in the room list.

### US-07: Submit a Rental Request

As a tenant, I want to submit a rental request so that I can request to rent an available room.

Acceptance criteria:

- Only authenticated tenants can submit rental requests.
- The tenant can select an available room and submit a request.
- The system associates the request with the correct tenant and room.
- The request is stored in the database with a default status of Pending.
- The tenant can view the request and its current status.
- The system prevents requests for unavailable rooms.

### US-08: Manage Rental Requests

As a landlord, I want to review and manage rental requests so that I can organize room rentals.

Acceptance criteria:

- The landlord can view rental requests for their own rooms.
- Each request displays the tenant, room, submission date, and request status.
- The landlord can approve or reject eligible requests.
- The updated request status is saved to the database.
- The system prevents unauthorized users from managing another landlord's rental requests.
- The room's availability is updated appropriately when a rental is confirmed.

## 4. Main Entities

- **User:** Stores user information, email address, password hash, and role.
- **Room:** Stores room information, address, monthly rental price, availability status, and landlord.
- **Rental:** Stores rental requests and rental records, including the associated tenant, room, dates, and status.

## 5. Project Scope

The first version focuses on room listings, room search and filtering, rental requests, and rental management. Authentication, role-based access control, database integration, backend validation, pagination, and automated testing will be implemented progressively during the semester using Vue 3, TypeScript, NestJS, PostgreSQL, and Prisma.
