# 📚 The Shared Library of Wisdom

<p align="center">
  <img width="399" height="265" alt="Image" src="https://github.com/user-attachments/assets/3b51ebf4-38a7-4b23-b956-a6363baaba51" />
</p>

## 📑 Table of Contents
- 📖 [About](#about)
- 📁 [File Structure](#file-structure)
- 📖 [History Facts](#history-facts)
- 📄 [Project Description](#project-description)
- 🧭 [How to Read the Library](#how-to-read-the-library)
- 🛠️ [How to Use the Library](#how-to-use-the-library)

## 📖 About
A CCS112 - Application and Emerging Technologies Laboratory Activity 3: **Collaborative Markdown-based digital encyclopedia built using Git workflows.**

## FILE STRUCTURE

```
The_Shared_Library_of_Wisdom/
├── .gradle/
│   ├── buildOutputCleanup/
│   ├── caches/
│   ├── daemon/
│   └── wrapper/
│
├── .idea/
│   ├── codeStyles/
│   ├── inspectionProfiles/
│   ├── libraries/
│   ├── modules.xml
│   ├── workspace.xml
│   └── misc.xml
│
├── .kotlin/
│   ├── caches/
│   └── sessions/
│
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── example/
│   │   │   │           └── thesharedlibraryofwisdom/
│   │   │   │               └── MainActivity.kt
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   ├── values/
│   │   │   │   └── drawable/
│   │   │   └── AndroidManifest.xml
│   │   │
│   │   ├── test/
│   │   │   └── java/
│   │   │       └── com/
│   │   │           └── example/
│   │   │               └── thesharedlibraryofwisdom/
│   │   │                   └── ExampleUnitTest.kt
│   │   │
│   │   └── androidTest/
│   │       └── java/
│   │           └── com/
│   │               └── example/
│   │                   └── thesharedlibraryofwisdom/
│   │                       └── ExampleInstrumentedTest.kt
│   │
│   ├── build.gradle.kts
│   └── proguard-rules.pro
│
├── gradle/
│   └── wrapper/
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
│
├── history/
│   └── git-workflow.md
│
├── .gitignore
├── build.gradle.kts
├── CONTRIBUTING.md
├── gradle.properties
├── gradlew
├── gradlew.bat
├── history.md
├── local.properties
├── README.md
└── settings.gradle.kts
```

### HISTORY FACTS

Facts's 1 to 3 Facts: https://github.com/Joronski/The-Shared-Library-of-Wisdom/blob/master/history.md

Workflow Facts: https://github.com/Joronski/The-Shared-Library-of-Wisdom/blob/master/history/git-workflow.md

## PROJECT DESCRIPTION

This project is a collaborative digital encyclopedia built using Markdown and Git, designed to showcase the practical application of
emerging technologies and modern software development best practices. It emphasizes:

Version Control:
Utilizing Git and GitHub to manage contributions, track changes, and ensure seamless collaboration among team members.

Structured Documentation:
Leveraging Markdown for clear, consistent, and easily maintainable content, making it accessible for both technical and non-technical users.

Team Collaboration:
Encouraging effective teamwork through branching strategies, pull requests, and code reviews, fostering a culture of peer feedback and
continuous improvement.

Hands-on Learning Experience:
Apply theoretical knowledge in a practical setting, allowing you to gain confidence in using Git and Markdown while working on a real collaborative
project, just like in professional software development environments.

*Knowledge Sharing & Accessibility: Building a collective resource that democratizes information, promotes open learning, and ensures that valuable insights are easily accessible to a wide audience.*

***Scalability & Future Growth***: Designing the encyclopedia with adaptability in mind, ensuring it can expand to include new topics, contributors, and technologies without losing structure or clarity.

The encyclopedia is not only a scalable and user-friendly resource but also a living document that evolves with the contributions of its users. It serves as a
valuable reference tool for learners, developers, and educators, bridging the gap between theory and practical application in software development.

## HOW TO READ THE LIBRARY
1. The library is organized into Kotlin packages.
2. Start with the core or main files to understand
3. Class and function names follow Kotlin naming
4. Comments are provided to explain important logic

## HOW TO USE THE LIBRARY
1. Import the required class or function:
2. Use `object` for shared or singleton functionality.
3. Use `data class` for structured data models.
4. Follow existing examples in the library to ensure.