# GuardianLink

**GuardianLink** is a comprehensive, JavaFX-based NGO Management System designed to streamline operations for non-governmental organizations. The application features a robust role-based architecture, facilitating efficient management of children, caregivers, donors, and administrative tasks.

## Key Features

*   **Role-Based Access Control:** Secure authentication with distinct interfaces and permissions for:
    *   **System Admin:** Global system overview and user management.
    *   **Organization Admin (OrgAdmin):** Organization-specific operations, child records, and expense tracking.
    *   **Caregiver:** Child assignment tracking, notifications, and daily updates.
    *   **Donor:** Sponsorship management and donation tracking.
    *   **Support:** Helpdesk, FAQ management, and user assistance.
*   **Child & Caregiver Management:** Link children to specific caregivers, track medical and educational access, and manage assignments.
*   **Real-time Notifications:** In-app notification system for caregiver assignments and important updates.
*   **Database Integration:** Lightweight, persistent local storage using SQLite.

##  Technology Stack

*   **Language:** Java 21
*   **UI Framework:** JavaFX 21.0.2
*   **Database:** SQLite (via JDBC)
*   **Build Tool:** Apache Maven 3.x

##  Getting Started

### Prerequisites

*   **Java Development Kit (JDK) 21** or higher
*   **Apache Maven** installed and configured in your system path
*   *(Optional)* An IDE like IntelliJ IDEA, Eclipse, or VS Code with Java/JavaFX support.

### Installation & Setup

1. **Clone the repository** (if not already downloaded):
   ```bash
   git clone <repository_url>
   cd GuardianLink
   ```

2. **Build the project** using Maven:
   ```bash
   mvn clean install
   ```

3. **Run the application:**
   You can run the application directly through the Maven JavaFX plugin:
   ```bash
   mvn javafx:run
   ```
   *Alternatively, you can run the `app.Launcher` main class directly from your IDE.*

## Database Configuration

The application uses an embedded SQLite database (`guardianlink.db`).
*   The database file is automatically created in the root directory upon startup if it doesn't exist.
*   Schema definitions and initial test data can be found in the provided `.sql` files (e.g., `database_schema.sql`, `insert_test_caregivers_and_children.sql`).

## Project Structure

*   `src/main/java/app/` - Contains the main application entry point (`Launcher.java` / `Main.java`).
*   `src/main/java/controller/` - JavaFX controller classes handling UI logic for different user roles (`AuthController`, `AdminController`, `OrgAdminController`, etc.).
*   `src/main/java/model/` - Data entities and business logic representations.
*   `src/main/java/util/` - Utility classes (e.g., `ContactValidator`, `FAQs`).
*   `src/main/resources/` - JavaFX FXML files and CSS stylesheets.

## Contributing

This project is currently closed for external contributions. For internal development, please ensure all new features adhere to the existing MVC pattern and maintain backwards compatibility with the current SQLite schema.
