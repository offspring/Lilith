# Lilith

**Free & Native Open Source C++ Remote Administration Tool for Windows**

Lilith is a console-based ultra light-weight RAT developed in C++. It features a straight-forward set of [commands](#commands) that allows for near complete control of a machine.

Features
---
* Remote Command Execution via
  * CMD
  * Powershell
  * **Any** other console app
* Extreme Modularity (see [this](#modularity))
* Multiple Connections
* Low Latency & Bandwith use
* Auto-Install
* Startup Persistence
* Self-Erases
* Error-Handler with logs

Modularity
---
The modularity and expandability of this RAT are what it's been built on. That's how it manages to stay very compact, light-weight and fast. You can download other utilities like password recovery or keylogging tools via Powershell scripts (link to some useful scripts will follow soon) and them execute the program as if it were running on your own machine. You can then upload the results of those (also with a ps script) or evaluate them on the spot (via the `type` command) in cmd.

Commands
---
|Command|Syntax|Comment|
|-------|------|---------|
|connect|`connect <clientID>` (`connect 0`)|Connects to a Client|
|exitSession|`exitSession`|Exits current session|
|switchSession|`switchSession <clientID>` (`switchSession 2`)|Switches to another Client|
|remoteControl|`remoteControl <C:\program.exe>` OR `remoteControl cmd`|[More Info](#remotecontrol)|
|remoteControl|`remoteControl`|Exits remoteControl if already in remoteControl|
|restart|`restart`|Restarts the Client|
|kill|`kill`|Quits the Client|

  ![Demo Image](/images/demo.png)

General Description
---
At the core of this RAT lies it's unique ability to remotely execute commands via CMD, Powershell and almost all console-based applications. It has the capabilities to automatically install on startup and clean up behind itself. It also features an error-handler that logs any issues. As of now, it is not 100% stable. Under 'normal' conditions it runs smoothly and without any disturbances, but severe irregularities in input (i.e. messing around with it *a lot*) may cause crashes. This will be resolved in the near future.

Requirements
---
* None!
* Supported Operating Systems (32/64-bit)
  * Windows XP SP3
  * Windows Server 2003
  * Windows Vista
  * Windows Server 2008
  * Windows 7
  * Windows Server 2012
  * Windows 8/8.1
  * Windows 10

[To-Do](https://github.com/werkamsus/lilith/blob/master/todo.md)
---

# More Info on Commands

remoteControl
---
Shortcuts are: `cmd`, `pws`, `pws32` which stand for Command Prompt, Powershell and Powershell 32-Bit respectively. You can use these instead of a full path to the executable. Example: `remoteControl pws` will remote-control `C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe`.
