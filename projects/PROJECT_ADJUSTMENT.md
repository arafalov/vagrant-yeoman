Fixes to make after creating a project with yeoman
==================================================

After you setup a yeoman project, you may need to change two things in **Gruntfile.js**:

+   Comment out test task for normal build - Chrome does not seem to be available on this Ubuntu box. It is at the real end as part of default task's dependencies
+   Grunt needs to listen on 0.0.0.0, not just localhost - the instructions are in the Gruntfile.js itself, just search for **localhost**
