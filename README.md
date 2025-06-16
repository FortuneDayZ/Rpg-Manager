# 🧝‍♂️ RPG Manager

## 🧭 Overview

**RPG Manager** is a SwiftUI-based app that allows users to create, edit, and manage characters in a fantasy role-playing game setting. With support for different classes, races, and character stats, users can visualize, modify, and store their heroes in a visually appealing interface using SwiftData for persistence.

---

## ✨ Features

- 🎨 **Create and Customize Characters**  
  Input your hero's name, class, race, and core stats such as HP, Mana, Level, Armor, and XP.

- 🔁 **Edit Existing Characters**  
  Modify completed or pending characters with immediate UI feedback and class-specific logic.

- 🌱 **Class-Specific Enhancements**  
  Special classes like Barbarian, Ranger, and Wizard inherit from a base `Actor` class and come with unique abilities.

- 💾 **Persistence with SwiftData**  
  Store your characters using SwiftData models for both completed and incomplete characters.

- 📚 **Two-tier Character System**  
  - `Actor`: for fully completed and validated characters.  
  - `PendingActor`: for partially filled forms, allowing progressive creation and error resilience.

- 🌌 **Glassmorphic UI + Fantasy Theme**  
  Visually immersive UI with fantasy illustrations, custom fonts, and modern blur effects.

---

## 🛠️ Technologies Used

- **Language**: Swift
- **Frameworks**: SwiftUI, SwiftData
- **Architecture**: MVVM-inspired modular components
- **Custom Views**: GlassmorphicButton, HeroImageView, LabeledTextField

---

## 🚀 How to Run

1. Clone the repository to your Mac using:
   ```bash
   git clone https://github.com/YourUsername/RPG-Manager.git
   ```
2. Open the `.xcodeproj` file in Xcode.
3. Run on a simulator or connected iOS device.

---

## 🖼️ Screenshots

### 1. Welcome Screen  
Entry point of the app with fantasy visuals and navigation options.

<img src="https://github.com/FortuneDayZ/Rpg-Manager/blob/main/Screenshots/Welcome.png?raw=true" width="250" />

---

### 2. Character Customization  
Users can select race, class, and customize stats in a dynamic and animated UI.

<img src="https://github.com/FortuneDayZ/Rpg-Manager/blob/main/Screenshots/customize.png?raw=true" width="250" />

---

### 3. Edit Existing Characters  
Update any previously created character, with stat validation and image previews.

<img src="https://github.com/FortuneDayZ/Rpg-Manager/blob/main/Screenshots/edit.png?raw=true" width="250" />

---

### 4. Load Characters  
Browse through completed and pending characters, each with its own preview card.

<img src="https://github.com/FortuneDayZ/Rpg-Manager/blob/main/Screenshots/load.png?raw=true" width="250" />

---

## 📁 File Structure

```
rpg_manager/
├── Models/
│   ├── Actor.swift
│   ├── PendingActor.swift
│   ├── CharacterClass.swift
│   ├── RacialTrait.swift
│   └── [Class Extensions: Barbarian.swift, Wizard.swift, Ranger.swift]
├── Views/
│   ├── MainMenu.swift
│   ├── PageTwo.swift
│   ├── LoadChar.swift
│   ├── EditChar.swift
│   ├── EditCharForPending.swift
│   └── ActorView.swift
├── Assets/
│   └── Images (e.g., dwarf_barbarian, elf_wizard, etc.)
└── rpg_managerApp.swift
```

---

## 👥 Credits

- **Phuc Thinh Nguyen**  
- **Marsel Abdullin**  
- **Ahmad Kaddoura**

---
