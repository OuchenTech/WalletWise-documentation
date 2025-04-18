![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/hero.png)

---

# WalletWise - Android Expense Tracker App Template

## Table of Contents
1. [Introduction](#1-introduction)
2. [App Structure](#2-app-structure)
3. [Getting Started](#3-getting-started)
4. [Firebase Integration](#4-firebase-integration)
5. [OpenAI Integration](#5-openai-integration)
6. [Customize the App](#6-customize-the-app)
7. [Performance Optimization Techniques](#7-performance-optimization-techniques)
8. [Converting the Kivy App to APK/AAB Using GitHub Actions](#8-converting-the-kivy-app-to-apkaab-using-github-actions)
9. [Troubleshooting Guide](#9-troubleshooting-guide)
10. [Frequently Asked Questions (FAQ)](#10-frequently-asked-questions-faq)
11. [Support and Contact](#11-support-and-contact)
12. [License](#12-license)

## 1. Introduction

### 1.1 Overview

**WalletWise** is a **production-ready, modular expense tracker template** built with Python and Kivy, designed to help developers quickly launch a feature-rich personal finance app.

The template includes:
- **User authentication**
- **Transaction management**
- **Data visualization**
- **AI financial assistant**
- **Customizable UI**

Built with **Firebase** integration for real-time data sync, **WalletWise** serves as a fully functional foundation that can be extended or rebranded for various use cases.

### 1.2 Purpose & Target Audience

This template is designed for developers looking to launch their own expense tracking application without building from scratch. It's particularly suited for:
- **Developers** creating MVP expense tracker apps
- **Startups** needing a budget-friendly financial app solution
- **Educators** teaching mobile app development with Python/Kivy
- **Freelancers** offering white-label finance apps to clients

The end-users of the app will benefit from a simple yet powerful solution to manage their finances, gain insights into spending habits, and improve budgeting decisions.

**Key advantages**:

✅ Reduces development time by **80+%** with pre-built core features

✅ Firebase Auth & DB Connected

✅ AI Assistant for Personal Finance

✅ Complete Source Code & Assets

✅ Optimized performance 

✅ Scalable architecture (separate UI, logic, and data)

✅ Template-ready design (easy customization of colors, fonts, assets and widgets)

### 1.3 Technologies Used

The application leverages several key technologies:
- **Python**: Core programming language (v3.9+)
- **Kivy/KivyMD**: UI framework for cross-platform applications
- **Firebase**: Backend services including authentication and database
- **OpenAI API**: AI-powered insights and natural language processing

[Download Now!](https://ko-fi.com/shop/settings?src=sidemenu&productType=0)

## 2. App Structure

This section provides a detailed breakdown of the application's file structure, explaining the purpose and functionality of each key file and component.

### 2.1 Files Map

Below is a detailed breakdown of the application's file structure:

```
WalletWise/
├── main.py                  
├── main.kv                  
├── .github/                 
│   └── workflows/
│       └── build.yml 
├── buildozer.spec          
├── icon.png                 
├── presplash.png            
├── assets/                  
│   ├── fonts/               
│   └── images/              
│       ├── icons/           
│       └── avatar/          
├── libs/                    
│   ├── authentication.py    
│   ├── user.py              
│   ├── config.py            
│   ├── utils.py             
│   └── ai_finance_assistant.py  
└── app/                     
    ├── screens/             
    │   ├── loginscreen/     
    │   ├── signupscreen/
    │   ├── forgotpasswordscreen/
    │   ├── navigationscreen/    
    │   ├── homescreen/      
    │   ├── transactionscreen/   
    │   ├── statisticscreen/ 
    │   ├── profilescreen/   
    │   ├── addtransactionscreen/    
    │   ├── aiscreen/        
    │   ├── changeavatarscreen/  
    │   ├── changenamescreen/    
    │   ├── changecurrencyscreen/    
    │   └── changepasswordscreen/    
    ├── customwidgets/       
    │   ├── custombuttons/   
    │   │   ├── custombuttons.py
    │   │   └── custombuttons.kv
    │   ├── customnavigationbar/     
    │   │   ├── customnavigationbar.py
    │   │   └── customnavigationbar.kv
    │   ├── customdatepicker.py      
    │   ├── customlabels.kv          
    │   ├── customlayouts.kv         
    │   └── custompopups.kv          
    └── components/          
        ├── transactioncard/     
        │   ├── transactioncard.py
        │   └── transactioncard.kv
        ├── categorycard/        
        │   ├── categorycard.py
        │   └── categorycard.kv
        ├── chatmessage/         
        │   ├── chatmessage.py
        │   └── chatmessage.kv
        ├── kivy_charts/         
        │   ├── barchart.py
        │   └── piechart.py
        └── statisticbox/        
            ├── statisticbox.py
            └── statisticbox.kv
```

### 2.2 Key Files and Their Functions

#### Root Level

`main.py`

The application entry point that initializes the Kivy app and manages the screen lifecycle. This file contains the main ExpenseTrackerApp class that orchestrates the entire application.

`main.kv`

The root Kivy language file that defines the application's visual structure and screen management.

`buildozer.spec`

Build configurations for Android deployment.

`icon.png`

Icon image of the app.

`presplash.png`

Image displayed in the splash screen during the app run.

`.github/workflows/build.yml`

Contains the build file to convert the app into APK/AAB using GitHub Actions.

#### Assets Management

`images`

Optimized PNGs in `/assets/images/`:
- Avatar images
- Icon images

`fonts`

Inter font family (Regular/SemiBold/Bold)

#### Library Modules (libs/)

`authentication.py`

Handles all Firebase Authentication operations including:
- User login with email/password
- New account registration
- Password reset functionality

`user.py`

Manages user data and transactions in Firebase database:
- Transaction operations (add, retrieve, analyze)
- Spending analytics and insights
- User profile management (name, avatar, currency)
- Password changing

`config.py`

Contains all the necessary configuration details to connect
to Firebase services including Authentication, Realtime Database, and Storage.

**Note**: In a production environment, these should be **secured** properly.

`utils.py`

Provides utility functions, dictionaries, and lists used throughout the application.

`ai_finance_assistant.py`

Implements the OpenAI-powered financial assistant:
- API communication with OpenAI
- Prompt engineering for financial insights
- Response processing and formatting
- Financial advice generation

#### App Screen Structure

Each screen in the `app/screens/` directory follows a consistent pattern with:
- **A Python file** (e.g., `homescreen.py`) containing the screen's logic
- **A KV file** (e.g., `homescreen.kv`) defining the screen's layout and styling

The application follows a nested screen architecture, with the `Navigation Screen` serving as a container that hosts four main screens:
1. `Home Screen`
2. `Transactions Screen`
3. `Statistics Screen`
4. `Profile Screen`

Additional screens like `Add Transaction` Screen and `AI Screen` are presented as modal overlays when needed.

**Description of each screen**

`Login Screen`

Handles:
- User authentication flow
- UI state management during login
- Loading of application resources and screens after successful login
- Navigation to main application screen

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/login-screen.jpg)

`Sign Up Screen`

Handles:
- New user registration with validation
- User profile creation

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/signup-screen.jpg)

`Forgot Password Screen`

Handles:
- Password reset request flow
- Email validation
- Communication with authentication service

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/reset-password-screen.jpg)

`Navigation Screen`

Navigation screen container for main application screens.

`Home Screen`

Provides:
- User profile summary display
- Monthly spending overview
- Recent transaction listing

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/home-screen.jpg)

`Add Transaction Screen`

Provides:
- Transaction form with amount, category, subcategory, and date inputs
- Input validation and error handling
- Date picker integration
- Category/subcategory dropdown menus
- Transaction submission and data synchronization

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/add-transaction-screen.jpg)

`AI Screen`

Provides:
- AI-powered financial advice interface
- Asynchronous chat messaging system
- Loading states and animations
- Error handling for AI operations

`Transactions Screen`

Provides:
- Comprehensive transaction listing with filtering capabilities
- Time-based filtering (year/month)
- Category-based filtering
- Interactive filtering UI with dropdown menus

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/transaction-screen.jpg)

`Statistics Screen`

Provides:
- Visual spending analytics (charts and cards)
- Monthly spending trends
- Category-wise breakdown
- Time-based filtering capabilities

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/statistic-screen.jpg)

`Profile Screen`

Provides:
- User profile display and management
- Navigation to profile editing screens
- User logout functionality

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/profile-screen.jpg)

`Change Avatar Screen`

Provides:
- Avatar selection grid with preview
- Avatar change functionality
- Visual feedback for selected avatar
- Avatar update propagation to other screens

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/avatar-screen.jpg)

`Change Name Screen`

Provides:
- First/Last Name editing interface
- Input validation
- Name update functionality
- Change propagation to other screens

`Change Currency Screen`

Provides:
- Currency code input and validation
- Currency update functionality
- Data synchronization across all screens

`Change Password Screen`

Provides:
- Secure password change functionality
- Password strength validation

#### App Components

`Transaction Card`

The TransactionCard component (found in `app/components/transactioncard/`) is a central UI element displaying individual transaction entries with the following features:
- **Category icon and color**
- **Category name**
- **Subcategory name**
- **Expense amount**
- **Transaction date**

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/transaction-card.png)

`Category Card`

The CategoryCard component (in `app/components/categorycard/`) provides a visual selection interface for transaction categories.

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/category-card.png)

`Chat Message`

The ChatMessage component (in `app/components/chatmessage/`) is used in the AI assistant screen to display:
- User queries about their finances
- AI-generated responses and insights
- Formatted financial advice
- Visual distinction between user and assistant messages

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/ai-message.png)

`Chart Components`

The application includes two customizable charting components in `app/components/kivy_charts/`:
- **BarChart**: Displays time-series data like monthly spending
- **PieChart**: Shows proportional data like category distribution

For more info about the charts visit: [https://github.com/OuchenTech/Kivy-Charts](https://github.com/OuchenTech/Kivy-Charts)

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/pie-chart.png)

`Statistic Box`

The StatisticBox component (in `app/components/statisticbox/`) encapsulates financial visualization with:
- Chart display area
- Time period filters
- Monthly spending by category (Category card)

#### App Custom Widgets (Reusable UI)

`Custom Buttons`

Button variants (filled/outlined/icon buttons)

`Custom Navigation Bar`

The application uses a custom navigation bar implementation in `app/customwidgets/customnavigationbar/` that:
- Provides tab-based navigation between main screens
- Maintains screen state during navigation
- Implements smooth transitions
- Shows active tab indicators

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/navbar.png)

`Custom Date Picker`

Material-style date selector

`Custom Labels`

Text display widgets with different purposes

`Custom Pop-ups`

Custom dialog and notification widgets

![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/popup.jpg)

`Custom Layouts`

Layout templates

## 3. Getting Started

### 3.1 Quick Start Guide

Follow these steps to get WalletWise up and running quickly:

1. **Purchase and Download the Template**
   - Purchase and Download the template from our [Ko-Fi shop](https://ko-fi.com/shop/settings?src=sidemenu&productType=0)

2. **Extract the Project Files**
   - Unzip the downloaded file to your preferred development directory
   - Ensure all files and folder structure are preserved
  
3. **Set Up Development Environment**
   ```bash
   # Create and activate a virtual environment (recommended)
   python -m venv walletwise-env
   
   # On Windows
   walletwise-env\Scripts\activate
   
   # On macOS/Linux
   source walletwise-env/bin/activate

   # Install dependencies
   pip install -r requirements.txt
   ```

4. **Configure Firebase (Required)**
   - Create a Firebase project (see [Firebase Integration](#4-firebase-integration))
   - Update the `config.py` file with your Firebase credentials
     
   ```python
   firebaseConfig = {
    "apiKey": "YOUR_API_KEY",
    "authDomain": "YOUR_PROJECT_ID.firebaseapp.com",
    # Add all other required Firebase configuration parameters
   }
   ```

5. **Configure OpenAI API (Required for AI Assistant)**
   - Obtain an API key from OpenAI
   - Add your API key to `config.py`
     
   ```python
   openai_api_key = "YOUR_OPENAI_API_KEY"
   ```
   
6. **Test the Application Locally**
   ```bash
   python main.py
   ```

7. **Customize the App (Optional)**
   - Refer to [Section 6](#6-customize-the-app): Customize the App for branding and functional customization
   - Replace placeholder assets with your own images, icons, and fonts

8. **Build for Android**
   - Review and modify buildozer.spec according to your app's requirements
   - Use GitHub Actions for automated builds (see [Section 8](#8-converting-the-kivy-app-to-apkaab-using-github-actions))
   - Alternatively, build locally using Buildozer

### 3.2 Dependency List

Key dependencies included in the template:
- **Kivy 2.3+**: Core UI framework
- **KivyMD 2.0+**: Material Design components
- **Firebase**: Firebase API for Firebase data CRUD operations
- **OpenAI**: API client for AI assistant functionality
- **Requests**: HTTP library for API communication

## 4. Firebase Integration

### 4.1 Project Setup

#### 4.1.1 Create Firebase Project:
1. Go to Firebase Console
2. Click "Add Project" → Name it (e.g., WalletWise-App)
3. Disable Google Analytics (optional)

#### 4.1.2 Add Firebase:
1. On the new project overview window click the web icon to add Firebase to your app
2. Enter a nickname and click Register App button

#### 4.1.3 Enable Authentication:
1. Navigate: Build → Authentication → Sign-in Method
2. Enable Email/Password provider
3. Save changes

#### 4.1.4 Realtime Database Configuration

**Create Database**:
1. Navigate: Build → Realtime Database → Create Database
2. Select Start in test mode (for development)
3. Choose location (e.g., europe-west1)

**Security Rules**:
Replace default rules with:

```json
{
  "rules": {
    "users": {
      "$uid": {
        ".read": "auth != null && auth.uid == $uid",
        ".write": "auth != null && auth.uid == $uid"
      }
    }
  }
}
```

**Why These Rules?**
- Ensures users can only access their own data
- auth.uid == $uid restricts operations to authenticated owners
- Prevents unauthorized reads/writes to other users' data

### 4.2 Connect to WalletWise

**Get Configuration**:
1. Project Settings → General → Your Apps → Web App
2. Copy the firebaseConfig object

**Update config.py**:

```python
firebaseConfig = {
    "apiKey": "YOUR_API_KEY",
    "authDomain": "YOUR_PROJECT_ID.firebaseapp.com",
    "projectId": "YOUR_PROJECT_ID",
    "storageBucket": "YOUR_PROJECT_ID.appspot.com",
    "messagingSenderId": "YOUR_MESSAGING_SENDER_ID",
    "appId": "YOUR_APP_ID",
    "measurementId": "YOUR_MEASUREMENT_ID",
}
```

**Get DatabaseURL**
1. Navigate: Build → Realtime Database
2. In Data section, copy the reference url
3. in `config.py` add "databaseURL": "reference-url" to `firebaseConfig`

In the end, the `firebaseConfig` should have the following configs:

```python
firebaseConfig = {
    "apiKey": "YOUR_API_KEY",
    "authDomain": "YOUR_PROJECT_ID.firebaseapp.com",
    "projectId": "YOUR_PROJECT_ID",
    "storageBucket": "YOUR_PROJECT_ID.appspot.com",
    "messagingSenderId": "YOUR_MESSAGING_SENDER_ID",
    "appId": "YOUR_APP_ID",
    "measurementId": "YOUR_MEASUREMENT_ID",
    "databaseURL": "https://YOUR_PROJECT_ID-default-rtdb.REGION.firebasedatabase.app/",
}
```

### 4.3 Database Structure

Path: /users/<user_id>

```json
{
  "first_name": "John",
  "last_name": "Doe",
  "email": "john@example.com",
  "currency": "USD",
  "avatar": "assets/images/avatars/avatar-1.png",
  "created_at": "2025-04-10T12:00:00Z",
  "transactions": {
    "-NtGj5kK9LmOp7": {
      "amount": 29.99,
      "category": "Shopping",
      "subcategory": "Electronics",
      "timestamp": "2023-10-25T14:30:00Z"
    }
  }
}
```

### 4.4 Testing Firebase Connection

**Verify Authentication**:
1. Run the app and attempt to create a new account
2. Check the Firebase Authentication dashboard to confirm new user creation
3. Test login functionality

**Verify Database Operations**:
1. Add some test transactions in the app
2. In the Firebase console, navigate to Realtime Database
3. Confirm that data appears under the correct user ID

### 4.5 Password Reset Email Customization

**Access Email Templates**:
1. Go to Firebase Console
2. Navigate: Authentication → Templates
3. Select Password reset email template

**Customizable Fields**:
- **Sender name**: Displayed as email sender (example: WalletWise Support)
- **Custom domain**: Replace firebaseapp.com links (example: auth.yourdomain.com)
- **Email subject**: Password reset subject line
- **Email message**: HTML email body
- **Action URL**: Custom reset page link

## 5. OpenAI Integration

This section explains how to set up and customize the AI-powered financial assistant feature.

### 5.1 Create an OpenAI Account
1. Navigate to [https://platform.openai.com/](https://platform.openai.com/)
2. Sign up for an account if you don't have one

### 5.2 Generate API Key
1. Go to API settings in your OpenAI dashboard
2. Create a new API key
3. Copy the key for use in your app

### 5.3 Configure Your App
1. Open `libs/config.py`
2. Replace the existing OpenAI API key with your own:

```python
openai_api_key = "YOUR_OPENAI_API_KEY"
```

### 5.4 Understanding the AI Assistant

#### 5.4.1 Functionality Overview:

The AI financial assistant uses OpenAI's GPT models to:
- Analyze spending patterns
- Provide personalized financial advice
- Answer questions about transactions and budgets
- Suggest ways to improve financial habits

#### 5.4.2 Implementation Details

The `ai_finance_assistant.py` module handles:
- Communication with OpenAI's API
- Context management for personalized responses
- Processing and formatting of AI responses
- Error handling for API issues

## 6. Customize the App
This section provides detailed instructions for customizing various aspects of the expense tracker template to create your own branded application.

### 6.1 Branding Customization

#### App Name and Identity
1. **Change App Name**
   - Open `buildozer.spec` and modify the `title` and `package.name` values
   - Update the app title in `main.py` within the `MainApp` class:
   
   ```python
   # In main.py
   class MainApp(MDApp):
       def build(self):
           self.title = "Your App Name"
           # rest of the method
   ```

2. **Update App Icon**
   - Replace the icon file at `root/icon.png` with your own (recommended size: 512x512 px)
   - Ensure the file name matches the one specified in `buildozer.spec`

3. **Splash Screen**
   - Replace the splash screen image at `root/presplash.png` with your own (recommended size: 512x512 px)
   - Ensure the file name matches the one specified in `buildozer.spec`

#### Visual Identity
1. **Color Scheme**
   Open `main.py` to modify the primary theme colors:
   
   ```python
   self.theme_cls.primary_palette = "Steelblue" # Change to your preferred palette
   ```

   Example:

   ```python
   self.theme_cls.primary_palette = "Steelblue"
   ```
   ![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/steelblue.PNG)

   ```python
   self.theme_cls.primary_palette = "Green"
   ```
   ![](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/green.PNG)
   
3. **Typography**
   - Replace font files in `assets/fonts/` directory
   - Update font references in all python and kivy files where the `font_name` parameter is used (Example: customlabels.kv)

4. **Icons**
   - Navigate to `assets/images/icons/`
   - Replace icons with your own (maintain naming convention)

5. **Avatars**
   - Navigate to `assets/images/avatars/` and add or replace avatars with your own (maintain naming convention)
   - Navigate to `libs/utils.py/` and update `avatars_images` list
  
### 6.2 Functional Customization

#### Transaction Categories
1. **Modify Existing Categories**
   - Open `libs/utils.py` and locate the category definitions
   - Update the categories list:
   
   ```python
   expense_categories = {
       "Category": {
           "subcategories": ["Sub1", "Sub2"],
           "icon": "icon", # kivy icon
           "color": "#HEXCODE"
       }
   }
   ```

2. **Add New Categories**
   - Add new entries to the `expense_categories` dict in `utils.py` (new category, subcategories, icon name, color)
  
#### UI Components
1. **Transaction Card**
   - Open `app/components/transactioncard/transactioncard.kv` to modify the appearance
   - Adjust layout, spacing, colors, and other visual properties

2. **Category Card**
   - Open `app/components/categorycard/categorycard.kv` to modify the appearance
   - Adjust layout, spacing, colors, and other visual properties
   
3. **Navigation Bar**
   - Customize the navigation bar in `app/customwidgets/customnavigationbar/customnavigationbar.kv`
   - Change icons, labels, and tab properties

### 6.3 Advanced Customization

#### Firebase Structure
1. **Modify Data Structure**
   - Update database operations in `libs/user.py`
   - Ensure consistent paths for all database operations
   - Update security rules if structure changes substantially

2. **Add New Collections**
   - Implement new data management functions in `libs/user.py`
   - Create UI components to interact with the new data
   - Update security rules to protect new data paths
  
#### AI Assistant
1. **Customize AI Personality**
   - Open `libs/ai_finance_assistant.py`
   - Locate the system prompt and modify to change the AI's personality:
   
   ```python
   SYSTEM_PROMPT = """
   You are a helpful financial assistant that provides advice on budgeting and spending.
   Your tone is [friendly/professional/casual] and you specialize in [basic budgeting/advanced investment/debt reduction/etc.].
   """
   ```

2. **Adjust AI Capabilities**
   - Modify the prompt templates in `ai_finance_assistant.py`
   - Add new prompt templates for additional AI features
   - Adjust token limits and model parameters

#### Code-Level Changes
1. **Adding New Screens**
   - Create new screen files in `app/screens/` following the existing pattern
   - Add screen classes to `main.py` or `loginscreen.py` depending on whether the screen is going to be loaded during the app start or login

2. **Custom Widgets**
   - Create new widget files in `app/customwidgets/`
   - Follow the template pattern of separate .py and .kv files
   - Import and use your new widgets in the appropriate screens
     
### 6.4 Testing Your Customizations
1. **UI Testing**
   - Run the app to verify visual changes
   - Test responsiveness on different screen sizes
   - Verify that all UI elements are properly aligned

2. **Functional Testing**
   - Test all modified features
   - Verify database operations still work
   - Check that AI functionality responds correctly with new prompts

3. **Performance Testing**
   - Monitor app performance after changes
   - Check for any memory leaks or slowdowns
   - Optimize resource-intensive customizations

## 7. Performance Optimization Techniques

This section details the optimization methods implemented in the expense tracker template to ensure smooth performance, fast loading times, and efficient resource usage, especially on mobile devices.

### 7.1 Lazy Loading Architecture

#### Initial App Loading

The template implements a strategic lazy loading approach that significantly reduces app startup time. This approach offers several benefits:

- **Faster startup time**: Only 3 screens are loaded initially
- **Reduced black screen issue**: Minimal delay between presplash and first screen
- **Lower initial memory footprint**: Fewer widgets in memory at startup

#### Deferred UI Loading

The remaining screens and components are loaded after authentication.

Benefits of this approach:
- **Smoother user experience**: User sees login screen quickly
- **Background loading**: Heavy UI elements load while user authenticates

### 7.2 Deferred Widget Initialization

#### Delayed UI Construction

Instead of building all UI elements during screen initialization, widgets are created on-demand.

This technique:
- **Reduces screen initialization time**: Screens load quickly with minimal content
- **Prevents UI freezing**: Complex UI elements are built only when needed
- **Optimizes memory usage**: Widgets exist only when their screen is active

### 7.3 Multithreading Implementation

#### Background Data Operations

Threading is extensively used to keep the UI responsive while performing data operations.

Benefits of threading:
- **Responsive UI**: Interface remains interactive during data operations
- **Smoother transitions**: No freezing during screen navigation
- **Background processing**: Data loads without blocking user interactions
- **Enhanced user experience**: Loading indicators provide feedback during processes

### 7.4 RecycleView for List Performance

#### Efficient Transaction Listing

The template uses RecycleView instead of traditional ScrollView for displaying transaction lists.

Key advantages:
- **Memory efficiency**: Only visible items are rendered in memory
- **Smooth scrolling**: No lag when scrolling through hundreds of transactions
- **Minimal memory footprint**: Large lists don't consume excessive resources

### 7.5 Reusable Widget Architecture

#### Component-Based Design

The template implements a reusable widget system to optimize performance and code maintenance.

Benefits of reusable widgets:
- **Reduced memory usage**: Widget definitions are loaded once
- **Faster rendering**: Common widgets are optimized for performance
- **Consistent UI**: Same component used across different screens
- **Simplified maintenance**: Changes to a widget propagate everywhere

## 8. Converting the Kivy App to APK/AAB Using GitHub Actions

This section explains how to automate the process of building your Kivy application into an APK (Android Package) or AAB (Android App Bundle) using a GitHub Actions. This method eliminates the need for manual builds and allows for continuous integration (CI) whenever changes are pushed to your repository.

### 8.1 GitHub Action Overview

GitHub Actions is a CI/CD (Continuous Integration/Continuous Deployment) platform that automates workflows directly within your GitHub repository. By defining a YAML configuration file (`.github/workflows/build.yml`), you can trigger automated builds, tests, and deployments whenever code is pushed or a pull request is made.

**Key Benefits**:
- **Automated Builds**: Once configured, new builds are triggered automatically on push or pull requests
- **Consistent Environment**: Eliminates "works on my machine" problems with reproducible build environments
- **No Local Setup Required**: No need to install Buildozer, Android SDK, or NDK locally
- **Version Control Integration**: Build history is directly tied to your code commits
- **Parallel Builds**: Can simultaneously build debug and release versions
- **CI/CD Integration**: Seamlessly fits into broader continuous integration pipelines

### 8.2 Conversion Process

The app includes a GitHub workflow configuration (`.github/workflows/build.yml`) and a buildozer.spec file to streamline the APK/AAB creation process.

1. Commit and push the code to your GitHub repository
2. Navigate to the Actions tab on your repository's GitHub page
3. Select the build.yml workflow and manually trigger it or wait for it to start automatically on push
4. Once completed, download the APK/AAB from the generated artifacts section of the workflow run

**Important**: Ensure all required fields in `buildozer.spec` are correctly configured before initiating the build process. 

### 8.3 Manual Build Option

If you prefer to build locally without GitHub Actions:

1. Install Buildozer:
   ```bash
   pip install buildozer
   ```

2. Install required dependencies (Ubuntu/Debian example):
   ```bash
   sudo apt-get install -y python3-pip build-essential git python3-dev
   sudo apt-get install -y libsdl2-dev libsdl2-image-dev libsdl2-mixer-dev libsdl2-ttf-dev
   sudo apt-get install -y libportmidi-dev libswscale-dev libavformat-dev libavcodec-dev
   sudo apt-get install -y zlib1g-dev libgstreamer1.0-dev
   ```

3. Build the APK:
   ```bash
   buildozer android debug
   ```

4. The APK will be available in the bin/ directory

## 9. Troubleshooting Guide

This section provides solutions to common issues developers might encounter when working with the WalletWise template.

### 9.1 Firebase Connection Issues

#### Problem: Authentication Failures
- **Symptoms**: Login fails with "Authentication failed" or similar errors
- **Possible causes**:
  - Incorrect Firebase configuration in config.py
  - Firebase Authentication not enabled
  - Internet connectivity issues
- **Solutions**:
  - Verify all Firebase configuration parameters in config.py
  - Check Firebase Console to ensure Authentication is enabled
  - Test network connectivity and Firebase status

#### Problem: Database Operations Failing
- **Symptoms**: Transactions not saving or loading
- **Possible causes**:
  - Incorrect database URL
  - Path structure mismatch
  - Security rules blocking operations
- **Solutions**:
  - Confirm database URL includes correct region
  - Check path construction in database operations
  - Verify security rules allow the operations

### 9.2 Build and Deployment Issues

#### Problem: GitHub Action Build Failures
- **Symptoms**: GitHub workflow fails during build process
- **Possible causes**:
  - Missing dependencies in buildozer.spec
  - Incompatible Python version
  - Resource file issues
- **Solutions**:
  - Check build logs for specific error messages
  - Verify all requirements are listed in buildozer.spec
  - Ensure all resource paths are correct

#### Problem: APK Installation Issues
- **Symptoms**: APK builds but fails to install on device
- **Possible causes**:
  - Incorrect permissions
  - Incompatible Android API level
  - Missing dependencies
- **Solutions**:
  - Verify android.permissions in buildozer.spec
  - Adjust android.api to match target devices
  - Check for missing or incompatible dependencies

### 9.3 UI Rendering Issues

#### Problem: Layout Inconsistencies
- **Symptoms**: UI elements misaligned or overlapping
- **Possible causes**:
  - Screen size adaptation issues
  - Incorrect layout properties
  - Font scaling problems
- **Solutions**:
  - Use relative sizing (dp) instead of absolute pixels
  - Use (sp) metric for text font size instead of pixel
  - Test on multiple screen sizes and densities

#### Problem: Performance Slowdowns
- **Symptoms**: Lag during navigation or transaction loading
- **Possible causes**:
  - Too many widgets loaded simultaneously
  - Inefficient list rendering
  - Background operations blocking UI thread
- **Solutions**:
  - Implement additional lazy loading
  - Convert ScrollView to RecycleView where appropriate
  - Move more operations to background threads

## 10. Frequently Asked Questions (FAQ)

### 10.1 General Questions

#### Q: Is WalletWise suitable for commercial applications?
A: Yes, WalletWise is designed to be a production-ready template that can be customized and deployed as a commercial application. Refer to the License section for specific usage terms.

#### Q: What platforms does WalletWise support?
A: Currently, WalletWise is optimized for Android deployment. The template architecture supports cross-platform development, but iOS-specific configurations would require additional setup.

#### Q: Can I use WalletWise without Firebase?
A: The template is built with Firebase integration as a core feature. While it's possible to replace Firebase with another backend, this would require significant modifications to the authentication and data management modules.

#### Q: Do I need an OpenAI API subscription to use the AI features?
A: Yes, the AI financial assistant feature requires an active OpenAI API key, which involves subscription costs based on usage. You can obtain this from the OpenAI platform.

### 10.2 Technical Questions

#### Q: What Python version is required?
A: WalletWise requires Python 3.9 or higher. Earlier versions may cause compatibility issues with some of the dependencies.

#### Q: What Kivy/KivyMD version is required?
A: WalletWise requires Kivy 2.3 or higher and KivyMD 2.0 or higher. Earlier versions may cause compatibility issues.

#### Q: Can I add more transaction categories?
A: Yes, you can easily add, modify, or remove transaction categories by editing the `expense_categories` dictionary in the `libs/utils.py` file.

#### Q: Does the template include income tracking?
A: The current version focuses on expense tracking. Income tracking can be implemented by extending the transaction system and adding appropriate categories.

#### Q: How can I implement additional languages?
A: For internationalization, you would need to:
1. Create a translation dictionary in `libs/utils.py`
2. Add a language selection option in the login screen and / or profile screen 
3. Apply the selected language's translations throughout the UI

### 10.3 Deployment Questions

#### Q: How do I create a release version vs. debug version?
A: The GitHub Action workflow includes configurations for both debug and release builds. To create a release build, specify the `--release` flag in the buildozer command in the workflow file, and ensure you've configured your **signing key**.

#### Q: How do I sign my APK for release?
A: You'll need to:
1. Generate a keystore file: `keytool -genkey -v -keystore my-release-key.keystore -alias alias_name -keyalg RSA -keysize 2048 -validity 10000`
2. Configure the GitHub Action to use your keystore or build locally with `buildozer android release`

#### Q: Can I publish the app to the Google Play Store?
A: Yes, the template is ready for Google Play Store publication. You'll need to:
1. Build a release version of the app (signed APK or AAB)
2. Create a developer account on Google Play Console
3. Follow the submission process including app listing, content rating, and pricing

## 11. Support and Contact

### 11.1 Getting Help

#### Documentation Resources
- Refer to this comprehensive documentation for most setup and customization questions
- Review the Kivy and KivyMD documentation for framework-specific questions

#### Community Support
- Join the [Kivy Discord Community](https://chat.kivy.org/) for general Kivy/KivyMD questions
- Participate in [Firebase Community](https://firebase.google.com/community/) for backend-related issues

### 11.2 Contact Information

For business inquiries, partnership opportunities, or other questions:

- **Email**: ouchen.yassine.umi@gmail.com
- **GitHub**: https://github.com/OuchenTech
- **YouTube**: https://www.youtube.com/@OuchenTech
- **Discord**: @OuchenTech

### 14.3 Updates and Notifications

- **GitHub Watch**: Watch the repository for updates
- **Social Media**: Follow @OuchenTech on youtube and discord for announcements

## 12. License

### 12.1 License Terms

WalletWise is released under a Commercial Template License. This license is designed to give developers flexibility while protecting the original work from unauthorized redistribution.

This license allows you to:
- Create multiple end products (personal or commercial applications) from a single license purchase
- Modify the template code for your own projects
- Sell or distribute applications created using this template
- Modify and resell the template as part of a substantially different product with proper attribution

The following restrictions apply:
- You may not resell or redistribute the original unmodified template
- You may not include the template in developer toolkits or template collections
- You may not claim the template design or code as your own original work

### 12.2 Commercial Template License Text

```
WalletWise Commercial Template License

Copyright (c) 2025 OuchenTech

This license grants the purchaser a non-exclusive right to use the WalletWise template under the following terms:

1. USAGE RIGHTS:
   - The purchaser may use the template to create unlimited end products for personal use or for clients.
   - Each end product may be sold or distributed without additional licensing fees.

2. REDISTRIBUTION RESTRICTIONS:
   - The original unmodified template may not be resold, redistributed, or included in template collections.
   - The template code may not be used to create a competing template product similar to WalletWise.

3. MODIFICATION RIGHTS:
   - The purchaser may modify the template for their own projects.
   - Substantially modified versions of the template may be resold as new products, provided they include significant changes or additions that transform it from the original.
   - Any resold modified version must include attribution to OuchenTech as the original creator in the documentation and about section.

4. ATTRIBUTION:
   - Attribution is not required in end products but is appreciated.
   - Attribution is required when reselling modified versions of the template.

5. WARRANTY:
   THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

### 12.3 Third-Party Components

WalletWise incorporates several third-party libraries and resources, each with its own license:

- **Kivy/KivyMD**: MIT License
- **Firebase**: Subject to Firebase's Terms of Use
- **OpenAI API**: Subject to OpenAI's Terms of Use
- **Kivy Charts**: MIT License

Please refer to each package's documentation for specific license details.

### 12.4 Purchase Entitlements

When you purchase WalletWise, you receive:
- The complete source code with all features described in this documentation
- All included assets (icons, avatar images, fonts)
- The right to use the template for unlimited personal or client projects
- The right to modify and redistribute substantially changed versions with attribution
- Basic support via email for 30 days after purchase

For questions regarding licensing or usage rights, please contact: ouchen.yassine.umi@gmail.com

## Appendix A: Directory Structure Reference

For a quick reference, here's the complete directory structure of the WalletWise template:

```
WalletWise/
├── main.py                  
├── main.kv                  
├── .github/                 
│   └── workflows/
│       └── build.yml 
├── buildozer.spec          
├── icon.png                 
├── presplash.png            
├── assets/                  
│   ├── fonts/               
│   └── images/              
│       ├── icons/           
│       └── avatar/          
├── libs/                    
│   ├── authentication.py    
│   ├── user.py              
│   ├── config.py            
│   ├── utils.py             
│   └── ai_finance_assistant.py  
└── app/                     
    ├── screens/             
    │   ├── loginscreen/     
    │   ├── signupscreen/
    │   ├── forgotpasswordscreen/
    │   ├── navigationscreen/    
    │   ├── homescreen/      
    │   ├── transactionscreen/   
    │   ├── statisticscreen/ 
    │   ├── profilescreen/   
    │   ├── addtransactionscreen/    
    │   ├── aiscreen/        
    │   ├── changeavatarscreen/  
    │   ├── changenamescreen/    
    │   ├── changecurrencyscreen/    
    │   └── changepasswordscreen/    
    ├── customwidgets/       
    │   ├── custombuttons/   
    │   │   ├── custombuttons.py
    │   │   └── custombuttons.kv
    │   ├── customnavigationbar/     
    │   │   ├── customnavigationbar.py
    │   │   └── customnavigationbar.kv
    │   ├── customdatepicker.py      
    │   ├── customlabels.kv          
    │   ├── customlayouts.kv         
    │   └── custompopups.kv          
    └── components/          
        ├── transactioncard/     
        │   ├── transactioncard.py
        │   └── transactioncard.kv
        ├── categorycard/        
        │   ├── categorycard.py
        │   └── categorycard.kv
        ├── chatmessage/         
        │   ├── chatmessage.py
        │   └── chatmessage.kv
        ├── kivy_charts/         
        │   ├── barchart.py
        │   └── piechart.py
        └── statisticbox/        
            ├── statisticbox.py
            └── statisticbox.kv
```

## Appendix B: Glossary of Terms

- **APK**: Android Package Kit, the file format used to distribute and install Android applications
- **AAB**: Android App Bundle, a newer format that optimizes APK delivery for different device configurations
- **Buildozer**: A tool used to package Kivy applications for Android and iOS
- **Firebase**: Google's mobile application development platform, providing tools for authentication, database, and hosting
- **KivyMD**: A collection of Material Design-compliant widgets for Kivy
- **OpenAI API**: A service that provides AI language models for text generation and analysis
- **RecycleView**: A widget in Kivy designed for efficient display of large datasets
- **GitHub Actions**: GitHub's CI/CD platform for automating workflows
