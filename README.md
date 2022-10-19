# REM
Rcilogic Enterprise Microservices

## Description
**REM** - is a boundle of microservices, based on different technologies and provides some useful tools for Enteprise networks (commonly based on `MS Active Directory`)

## Components

### Backend
**[ADAuth](https://github.com/rcilogic/ADAuth)** [`c#`,`ASP.NET Core 6.0`] _(service)_ - provides windows-authentication for specified services. Generates signed **JWT** with user's data

**[REMCommons](https://github.com/rcilogic/REMCommons)** [`swift`] _(library)_ - contains common tools and settings used by other services, e.g. config helpers, db settings, etc.

**[REMAuth](https://github.com/rcilogic/REMAuth)** [`swift`] _(service)_ - main backend auth service. Generates **Redis** session for authentiated users. It also puts session key to users cookie. 

**[REMConnectionTracker](https://github.com/rcilogic/REMConnectionTracker)** [`swift`] _(service)_ Connects to remote servers (targets) using **SSH**, then sends script (**Bash** / **Powershell** / etc) and returns result. Possible target types:
- **IIS** (parsing logs using **Microsoft Log Parser 2.2 COM API**).
