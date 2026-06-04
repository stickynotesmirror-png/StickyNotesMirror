StickyNotesMirror deployment package

Files:
- StickyNotesMirror.exe
- e_sqlite3.dll
- firebird\x64\fbclient.dll
- firebird\x86\fbclient.dll
- mysql\x64\libmysql.dll
- mysql\x86\libmysql.dll
- VERSION.txt

Requirements:
1. Windows with .NET Framework 4.x
2. If Firebird is used:
   - bundled fbclient.dll can be selected from the local firebird\x64 or firebird\x86 folder
   - reachable Firebird database
3. If MariaDB / MySQL is used:
   - bundled libmysql.dll can be selected from the local mysql\x64 or mysql\x86 folder
   - reachable MariaDB / MySQL server and target database
4. If Microsoft Sticky Notes integration is used:
   - Microsoft Sticky Notes installed
   - plum.sqlite present in the default LocalState folder

First start:
1. Run StickyNotesMirror.exe
2. Open "Database settings" if needed
3. Configure Firebird or MySQL client path and database connection
   - by default the app auto-selects firebird\x64\fbclient.dll on 64-bit Windows
   - by default the app auto-selects firebird\x86\fbclient.dll on 32-bit Windows
   - by default the app auto-selects mysql\x64\libmysql.dll on 64-bit Windows
   - by default the app auto-selects mysql\x86\libmysql.dll on 32-bit Windows
   - you can still override the path manually in Database Settings
4. Use "Test connection" to verify the enabled remote database access
5. Optionally export/import settings between PCs

Notes:
- The app automatically checks startup dependencies
- The app automatically initializes required Firebird tables
- Logs are stored in the local "logs" folder with automatic rotation
- VERSION.txt contains the deployment build timestamp and package details
