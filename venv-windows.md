# Venv-Windows

This guide outlines common PIP commands for managing Python packages.

- **Create a virtual environment named 'myvenv':**
    ```
    python -m venv myvenv
    ```

- **Activate on Windows (replace 'myvenv' with your virtual environment name)**
    ```
    myvenv\Scripts\activate.bat
    ```

- **Deactivate the virtual environment (works across platforms)**
    ```
    deactivate
    ```

## Overcoming "Execute Command Permission" Issues on Windows

**Problem:** When attempting to activate your virtual environment on Windows, you might encounter an error related to execution policies.

**Solution:** Windows has a security feature called the **Execution Policy** that can restrict the execution of scripts. To resolve this issue, follow these steps:

1. **Open PowerShell as Administrator:**
   - Press `Win + X` and select `Windows PowerShell (Admin)`.

2. **Check the Current Execution Policy:**
   - Run the following command to see your current policy:   

     ```bash
     Get-ExecutionPolicy
     ```

3. **Set the Execution Policy to Allow Scripts to Run:**
   - If the policy is set to something restrictive (e.g., "Restricted"), change it to a less restrictive policy like "RemoteSigned" to allow local scripts to run:
     ```bash
     Set-ExecutionPolicy RemoteSigned
     ```
   - Confirm the change by typing `Y` and pressing Enter.

4. **Reactivate the Virtual Environment:**
   - Now you should be able to activate your virtual environment without issues:
     ```bash
     myvenv\Scripts\activate.bat
     ```

**Note:** Changing the execution policy is a system-wide change. If you need to revert it back, use the following command:
```bash
Set-ExecutionPolicy Restricted