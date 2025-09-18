## **Authentication & Profile**

### **1.1 Registration**

**As a** new user, I want to register an account so that I can access booking.  
**Acceptance criteria:**

* *Given*: I entered a valid email and password

* *When*: I click "Sign Up"

* *Then*: an account is created and I receive a confirmation email

  ### **1.2 Login**

  **As a** user, I want to log in to the system so that I can access my dashboard.  
  **Acceptance criteria:**

* *Given*: my account is verified

* *When*: I enter email/password

* *Then*: I am redirected to my profile

  ### **1.3 Profile Management**

  **As a** user, I want to edit my information (name, photo, contacts) so that my profile stays up-to-date.  
  **Acceptance criteria:**

* *Given*: I am in my profile

* *When*: I change name, photo, or contacts and click "Save"

* *Then*: my information is updated and displayed in the profile

  ---

  ## **Booking & Space Management**

  ### **2.1 View Available Spaces**

  **As a** user, I want to see available rooms/workspaces so that I can choose where to work.  
  **Acceptance criteria:**

* *Given*: I opened the space search page

* *When*: the system loads a list of available rooms and workspaces

* *Then*: I see the up-to-date availability information

  ### **2.2 Filtering & Search**

  **As a** user, I want to filter spaces by type (room, open space, conference hall) so that I can quickly find what I need.  
  **Acceptance criteria:**

* *Given*: I am in the list of spaces

* *When*: I select a filter (space type) or enter a search query

* *Then*: the system shows only spaces matching the criteria

  ### **2.3 Book a Space**

  **As a** user, I want to book a workspace for a specific date and time so that it is guaranteed to be mine.  
  **Acceptance criteria:**

* *Given*: I selected a free space and date/time

* *When*: I click "Book"

* *Then*: the space is reserved for me and I see a booking confirmation


  ### **2.4 Cancel Booking**

  **As a** user, I want to cancel a booking so that the space becomes available if my plans change.  
  **Acceptance criteria:**  
* *Given*: I have an active booking

* *When*: I click "Cancel"

* *Then*: the booking is removed and the space becomes available to others

  ### **2.5 View My Calendar**

  **As a** user, I want to see all my bookings in a calendar so that I can plan my work time.  
  **Acceptance criteria:**

* *Given*: I opened the calendar

* *When*: the system loads my bookings

* *Then*: I see all my bookings as events on the selected dates

  ---

  ## **Notifications**

  ### **3.1 Booking Confirmation Email**

  **As a** user, I want to receive a confirmation email after booking so that I have proof.  
  **Acceptance criteria:**

* *Given*: I booked a space

* *When*: the booking is successfully created

* *Then*: I receive a confirmation email

  ---

  ### **3.2 Reminder**

  **As a** user, I want to receive a reminder 24 hours before my booking so that I don’t forget.  
  **Acceptance criteria:**

* *Given*: I have an active booking

* *When*: 24 hours remain before the start

* *Then*: I receive an email reminder

  ---

  ## **Roles & Management**

  ### **4.1 Admin Adds New Rooms**

  **As an** administrator, I want to add new rooms and spaces so that the infrastructure is updated.  
  **Acceptance criteria:**

* *Given*: I am logged in as an administrator

* *When*: I enter new room/space data and click "Add"

* *Then*: the new space appears in the list of available spaces


  ### **4.2 Admin Manages Bookings**

  **As an** administrator, I want to see all bookings and be able to edit/delete them to avoid conflicts.  
  **Acceptance criteria:**

* *Given*: I am logged in as an administrator

* *When*: I view the list of all bookings

* *Then*: I can edit or delete them


  ### **4.3 Admin Manages Users**

  **As an** administrator, I want to block or activate users to maintain order. **Acceptance criteria:**  
* *Given*: I am logged in as an administrator

* *When*: I open the user list

* *Then*: I can block or activate accounts

  ---

  ## **Payments**

  ### **5.1 Online Payment**

  **As a** user, I want to pay for a booking with a card so that I immediately secure the space.  
  **Acceptance criteria:**

* *Given*: I have a created booking

* *When*: I select card payment and confirm the transaction

* *Then*: the system charges the amount and marks the booking as paid

  ### **5.2 Payment History**

  **As a** user, I want to see my payment history so that I can track my expenses.  
  **Acceptance criteria:**

* *Given*: I am in the "My Payments" section

* *When*: the system loads the payment history

* *Then*: I see a list of transactions with amounts and dates

  ---

  ## **Analytics & Statistics**

  ### **6.1 Space Utilization**

  **As an** administrator, I want to see room usage statistics to analyze demand.  
  **Acceptance criteria:**

* *Given*: I am logged in as an administrator

* *When*: I open the analytics section

* *Then*: I see statistics on room usage

  ### **6.2 Peak Hours**

  **As an** administrator, I want to see peak booking hours to optimize scheduling.  
  **Acceptance criteria:**

* *Given*: I am logged in as an administrator

* *When*: I view the booking report by time

* *Then*: I see hours with the highest number of bookings

  ---

  ## **Security**

  ### **7.1 Access Control**

  **As a** user, I want access only to my bookings to ensure privacy.  
  **Acceptance criteria:**

* *Given*: I am logged in as a user

* *When*: I view bookings

* *Then*: I see only my own records


  ### **7.2 Admin Privileges**

  **As an** administrator, I want additional functionality that is not available to regular users.  
  **Acceptance criteria:**

* *Given*: I am logged in as an administrator

* *When*: I view the interface and available features

* *Then*: I see extra functionality (user, booking, and room management) not accessible to regular users


  ### **7.3 Sessions**

  **As a** user, I want to be automatically logged out after inactivity to protect my account.  
  **Acceptance criteria:**

* *Given*: I am logged in as a user

* *When*: I remain inactive for a long period

* *Then*: the system automatically logs me out

