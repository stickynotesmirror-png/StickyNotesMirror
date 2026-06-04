Sticky Notes Mirror installers
==============================

Files
-----
- StickyNotesMirrorSetup.exe  - interactive EXE installer (Inno Setup)
- StickyNotesMirrorSetup.msi  - MSI package for deployment tools

Interactive install
-------------------
EXE:
  StickyNotesMirrorSetup.exe

MSI:
  msiexec /i StickyNotesMirrorSetup.msi

Silent install
--------------
EXE:
  StickyNotesMirrorSetup.exe /VERYSILENT /SUPPRESSMSGBOXES /NORESTART /SP-

MSI:
  msiexec /i StickyNotesMirrorSetup.msi /qn /norestart

Silent uninstall
----------------
EXE:
  "C:\Program Files\Sticky Notes Mirror\unins000.exe" /VERYSILENT /SUPPRESSMSGBOXES /NORESTART

MSI:
  msiexec /x StickyNotesMirrorSetup.msi /qn /norestart

Logging
-------
MSI log:
  msiexec /i StickyNotesMirrorSetup.msi /qn /norestart /l*v install.log

EXE log:
  StickyNotesMirrorSetup.exe /LOG=install.log

Notes
-----
- EXE installer supports optional autostart and launch-after-install in the wizard UI.
- MSI is intended for deployment systems and standard Windows Installer workflows.
- Application settings are stored per Windows user under LocalAppData after first run.
