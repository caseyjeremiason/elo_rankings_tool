# ELO Rankings Tool

## Overview

This project aims to develop a Python-based GUI application for automating ELO ranking calculations for combat robot events. The tool provides an intuitive interface for managing fight data, calculating ELO scores, and visualizing rankings.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Architecture](#architecture)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Development Practices](#development-practices)
7. [Contribution Guidelines](#contribution-guidelines)
8. [Project Management](#project-management)
9. [Scalability](#scalability)
10. [Security Considerations](#security-considerations)
11. [Appendix](#appendix)

## Introduction

### Purpose

The ELO Rankings Tool aims to streamline the process of updating and managing ELO rankings for combat robot events. It reduces manual processing, enhances accuracy, and provides valuable insights through data visualization.

### Scope

The tool is developed in Python using Tkinter/CustomTkinter for the GUI and JSON files for data storage. Future scalability includes transitioning to a web application with more robust database systems.

## Features

### Main Screen

- **Add Fight Data**
- **Generate ELO Rankings**
- **Adjust ELO Settings**

### Fight Data Screen

- **Add Individual Fights**: Input fight results manually.
- **Bulk Add Fights**: Import fight results in bulk from CSV or JSON files.
- **Export Fight Data**: Export fight records as CSV files.

### Generate ELO Rankings Screen

- **Generate Rankings**: Process fight data and compute ELO scores.
- **Export Rankings**: Export rankings as CSV files for reporting and analysis.

### Settings Screen

- **Modify Key ELO Parameters**:
  - **K-Factor**: The rate of ranking adjustment after fights.
  - **Starting Rank**: Default initial ranking for new competitors.
  - **Yearly Devaluation Values**: Settings for historical ranking decay over time.

### Data Storage

- All settings, fight records, and ELO save files are stored in JSON format for ease of modification and backup.

## Architecture

### Modular Design

The project follows a modular design, splitting functionality into separate modules:

- `gui.py`: Handles the GUI interface.
- `elo_calculations.py`: Contains ELO ranking logic.
- `data_handler.py`: Manages data input/output.
- `visualizations.py`: Handles data visualization.

### Project Structure

    elo_rankings_tool/
    ├── gui.py
    ├── elo_calculations.py
    ├── data_handler.py
    ├── visualizations.py
    ├── static/             # For CSS files (future web app)
    ├── templates/          # For HTML files (future web app)
    └── app.py              # Main Flask application (future web app)

## Installation

### Prerequisites

- Python 3.x
- Required Python libraries:
  - `tkinter`
  - `customtkinter`
  - `pandas`
  - `matplotlib`
  - `seaborn`

### Installation Steps

1. **Clone the repository**:

       git clone https://github.com/yourusername/elo_rankings_tool.git
       cd elo_rankings_tool

2. **Install required libraries**:

       pip install -r requirements.txt

3. **Run the application**:

       python gui.py

## Usage

### Main Screen

- Navigate through the main screen to add fight data, generate rankings, and adjust settings.

### Fight Data Screen

- **Add Individual Fights**: Manually input fight results.
- **Bulk Add Fights**: Import fight data from CSV or JSON files.
- **Export Fight Data**: Export fight records to CSV files.

### Generate ELO Rankings Screen

- **Generate Rankings**: Calculate ELO scores based on fight data.
- **Export Rankings**: Export the rankings to CSV files for analysis.

### Settings Screen

- Adjust key ELO parameters to customize ranking calculations:
  - **K-Factor**
  - **Starting Rank**
  - **Yearly Devaluation Values**

## Development Practices

### Version Control

- Use Git for version control.
- Follow a branching strategy (e.g., feature branches, develop/main branches).

### Code Style and Linting

- Follow PEP8 coding standards.
- Use linters like `Pylint` or `Flake8`.

### Automated Testing

- Develop unit tests using `unittest` or `pytest`.
- Implement CI/CD pipelines with GitHub Actions or Travis CI.

### Code Reviews

- Conduct code reviews through pull requests.
- Provide constructive feedback and ensure code quality.

## Contribution Guidelines

### How to Contribute

1. **Fork the repository**.
2. **Create a new branch** for your feature or bug fix.
3. **Commit your changes** with clear and descriptive messages.
4. **Push your branch** and create a pull request.

### Code of Conduct

- Be respectful and inclusive.
- Provide constructive feedback.
- Collaborate and communicate effectively.

## Project Management

### Tools

- GitHub Projects for task management.
- Slack or Microsoft Teams for team communication.
- Regular virtual meetings for progress updates.

### Milestones

- Design the UI structure.
- Implement data handling.
- Develop fight data entry functionality.
- Implement ELO calculation logic.
- Create export functions.
- Test and refine the tool.

## Scalability

### Database Transition

- Plan to transition from JSON files to a database system (e.g., SQLite, PostgreSQL) for better scalability.

### Web Application Framework

- Use Flask or Django for developing the web application.

### Performance Monitoring

- Implement performance monitoring tools (e.g., Prometheus, Grafana) for tracking application health.

## Security Considerations

### Authentication and Authorization

- Implement secure authentication mechanisms (e.g., OAuth, JWT).
- Follow best practices for password storage and access control.

### Data Protection

- Ensure data encryption for secure storage and transmission.
- Regularly audit and update dependencies for security vulnerabilities.

## Appendix

### References

- **ELO Rating System**: [Wikipedia](https://en.wikipedia.org/wiki/Elo_rating_system)
- **Python Tkinter Documentation**: [Tkinter](https://docs.python.org/3/library/tkinter.html)
- **CustomTkinter Documentation**: [CustomTkinter](https://customtkinter.readthedocs.io/en/latest/)
