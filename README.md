vagrant-yeoman
==============

Setting up Yeoman development environment under Vagrant. Basic steps: 

1. Install Vagrant, VirtualBox
2. Clone/copy this repository to new *host-side* project directory
3. Run **vagrant up** - have a cup of cofee, while VM is downloading and is being setup
4. Run **vagrant ssh** to connect to client VM
5. Inside **projects** directory, create a sub-directory for actual yeoman project. For example **yeoman-test**
6. Run **yo angular** - agree to all default choices
7. As per PROJECT_ADJUSTMENT.md:
    - Change **localhost** to **0.0.0.0** in Gruntfile.js (vi is available or use whatever you want on host-side)
    - Comment out test call for default **grunt** action
8. Run **grunt server**
9. Load **http://localhost:9000/** on your real machine - ports are proxied through
10. Edit **yeoman-test/app/scripts/controllers/main.js**
11. Add *Vagrant* to the list of technologies
12. See it update on the screen - demonstrating round-trip and isolation
13. Run **grunt** to compile production version of the website
14. **exit** from the VM
15. Run **vagrant suspend** to stop VM running

