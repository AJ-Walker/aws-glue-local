AWS Glue Local Development Setup
This repository contains local development configurations for AWS Glue. To get full IntelliSense, code completion, and method signature details in VS Code without running a heavy Docker container, follow the steps below.

Getting Started
1. Prerequisites
Python 3.10+ (Matching your Glue runtime version)

VS Code with the Python (Pylance) extension installed.

2. Installation
Instead of manually managing local paths, you can install the Glue libraries directly into your virtual environment. This allows VS Code's language server to index the functions and classes.

Bash
# Create a virtual environment (recommended)
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install the Glue libraries directly from the source
pip install git+https://github.com/awslabs/aws-glue-libs.git
3. VS Code Configuration
To ensure VS Code uses the correct environment for code completion:

Open your Glue script folder in VS Code.

Press Ctrl+Shift+P (or Cmd+Shift+P on Mac).

Type "Python: Select Interpreter".

Choose the interpreter inside your .venv folder.

Features Enabled
By installing the library via pip, you gain access to:

Auto-complete: Suggestions for GlueContext, DynamicFrame, and Job methods.

Go to Definition: Ctrl + Click on any Glue method to see the underlying Python source code.

Type Checking: Real-time feedback on parameter types and missing arguments.

License Note
The AWS Glue libraries are licensed under the Amazon Software License (ASL). This setup is intended for development and testing purposes in conjunction with Amazon Web Services.
