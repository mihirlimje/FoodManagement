# Food Management ServiceNow Application

## Overview
This is a comprehensive Food Management System built on ServiceNow platform for tracking meals, inventory, and nutrition information.

## Application Details
- **Name**: Food Management
- **Scope**: x_951571_food_mgt
- **Prefix**: food
- **Version**: 1.0.0

## Features
- Meal tracking and management
- Food inventory management
- Nutrition information tracking
- Category-based meal organization (Breakfast, Lunch, Dinner, Snack)

## Tables
1. **Meal** (x_951571_food_mgt_meal)
   - Number (auto-generated)
   - Meal Name
   - Category (choice field)

2. **Food Inventory** (x_951571_food_mgt_inventory)
   - For tracking food items and quantities

## Installation
1. Import the application files into your ServiceNow instance
2. Activate the application
3. Assign appropriate user roles
4. Configure access controls as needed

## File Structure
```
FoodManagement/
├── sys_app.xml                    # Application definition
├── manifest.xml                   # Application manifest
├── README.md                      # This file
└── update/                        # Update set files
    ├── sys_db_object_*.xml        # Table definitions
    ├── sys_dictionary_*.xml       # Field definitions
    ├── sys_choice_*.xml           # Choice list definitions
    └── ...                        # Additional configuration files
```

## Getting Started with Git
To clone this project into your GitHub repository:

```bash
# Navigate to your projects directory
cd C:\Users\mihir.limje_jadeglob\CascadeProjects

# Clone your existing repository
git clone https://github.com/mihirlimje/FoodManagement.git

# Navigate into the cloned repository
cd FoodManagement

# Create and switch to the 'food' branch
git checkout -b food

# Add the Food Management ServiceNow application files
git add .

# Commit the changes
git commit -m "Add Food Management ServiceNow application with complete structure"

# Push the new branch to GitHub
git push origin food
```

## Import into ServiceNow

### Method 1: Application Import
1. Download the files from the `food` branch in your GitHub repository
2. In your ServiceNow instance, navigate to **System Definition > Applications**
3. Click **Import Application**
4. Upload the `app.xml` file
5. Follow the import wizard to install the application

### Method 2: Update Set Import
1. Download the files from the `food` branch in your GitHub repository
2. In your ServiceNow instance, navigate to **System Update Sets > Retrieved Update Sets**
3. Click **Import Update Set from XML**
4. Upload the `update_set.xml` file
5. Preview and commit the update set
6. Activate the Food Management application
7. Assign the `x_951571_food_mgt.user` role to users who need access

### Method 3: Individual XML Import
1. Download the files from the `food` branch in your GitHub repository
2. In your ServiceNow instance, navigate to **System Import Sets > Import XML**
3. Upload all XML files from the `update` directory
4. Preview and commit the update set
5. Activate the Food Management application
6. Assign the `x_951571_food_mgt.user` role to users who need access

## Development Notes
- All table and field names follow ServiceNow naming conventions
- Application uses standard ServiceNow security model
- Forms and lists can be customized as needed
- Additional business rules and client scripts can be added for enhanced functionality
