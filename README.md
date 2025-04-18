# WalletWise - Android Expense Tracker App Template

![WalletWise Hero](https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/hero.png)

## Overview

WalletWise is a **production-ready, modular expense tracker template** built with Python and Kivy, designed to help developers quickly launch a feature-rich personal finance app.

### Key Features

- **User Authentication**: Secure email/password login and registration
- **Transaction Management**: Add, view, and filter expenses
- **Data Visualization**: Charts and statistics to analyze spending
- **AI Financial Assistant**: OpenAI-powered advice and insights
- **Firebase Integration**: Real-time data synchronization
- **Customizable UI**: Easy to rebrand and modify

### Screenshots

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/home-screen.jpg" width="24%">
    <img src="https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/transaction-screen.jpg" width="24%">
    <img src="https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/statistic-screen.jpg" width="24%">
    <img src="https://github.com/OuchenTech/WalletWise-documentation/blob/main/screenshots/profile-screen.jpg" width="24%">
</div>

## Quick Start Guide

### Prerequisites
- Python 3.9 or higher
- Firebase account
- OpenAI API key (for AI features)

### Installation

1. Download the template from our [Ko-Fi shop](https://ko-fi.com/shop/settings?src=sidemenu&productType=0)
2. Extract the files to your project directory
3. Set up a virtual environment:

```bash
python -m venv walletwise-env
source walletwise-env/bin/activate  # On Windows: walletwise-env\Scripts\activate
pip install -r requirements.txt
```

4. Configure Firebase and OpenAI:
   - Update `libs/config.py` with your credentials

5. Run the application:

```bash
python main.py
```

### Build for Android

Configure `buildozer.spec` and use GitHub Actions workflow for automated builds:

```bash
# Or build locally if preferred
buildozer android debug
```

## Documentation

For complete documentation, please refer to the [comprehensive guide](DOCUMENTATION.md) included with the template, covering:

- Detailed app structure and architecture
- Firebase and OpenAI integration guides
- Customization options
- Performance optimization techniques
- Troubleshooting common issues

## Template Benefits

✅ Reduces development time by **80+%** with pre-built core features  
✅ Firebase Auth & DB connected and ready to use  
✅ AI Assistant for Personal Finance  
✅ Complete source code & assets  
✅ Performance-optimized architecture  
✅ Template-ready design (easy customization)  

## License

WalletWise is released under a Commercial Template License. See [LICENSE](LICENSE) for details.

## Support and Contact

- **Email**: ouchen.yassine.umi@gmail.com
- **GitHub**: https://github.com/OuchenTech
- **YouTube**: https://www.youtube.com/@OuchenTech
- **Discord**: @OuchenTech

## Get Started Now

[Purchase and Download](https://ko-fi.com/shop/settings?src=sidemenu&productType=0) to start building your finance app today!

---
Copyright (c) 2025 OuchenTech
