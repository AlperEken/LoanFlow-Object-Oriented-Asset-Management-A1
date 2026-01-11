# LoanFlow: Object-Oriented Asset Management

## Key Features

LoanFlow is an advanced asset management engine designed to coordinate the complex lifecycle of resource distribution and membership-based lending. The system facilitates sophisticated member registration and tracking, allowing for the granular management of a lending community alongside a comprehensive inventory of loanable products. At its core, the platform automates the loan and return workflows, providing real-time statistics on availability and borrower status. Integrated analytical tools offer organisers immediate oversight of the system's throughput, ensuring that the movement of assets is transparent, efficient, and easily adjustable through a dynamic GUI.

## Technical Implementation

This application is engineered using a robust Model-View-Controller (MVC) architecture, optimized for high modularity and separation of concerns. Developed in Java, the system moves beyond monolithic logic by distributing responsibilities across specialized domain managers—including `MemberManager`, `ProductManager`, and `LoanItemManager`—which handle specific data sets with dedicated encapsulation. A unique aspect of this implementation is the use of task-based command objects, such as `LoanTask` and `ReturnTask`, which encapsulate business logic into discrete units for better maintainability and modular execution. The user interface is built with `javax.swing`, utilizing a multi-panel layout to provide a professional and responsive desktop experience.

## Challenges & Reflection

Transitioning to a multi-manager architecture presented significant technical hurdles, primarily centered on synchronizing state transitions across disparate domain entities. Developing the logic to link a `Member` to a `Product` through a `LoanItem` required a deep understanding of object associations and data persistence within a modular environment. Furthermore, implementing the task-based architecture was a pivotal design decision that moved the complexity away from the UI controller, allowing for more robust error handling and cleaner event management. This project ultimately served as a vital exercise in managing concurrent data states and refined the developer's ability to architect systems where logic is as modular as the assets they manage.

## Getting Started

To execute the LoanFlow system on your local machine, ensure the JDK is installed and use the following terminal commands:

```bash
# Navigate to the source root
cd A1-d18ea5e3f6495c5c01ecf3514594c064383bc265/src

# Compile the package modules
javac loanSysControllers/*.java loanSysModel/*.java loanSysView/*.java

# Run the system via the main entry point
java loanSysControllers.MainProgram
```
*Author: Alper Eken Course: Concurrent Programming Semester: Spring 2025 (VT25)*
