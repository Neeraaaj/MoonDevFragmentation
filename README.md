# Approach

In order to enhance the readability, maintainability, and reusability of the codebase, a modular and organized structure has been adopted. This approach involves dissection of the code into custom hooks and components.

## Custom Hooks

### 1. **useWallet Hook:**
   - Manages wallet-related state and functions.
   - Extracts wallet-related logic, such as connecting wallets and handling balances.

### 2. **useChainSelector Hook:**
   - Handles chain selection modal state and related functions.
   - Decouples the logic for chain selection to improve code readability.

### 3. **useAppSupplies Hook:**
   - Manages application supplies state and provides functions to fetch and manipulate data.
   - Separates supplies-related logic for better organization.

### 4. **useEthersSigner Hook:**
   - Provides an ethers signer based on the specified chain ID.
   - Abstracts away ethers-related logic for ease of use.

### 5. **useAppToast Hook:**
   - Manages toast notifications and provides functions to display different types of toasts.
   - Isolates toast-related logic for cleaner code.

### 6. **Other Custom Hooks:**
   - Additional custom hooks for specific functionalities, each focusing on a specific concern for modularization.

## Components

### 1. **BurnPage Component:**
   - The main component for the burn page.
   - Utilizes various custom hooks for wallet, chain selection, supplies, ethers signer, toast, etc.
   - Dissects logic into smaller, manageable parts for improved readability.

### 2. **BurnStatsContainer Component:**
   - A component responsible for rendering burn statistics.
   - Can be reused in different parts of the application for consistent display.

### 3. **BurnButtonBar Component:**
   - A component encapsulating the UI and logic related to burning tokens.
   - Enhances code readability by separating the burn button and input logic.

### 4. **Other Reusable Components:**
   - Components such as `Button`, `CircularProgress`, `AppIcon`, `AppTooltip`, `AppExtLink`, etc., which are reused across different parts of the application.

# Why this code should be fragmented like this?

## 1.Ease of Maintenance: Each custom hook or component addresses a specific concern, making it easier to understand, maintain, and update. Developers can focus on one piece of functionality at a time.
## 2.Reusability: Modular code can be reused in different parts of the application, promoting consistency and reducing redundancy.
## 3.Component Reusability: Components designed with a specific purpose can be reused across different parts of the application, maintaining a consistent look and feel.
## 4.Code Maintenance: A modular structure facilitates ongoing maintenance, updates, and bug fixes. Changes are localized, minimizing the risk of unintended consequences. 

