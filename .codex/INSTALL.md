# Installing Supergos for Codex

Quick setup to enable supergos skills in Codex.

## Installation

1. **Clone supergos repository**:
   ```bash
   mkdir -p ~/.codex/supergos
   cd ~/.codex/supergos
   git clone https://github.com/ThePeppy/supergos.git .
   ```

2. **Create personal skills directory**:
   ```bash
   mkdir -p ~/.codex/skills
   ```

3. **Update ~/.codex/AGENTS.md** to include this supergos section:
   ```markdown
   ## Supergos System

   <EXTREMELY_IMPORTANT>
   You have supergos. Supergos teach you new skills and capabilities. RIGHT NOW run: `~/.codex/supergos/.codex/supergos-codex bootstrap` and follow the instructions it returns.
   </EXTREMELY_IMPORTANT>
   ```

## Verification

Test the installation:
```bash
~/.codex/supergos/.codex/supergos-codex bootstrap
```

You should see skill listings and bootstrap instructions. The system is now ready for use.