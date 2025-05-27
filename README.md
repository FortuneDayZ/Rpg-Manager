# 🛡️ Rpg-Manager

## 📖 Overview

**Rpg-Manager** is a character creation and management application for role-playing games, built natively with SwiftUI and Swift. It allows users to design detailed characters, specifying attributes like class, race, level, stats, and more. The app leverages SwiftData for robust on-device data persistence.

---

## ✨ Features

* 🔐 **Character Data Persistence**: Securely saves character information locally using SwiftData.
* 🎭 **Detailed Character Creation**:
    * Define a unique `name` for each character.
    * Select a `CharacterClass` (e.g., Barbarian, Ranger, Wizard).
    * Choose a `RacialTrait` (e.g., Elf, Human, Dwarf).
    * Set `level`, `mana`, `maxHP`, `currentHP`, `armorClass`, and `experience`.
    * Track `isAlive` and `isActive` status.
* ⚔️ **Basic Actions**: Includes an `attack()` method for characters.
* 📝 **Form-Based Input**: Likely uses a form (suggested by `ActorView.swift` and `MainMenu` parameters) for inputting character attributes.
* 🔄 **Two-Stage Data Handling**: Utilizes an `Actor` model for finalized characters and a `PendingActor` model, possibly for temporary data handling during the creation process (e.g., form inputs as strings before conversion).
* 📱 **SwiftUI Interface**: Modern and declarative UI built with SwiftUI.

---

## 🧰 Core Components & Technologies

* **Swift**: The primary programming language.
* **SwiftUI**: Used for building the user interface.
* **SwiftData**: For on-device data persistence of character models.
* **Xcode**: The development environment for building and running the app.

---

## 🚀 How to Run

### 1. Obtain the Project Files
   Clone or download the repository/project files to your local machine.

### 2. Open in Xcode
   Navigate to the project directory and open the `.xcodeproj` or `.swiftpm` file. This will launch the project in Xcode.

### 3. Select a Target
   Choose a target simulator (e.g., iPhone, iPad) or a connected physical Apple device from the Xcode toolbar.

### 4. Build & Run
   Click the "Play" button (or `Cmd+R`) in Xcode to build and run the application on the selected target.

---

## 🗂 Project Structure (Key Files)

Rpg-Manager/
├── rpg_managerApp.swift     # Main application entry point, SwiftData setup
├── Models/
│   ├── Actor.swift          # Core data model for a character
│   ├── PendingActor.swift   # Model for character data during creation/editing
│   ├── CharacterClass.swift # Enum defining character classes
│   └── RacialTrait.swift    # Enum defining character races
├── Views/
│   ├── MainMenu.swift       # (Referenced in rpg_managerApp.swift) Likely the main UI screen
│   └── ActorView.swift      # (ActorFormView) SwiftUI view for character creation/editing form
└── (Other supporting files and assets)


---

## ✅ Usage

1.  Launch the **Rpg-Manager** app on your device or simulator.
2.  Navigate through the `MainMenu` (or initial view) to the character creation section.
3.  Fill out the character creation form (`ActorFormView`), providing details such as:
    * Name
    * Class (selected from a Picker)
    * Race (selected from a Picker)
    * Level, Mana, HP, Armor Class, Experience (entered into text fields)
4.  Save the new character. The data will be persisted using SwiftData.
5.  View, manage, or (eventually) use your created characters within the app.

---

## 🧱 Data Models In-Depth

* **`Actor` Model**:
    * Represents a fully defined character.
    * Stores attributes like `name` (String), `actorClass` (CharacterClass), `level` (Int), `mana` (Int), `maxHP` (Int), `currentHP` (Int), `armorClass` (Int), `experience` (Int), `race` (RacialTrait), `isAlive` (Bool), `isActive` (Bool).
    * Includes methods like `attack()`, `characterIsAlive()`, and various getters/setters.
    * Managed by SwiftData for persistence.

* **`PendingActor` Model**:
    * Seems to be an intermediate representation of a character, possibly used in forms before validation or finalization.
    * Stores many attributes as `String` (e.g., `pendingLevel`, `pendingMana`, `pendingMaxHP`), which could simplify text input handling.
    * Also includes `pendingName` (String), `pendingActorClass` (CharacterClass), `pendingRace` (RacialTrait), `pendingIsAlive` (Bool), `pendingIsActive` (Bool).
    * Has its own `attack()` and `characterIsAlive()` methods.
    * Also managed by SwiftData.

---

## 🛠 Troubleshooting

* **Build Fails**: Ensure you have the latest compatible version of Xcode installed. Clean the build folder (Product > Clean Build Folder) and try again.
* **Data Not Saving**:
    * Verify the `ModelContainer` in `rpg_managerApp.swift` is correctly configured with the `Actor` and `PendingActor` schemas.
    * Ensure that instances of `Actor` or `PendingActor` are being correctly created and that the context is saved if manual saving is implemented.
* **UI Issues**: If views are not displaying as expected, check the SwiftUI layout code in the respective view files (e.g., `ActorView.swift`, `MainMenu`).

---

## 📄 License

*(You can add your chosen license here, e.g., MIT License)*

This project is licensed under the MIT License - see the LICENSE.md file for details (if applicabl