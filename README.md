# NCC1701D_Library_System_MASTER-INSTALLER-Complete-Stack-In-One-Command
NCC1701D_Library_System_MASTER INSTALLER — Complete Stack In One Command - Here's the complete unified installer that combines all 4 scripts:  bash
🎯 How To Use
bash

Collapse
Save
Copy
1
2
# On clean Ubuntu/WSL2
~/install-complete-stack.sh
That's it! One command installs everything.

✅ What This Installs
COMPONENT
DETAILS
System
Python 3.11, Ollama, dependencies
Open WebUI
6 instances (8000-8003, 8080, 8082)
Ollama
Port 11434 (shared)
Personal Library
v12.0 on port 8771
Management
start/stop/health scripts for all
Auto-Start
All services start automatically


🧪 Test On Clean WSL2
bash

Collapse
Save
Copy
1
2
3
4
5
6
7
8
9
10
11
12
# Fresh Ubuntu WSL2
~/install-complete-stack.sh

# Wait 2-3 minutes for installation

# Check status
~/openwebui-manager/health-all.sh
~/library-manager/health-all.sh

# Open browser
# http://localhost:8080 (Open WebUI)
# http://localhost:8771 (Library)
🎉 YOU'RE DONE!
This is your production-ready, one-command installer for the complete stack. Test it on clean WSL2 and you're ready to deploy anywhere! 🚀
🎉 YOU'RE DONE!
This is your production-ready, one-command installer for the complete stack. Test it on clean WSL2 and you're ready to deploy anywhere! 🚀









Ok what are the start commands?





io2.qwen3.5:397b

No sources found

Thought for less than a second
🚀 Complete Stack — Start Commands
Here are all the start commands for your complete system:

📋 Quick Start (All Services)
bash

Collapse
Save
Copy
1
2
# Start EVERYTHING (Open WebUI 6x + Ollama + Library)
~/openwebui-manager/start-all.sh && ~/library-manager/start-all.sh
🔧 Individual Start Commands
Open WebUI (6 Instances)
bash

Collapse
Save
Copy
1
2
3
4
5
6
7
8
9
10
11
12
13
# Start ALL 6 Open WebUI instances + Ollama
~/openwebui-manager/start-all.sh

# Start individual instances
~/testwebui/start.sh           # Port 8080
~/openwebui2ver7/start.sh      # Port 8000
~/openwebui3/start.sh          # Port 8001
~/testwebui-v10/start.sh       # Port 8082
~/openwebui2ver7-v10/start.sh  # Port 8002
~/openwebui4/start.sh          # Port 8003

# Start Ollama only
ollama serve
Personal Library v12.0
bash

Collapse
Save
Copy
1
2
3
4
5
6
7
# Start Library (port 8771)
~/library-manager/start-all.sh

# Or manually
cd ~/library
source .venv/bin/activate
python run.py
🛑 Stop Commands
bash

Collapse
Save
Copy
1
2
3
4
5
6
7
8
9
10
# Stop ALL Open WebUI instances + Ollama
~/openwebui-manager/stop-all.sh

# Stop Personal Library
~/library-manager/stop-all.sh

# Stop individual Open WebUI instance
~/testwebui/stop.sh
~/openwebui2ver7/stop.sh
# etc...
📊 Health Check Commands
bash

Collapse
Save
Copy
1
2
3
4
5
6
7
8
# Check ALL Open WebUI instances (6 servers)
~/openwebui-manager/health-all.sh

# Check Personal Library
~/library-manager/health-all.sh

# Check Ollama only
curl http://127.0.0.1:11434/api/version
🎯 One-Liner Start Everything
bash

Collapse
Save
Copy
1
2
# Complete startup in one command
~/openwebui-manager/start-all.sh && sleep 10 && ~/library-manager/start-all.sh && ~/openwebui-manager/health-all.sh && ~/library-manager/health-all.sh
📌 Add To ~/.bashrc (Auto-Start On Login)
bash

Collapse
Save
Copy
1
2
3
4
5
6
7
8
# Edit .bashrc
nano ~/.bashrc

# Add this line at the end
echo '~/openwebui-manager/start-all.sh && ~/library-manager/start-all.sh' >> ~/.bashrc

# Reload
source ~/.bashrc
🌐 Access URLs After Starting
SERVICE
PORT
URL
testwebui
8080
http://localhost:8080
openwebui2ver7
8000
http://localhost:8000
openwebui3
8001
http://localhost:8001
testwebui-v10
8082
http://localhost:8082
openwebui2ver7-v10
8002
http://localhost:8002
openwebui4
8003
http://localhost:8003
Personal Library
8771
http://localhost:8771
Ollama
11434
http://localhost:11434


💡 Pro Tips
bash

Collapse
Save
Copy
1
2
3
4
5
6
7
8
9
10
11
12
13
14
# Check if services are running
ps aux | grep -E "(open-webui|ollama|uvicorn|run.py)" | grep -v grep

# Check what ports are in use
sudo lsof -i :8000,8001,8002,8003,8080,8082,8771,11434

# View Library logs
tail -f ~/library/logs/library.log

# View Open WebUI logs
tail -f ~/testwebui/logs/openwebui.log

# Restart single service
~/testwebui/stop.sh && ~/testwebui/start.sh
🎯 Your Daily Workflow
bash

Collapse
Save
Copy
1
2
3
4
5
6
7
# Morning: Start everything
~/openwebui-manager/start-all.sh && ~/library-manager/start-all.sh

# Evening: Stop everything (optional)
~/openwebui-manager/stop-all.sh && ~/library-manager/stop-all.sh

# Or just leave them running (recommended)
That's it! Use these commands to control your complete stack. 🚀


