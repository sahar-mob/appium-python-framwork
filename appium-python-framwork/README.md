# AutomationCamp Appium Python Framework

A mobile test automation framework built with **Python**, **pytest**, and **Appium**. It uses the Page Object Model (POM) pattern to automate the [Swag Labs mobile app](https://github.com/saucelabs/sample-app-mobile) on Android (and iOS-ready configuration).

## Features

- Page Object Model with a reusable `BasePage` for common mobile interactions (tap, scroll, swipe, etc.)
- Singleton `DriverManager` for Android (UiAutomator2) and iOS (XCUITest) driver lifecycle
- pytest fixtures for driver setup/teardown, screenshots on failure, and Allure attachments
- YAML-based configuration (`config/config.yml`)
- Allure and HTML reporting
- Docker-based Android emulator with Appium for local and CI runs
- GitHub Actions workflow for automated test execution and report publishing

## Project Structure

```
automationcamp-appium-python-framework/
├── config/
│   └── config.yml              # Appium, platform, logging, and Allure settings
├── framework/
│   ├── base_page.py            # Base page object with shared mobile actions
│   ├── driver_manager.py       # Appium driver creation and management
│   ├── test_logger.py          # Structured logging utilities
│   └── test_utils.py           # Test helpers (data generation, performance, etc.)
├── tests/
│   ├── pages/
│   │   ├── login_page.py       # Login page object
│   │   └── home_page.py        # Home page object
│   ├── test_login.py           # Login and validation tests
│   └── test_home.py            # Home page, menu, scroll, and logout tests
├── app/
│   └── saucelabs.apk           # Swag Labs APK (not included — download separately)
├── conftest.py                 # pytest fixtures and hooks
├── docker-compose.yml          # Docker-Android emulator + Appium stack
├── pytest.ini                  # pytest defaults, markers, and logging
├── requirements.txt
└── .github/workflows/main.yml  # CI pipeline
```


