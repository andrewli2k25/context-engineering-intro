## FEATURE:

Your goal is to: Build an AI-powered iOS app used to optimize middle school, high school, and college student schedules and productivity 

4 main tabs within the app: Tasks, AI assistant, calendar, stats 

Try to sync google calendar/google classroom
Give the students the ability to input their class schedule and any extracurricular commitments they have into the app 


Tasks: Shows user a list of tasks that they need to do and the time slot allocated to each task
Academic: “Complete AP Biology Lab 5:00 - 6:00 PM,” “Study for Chemistry exam 6:00 - 7:00 PM,” “Finish English project due Friday” 
Extracurricular: “Recruit 2 people to business club,” “Go to football practice at 6pm,” “finish the treasurer ledger,” “Sign up for volunteer work on Saturday”   

Game/Point system: Used to boost the student’s productivity and serves as a visual indicator to the student of their progress. Each task will be assigned a point value determined by the AI assistant, and when the user completes a task they will be awarded said points. 

Stats: The statistics of the game system will be displayed in the stats tab. Points earned can be used to advance the user’s level (the amount of points required to level up increases exponentially.) There will also be achievements in the app which can be displayed on the user’s profile as badges. The user will also have their streak displayed (a streak starts when the user completes all of their daily tasks) and their longest streak. 


AI Assistant: Tool used to optimize student schedules and help with any studying problems. Will understand the details of the student’s academic and extracurricular life so that it can help with any problems associated with either. It is imperative that the AI remembers these details of the student the whole time the user is using the app. Also provides support for productivity (e.g. cheering the student on idk)
    -After the student inputs their day-to-day schedule, the AI remembers this and assists with any scheduling difficulties. 
    -If the user has tasks that aren’t due the day of such as an exam or project for a class, the AI will be able to determine how much time the user should allocate per day based on the user’s schedule and free time within that schedule so that the user can study effectively for the exam or complete the project on time 
    -The user can personally notify the AI if they want to focus on a specific class, and the AI will automatically allocate more study time or extra time for assignments associated with that class
    -Automatic deadline reminders with escalating urgency as due dates approach
    -Study method recommendations based on learning style assessment and past performance
    -Integration with learning management systems (Google Classroom, Canvas, Blackboard, etc.) to pull assignments and grades automatically
    -"Focus mode" that blocks distracting apps during scheduled study sessions
    -Sleep schedule optimization based on class times and study load
    -Ability to analyze class syllabuses to see when teachers have office hours so students can plan specific times and dates where they can to       office hours


Calendar: Integration with learning systems (Google Classroom, Canvas, Blackboard, etc.) as well as outside calendars (Google Calendar) to display the user’s schedule on a daily, weekly, and monthly basis. 
The app will also have an in-house calendar system that displays information from learning systems and outside calendars along with the various tasks that the user has. 


## DOCUMENTATION:

iOS Development & Core Frameworks
Apple Developer Documentation

Swift Programming Language Guide - https://docs.swift.org/swift-book/
SwiftUI Framework - https://developer.apple.com/documentation/swiftui/
UIKit Framework (if using hybrid approach) - https://developer.apple.com/documentation/uikit/
Core Data Framework (local data persistence) - https://developer.apple.com/documentation/coredata/
CloudKit Framework (iCloud sync) - https://developer.apple.com/documentation/cloudkit/
UserNotifications Framework (reminders/notifications) - https://developer.apple.com/documentation/usernotifications/
EventKit Framework (calendar integration) - https://developer.apple.com/documentation/eventkit/
App Store Connect API - https://developer.apple.com/documentation/appstoreconnectapi/

AI Integration & Natural Language Processing
OpenAI APIs

OpenAI API Documentation - https://platform.openai.com/docs/
GPT-4 API Reference - https://platform.openai.com/docs/api-reference/
Function Calling Guide - https://platform.openai.com/docs/guides/function-calling/

Alternative AI Services

Anthropic Claude API - https://docs.anthropic.com/
Google Gemini API - https://ai.google.dev/docs/
Azure OpenAI Service - https://learn.microsoft.com/en-us/azure/cognitive-services/openai/

Calendar & Educational Platform Integration
Google APIs

Google Calendar API - https://developers.google.com/calendar/api/
Google Classroom API - https://developers.google.com/classroom/
Google OAuth 2.0 Documentation - https://developers.google.com/identity/protocols/oauth2/
Google APIs Client Library for Swift - https://github.com/googleapis/google-api-swift-client

Learning Management Systems

Canvas API Documentation - https://canvas.instructure.com/doc/api/
Blackboard REST API - https://developer.blackboard.com/portal/displayApi/
Schoology API - https://developers.schoology.com/api/
Moodle Web Services API - https://docs.moodle.org/dev/Web_services_API/

Data Storage & Backend Services
Firebase (Google)

Firebase iOS Documentation - https://firebase.google.com/docs/ios/
Firestore Database - https://firebase.google.com/docs/firestore/
Firebase Authentication - https://firebase.google.com/docs/auth/ios/
Firebase Cloud Functions - https://firebase.google.com/docs/functions/

Alternative Backend Services

AWS Amplify iOS - https://docs.amplify.aws/lib/q/platform/ios/
Supabase Swift - https://supabase.com/docs/reference/swift/
MongoDB Realm Swift - https://docs.mongodb.com/realm/sdk/swift/

Networking & API Integration
HTTP & Networking

URLSession Documentation - https://developer.apple.com/documentation/foundation/urlsession/
Alamofire (Third-party HTTP library) - https://github.com/Alamofire/Alamofire
Combine Framework (reactive programming) - https://developer.apple.com/documentation/combine/

Local Storage & Data Management
Core Data & SQLite

Core Data Programming Guide - https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/CoreData/
SQLite.swift - https://github.com/stephencelis/SQLite.swift
FMDB (SQLite wrapper) - https://github.com/ccgus/fmdb

UI/UX & Design Resources
Design Guidelines

Apple Human Interface Guidelines - https://developer.apple.com/design/human-interface-guidelines/
SF Symbols - https://developer.apple.com/sf-symbols/
Apple Design Resources - https://developer.apple.com/design/resources/

Third-party UI Libraries

Charts (Swift charting library) - https://github.com/danielgindi/Charts
Lottie iOS (animations) - https://github.com/airbnb/lottie-ios

Push Notifications & Background Processing
Apple Push Notification Service

APNs Documentation - https://developer.apple.com/documentation/usernotifications/
Background App Refresh - https://developer.apple.com/documentation/backgroundtasks/
Local Notifications - https://developer.apple.com/documentation/usernotifications/scheduling_a_notification_locally_from_your_app

Security & Privacy
Data Protection

App Transport Security - https://developer.apple.com/documentation/security/app_transport_security/
Keychain Services - https://developer.apple.com/documentation/security/keychain_services/
Privacy Guidelines - https://developer.apple.com/app-store/review/guidelines/#privacy

Testing & Analytics
Testing Frameworks

XCTest Framework - https://developer.apple.com/documentation/xctest/
Quick & Nimble (BDD testing) - https://github.com/Quick/Quick

Analytics & Monitoring

Firebase Analytics - https://firebase.google.com/docs/analytics/ios/
Crashlytics - https://firebase.google.com/docs/crashlytics/get-started?platform=ios
TestFlight - https://developer.apple.com/testflight/

MCP Servers & RAG Systems
Web Scraping & Content Analysis

Crawl4AI - https://github.com/unclecode/crawl4ai
Beautiful Soup Documentation (if using Python backend) - https://www.crummy.com/software/BeautifulSoup/bs4/doc/
Scrapy Documentation - https://docs.scrapy.org/

Vector Databases & RAG

Pinecone Documentation - https://docs.pinecone.io/
Weaviate Documentation - https://weaviate.io/developers/weaviate/
Chroma Documentation - https://docs.trychroma.com/

Educational Standards & Compliance
Privacy Compliance

FERPA Guidelines - https://www2.ed.gov/policy/gen/guid/fpco/ferpa/index.html
COPPA Compliance - https://www.ftc.gov/enforcement/rules/rulemaking-regulatory-reform/childrens-online-privacy-protection-rule
GDPR for Apps - https://gdpr.eu/

Deployment & App Store
App Store Guidelines

App Store Review Guidelines - https://developer.apple.com/app-store/review/guidelines/
App Store Connect Help - https://help.apple.com/app-store-connect/
TestFlight Documentation - https://developer.apple.com/testflight/
