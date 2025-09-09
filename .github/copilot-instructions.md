# Empty Repository
This is currently an empty repository with minimal structure. It contains only basic files (README, LICENSE, .gitignore) and no functional code.

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively

### Current Repository State
- This is an EMPTY repository with no source code, build system, or functionality
- Contains only: README.md, LICENSE (Apache 2.0), and .gitignore (Go template)
- No dependencies to install, no code to build, no tests to run
- The .gitignore suggests this may become a Go project in the future

### Initial Setup Commands
- `git status` -- verify repository state
- `ls -la` -- list all files (should show only README.md, LICENSE, .gitignore, .git/)
- No build commands available - repository is empty
- No test commands available - repository is empty  
- No dependencies to install - repository is empty

### Available Development Tools
The environment includes these pre-installed development tools:
- Go 1.24.7 linux/amd64: `go version`
- Node.js v20.19.5: `node --version` 
- npm 10.8.2: `npm --version`
- Python 3.12.3: `python3 --version`
- pip 24.0: `pip --version`
- Docker 28.0.4: `docker --version`
- GNU Make 4.3: `make --version`
- Git: `git --version`

### If/When Code Is Added
Based on the Go .gitignore template, this repository may become a Go project. When code is added:

#### For Go Projects (if Go code is added):
- Go is already installed: `go version` shows go1.24.7 linux/amd64
- Initialize Go module: `go mod init [module-name]`
- Install dependencies: `go mod tidy` 
- Build: `go build ./...` -- NEVER CANCEL: Go builds can take 5-15 minutes. Set timeout to 30+ minutes.
  - With no Go files: shows "warning: './...' matched no packages" (normal behavior)
- Test: `go test ./...` -- NEVER CANCEL: Go tests can take 5-30 minutes. Set timeout to 45+ minutes.
  - With no Go files: shows "no packages to test" and exits with code 1 (normal behavior)
- Format: `go fmt ./...`
- Lint: `go vet ./...` and consider `golangci-lint run`
- Install additional Go tools if needed: `sudo apt-get update && sudo apt-get install -y [package-name]`

#### For Other Project Types:
Available tools in environment:
- Node.js v20.19.5 and npm 10.8.2: Check for package.json then `npm install && npm run build && npm test`
- Python 3.12.3 and pip 24.0: Check for requirements.txt then `pip install -r requirements.txt && python -m pytest`
- GNU Make 4.3: Check for Makefile then `make` or `make build && make test`
- Docker 28.0.4: Check for Dockerfile then `docker build -t app .`

## Validation

### Current Validation Steps
- Verify repository contains only expected files: `ls -la` should show README.md, LICENSE, .gitignore, .git/
- Verify README content: `cat README.md` should show "# -"
- Verify license: `head -5 LICENSE` should show Apache License Version 2.0
- No functional validation possible - repository is empty

### Future Validation Steps (when code is added)
- ALWAYS run build and test commands after making changes
- ALWAYS validate that new code follows the project's existing patterns
- ALWAYS test any new functionality manually before committing
- For Go projects: run `go fmt`, `go vet`, and tests before committing
- For web applications: test in browser and take screenshots of changes
- For CLI applications: test with sample inputs and verify outputs

## Common Tasks

### Repository Information
```bash
# Current repository structure
ls -la
.
..
.git/
.gitignore  # Go template
LICENSE     # Apache 2.0
README.md   # Contains "# -"

# Git status check
git status
# Should show clean working tree

# View README content
cat README.md
# Output: # -

# View gitignore
cat .gitignore
# Shows Go-specific ignore patterns including *.exe, *.dll, *.so, *.dylib, etc.
```

### When Adding New Code
- ALWAYS update this copilot-instructions.md file when adding build systems, dependencies, or functionality
- Add specific build commands with proper timeout warnings
- Document any special setup requirements or dependencies
- Include validation scenarios specific to the application type
- Update the "Common Tasks" section with project-specific commands

### Build Time Expectations (when applicable)
- NEVER CANCEL: Build operations can take significant time
- Go builds: typically 5-15 minutes, set timeout to 30+ minutes
- Node.js builds: typically 2-10 minutes, set timeout to 20+ minutes  
- Docker builds: typically 5-30 minutes, set timeout to 45+ minutes
- Always wait for completion rather than canceling long-running operations

## Important Notes
- This repository is currently EMPTY - no code exists to build, test, or run
- Instructions will need updates when functional code is added
- The Go .gitignore suggests future Go development but no Go code currently exists
- Always verify actual project structure before assuming build commands will work
- When code is added, measure actual build times and update timeout recommendations accordingly
- No GitHub Actions workflows exist yet - add .github/workflows/ when CI/CD is needed