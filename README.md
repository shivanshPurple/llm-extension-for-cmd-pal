<p align=center>
  <img src="./Assets/Logo.png" width="240px"/>
</p>

# <p align=center>LLM Extension for Command Palette</p>

<p align=center>This is an extension for <a href="https://learn.microsoft.com/en-us/windows/powertoys/command-palette/overview">PowerToys Command Palette</a> that allows you to chat with a large language model (LLM) directly.</p>

<p align=center>
  <img alt="GitHub License" src="https://img.shields.io/github/license/lioqing/llm-extension-for-cmd-pal">
  <img alt="GitHub Release" src="https://img.shields.io/github/v/release/lioqing/llm-extension-for-cmd-pal">
</p>

<p align=center>
  <a href="https://apps.microsoft.com/detail/9NPK6KSDLC81">
  	<img src="https://get.microsoft.com/images/en-us%20dark.svg" width="200"/>
  </a>
</p>

> [!NOTE]
>
> The Microsoft store page has been down due to crashes caused by a bug still in investigation, but you may still install the extension directly from Command Palette or from the [Release page](https://github.com/LioQing/llm-extension-for-cmd-pal/releases).

## Demo Video

https://github.com/user-attachments/assets/d8b707a9-b086-470f-8d01-7508091ebd9d

It currently supports the following APIs:

- [Ollama](https://ollama.com/)
- [OpenAI](https://platform.openai.com/docs/overview) (and any other compatible API, such as [Docker Model Runner](https://docs.docker.com/model-runner/))
- [Azure OpenAI](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/overview)
- [Google](https://aistudio.google.com/)
- [Mistral](https://console.mistral.ai/)

## Setup

There is a [YouTube playlist with setup tutorials for different services](https://www.youtube.com/playlist?list=PLtpfYcxJV4LHu0gpKagHWjYR1Lghulnt8).

## Development

To run this extension locally from source:

1.  **Prerequisites**:

    - **Windows SDK 10.0.22621**: Install from the [Windows SDK Archive](https://developer.microsoft.com/en-us/windows/downloads/sdk-archive/).
    - **Windows App Runtime 1.8 Experimental 3**: Download and install the [x64 installer](https://aka.ms/windowsappsdk/1.8/1.8.250610002-experimental3/windowsappruntimeinstall-x64.exe).
    - **.NET 9 SDK**: Ensure you have the .NET 9 SDK installed.

2.  **Enable Developer Mode**:

    - Go to Windows Settings > System > For developers.
    - Toggle **Developer Mode** to **On**.

3.  **Build**:

    ```powershell
    cd LlmExtension
    dotnet build -r win-x64
    ```

4.  **Register**:
    Run this command in PowerShell to register the development build:

    ```powershell
    Add-AppxPackage -Register "bin\Debug\net9.0-windows10.0.22621.0\win-x64\AppxManifest.xml"
    ```

5.  **Restart PowerToys**: Quit PowerToys from the system tray and restart it to load the extension.
