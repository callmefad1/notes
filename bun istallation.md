# bun istallation

### Powershell:

- `powershell -c "irm bun.sh/install.ps1|iex"`     
- **Add to system path**:
  - `[System.Environment]::SetEnvironmentVariable(`
  `"Path",`
  `[System.Environment]::GetEnvironmentVariable("Path", "User") + ";$env:USERPROFILE\.bun\bin",`
  `[System.EnvironmentVariableTarget]::User`
  `)`
- **restart pc**

 