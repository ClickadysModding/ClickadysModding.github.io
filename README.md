<html><head><base href="https://amazing-scripthub.example"><meta charset="UTF-8"><meta name="viewport" content="width=device-width, initial-scale=1.0"><title>flow | Scripts</title><style>
:root {
  --primary: #0066ff;
  --secondary: #1f1f1f;
  --accent: #00b2ff;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
  background: #121212;
  color: white;
  min-height: 100vh;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
}

nav {
  background: var(--secondary);
  padding: 1rem;
  box-shadow: 0 2px 10px rgba(0,0,0,0.3);
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
  color: var(--primary);
  text-shadow: 0 0 10px rgba(0, 102, 255, 0.7);
  animation: logoGlow 2s ease-in-out infinite alternate;
}

@keyframes logoGlow {
  from {
    text-shadow: 0 0 10px rgba(0, 102, 255, 0.7);
  }
  to {
    text-shadow: 0 0 20px rgba(0, 102, 255, 1), 0 0 30px rgba(0, 102, 255, 0.7);
  }
}

.script-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}

.script-card {
  background: var(--secondary);
  border-radius: 10px;
  padding: 1.5rem;
  transition: transform 0.2s;
  cursor: pointer;
}

.script-card:hover {
  transform: translateY(-5px);
}

.script-header {
  display: flex;
  align-items: center;
  margin-bottom: 1rem;
}

.script-icon {
  width: 40px;
  height: 40px;
  margin-right: 1rem;
  fill: var(--accent);
}

.copy-btn {
  background: var(--primary);
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 5px;
  cursor: pointer;
  margin-top: 1rem;
  transition: all 0.2s;
  box-shadow: 0 0 15px rgba(0, 102, 255, 0.5);
  text-shadow: 0 0 5px rgba(255, 255, 255, 0.5);
  animation: glow 1.5s ease-in-out infinite alternate;
}

.rainbow-btn {
  animation: rainbow 3s linear infinite;
}

@keyframes rainbow {
  0% { background: #ff0000; }
  17% { background: #ff8000; }
  33% { background: #ffff00; }
  50% { background: #00ff00; }
  67% { background: #0000ff; }
  83% { background: #8000ff; }
  100% { background: #ff0000; }
}

@keyframes glow {
  from {
    box-shadow: 0 0 10px rgba(0, 102, 255, 0.5);
  }
  to {
    box-shadow: 0 0 20px rgba(0, 102, 255, 0.8);
  }
}

.copy-btn:hover {
  background: #0052cc;
  box-shadow: 0 0 25px rgba(0, 102, 255, 0.8);
}

.code-preview {
  background: #2a2a2a;
  padding: 1rem;
  border-radius: 5px;
  font-family: 'Courier New', Courier, monospace;
  font-size: 0.9rem;
  color: #e0e0e0;
  max-height: 150px;
  overflow-y: auto;
}

.notification {
  position: fixed;
  bottom: 20px;
  right: 20px;
  background: var(--accent);
  padding: 1rem;
  border-radius: 5px;
  transform: translateY(100px);
  opacity: 0;
  transition: all 0.3s;
}

.notification.show {
  transform: translateY(0);
  opacity: 1;
}

</style><script type="text/javascript" src="https://party.websim.ai/upy_h3u1DGSER4GKNgFEW6OK_KX_o2T62NsQf41J7WVJQUpSP5gExQot66JI3blUJEmgMywxh8gSdHiQd_D-mA=="></script></head><body>
<nav>
  <div class="container">
    <div class="logo">flow | Scripts</div>
  </div>
</nav>

<div class="container">
  <div class="script-grid">
    <div class="script-card">
      <div class="script-header">
        <svg class="script-icon" viewBox="0 0 24 24">
          <path d="M12,2A10,10 0 0,1 22,12A10,10 0 0,1 12,22A10,10 0 0,1 2,12A10,10 0 0,1 12,2M12,4A8,8 0 0,0 4,12A8,8 0 0,0 12,20A8,8 0 0,0 20,12A8,8 0 0,0 12,4M12,6A6,6 0 0,1 18,12A6,6 0 0,1 12,18A6,6 0 0,1 6,12A6,6 0 0,1 12,6M12,8A4,4 0 0,0 8,12A4,4 0 0,0 12,16A4,4 0 0,0 16,12A4,4 0 0,0 12,8Z"/>
        </svg>
        <h3>Speed Boost</h3>
      </div>
      <div class="code-preview">
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
humanoid.WalkSpeed = 50
      </div>
      <button class="copy-btn" data-script="speed">Copy Script</button>
    </div>

    <div class="script-card">
      <div class="script-header">
        <svg class="script-icon" viewBox="0 0 24 24">
          <path d="M13,2V7H16L12,11L8,7H11V2H13M3,13H8V16L12,12L16,16V13H21V11H16V8L12,12L8,8V11H3V13Z"/>
        </svg>
        <h3>Infinite Jump</h3>
      </div>
      <div class="code-preview">
local player = game.Players.LocalPlayer
local uis = game:GetService("UserInputService")

uis.JumpRequest:Connect(function()
   player.Character:FindFirstChildWhichIsA("Humanoid"):ChangeState("Jumping")
end)
      </div>
      <button class="copy-btn" data-script="jump">Copy Script</button>
    </div>

    <div class="script-card">
      <div class="script-header">
        <svg class="script-icon" viewBox="0 0 24 24">
          <path d="M12,4A4,4 0 0,1 16,8A4,4 0 0,1 12,12A4,4 0 0,1 8,8A4,4 0 0,1 12,4M12,14C16.42,14 20,15.79 20,18V20H4V18C4,15.79 7.58,14 12,14Z"/>
        </svg>
        <h3>ESP Player Tracker</h3>
      </div>
      <div class="code-preview">
for i,v in pairs(game.Players:GetPlayers()) do
    if v.Character and v.Character:FindFirstChild("Head") then
        local BillboardGui = Instance.new("BillboardGui")
        local TextLabel = Instance.new("TextLabel")
        
        BillboardGui.Parent = v.Character.Head
        BillboardGui.AlwaysOnTop = true
        BillboardGui.Size = UDim2.new(0, 50, 0, 50)
        BillboardGui.StudsOffset = Vector3.new(0, 2, 0)
        
        TextLabel.Parent = BillboardGui
        TextLabel.BackgroundTransparency = 1
        TextLabel.Size = UDim2.new(1, 0, 1, 0)
        TextLabel.Text = v.Name
        TextLabel.TextColor3 = Color3.new(1, 1, 1)
    end
end
      </div>
      <button class="copy-btn" data-script="esp">Copy Script</button>
    </div>

    <div class="script-card">
      <div class="script-header">
        <svg class="script-icon" viewBox="0 0 24 24">
          <path d="M21,9L17,5V8H10V10H17V13M7,11L3,15L7,19V16H14V14H7V11Z"/>
        </svg>
        <h3>skeet.cc | Universal Aimbot</h3>
      </div>
      <div class="code-preview">
loadstring(game:HttpGet("https://pastebin.com/raw/eCdLeTBh"))()
      </div>
      <button class="copy-btn rainbow-btn" data-script="aimbot">Copy Script</button>
    </div>

    <div class="script-card">
      <div class="script-header">
        <svg class="script-icon" viewBox="0 0 24 24">
          <path d="M12,15.5A3.5,3.5 0 0,1 8.5,12A3.5,3.5 0 0,1 12,8.5A3.5,3.5 0 0,1 15.5,12A3.5,3.5 0 0,1 12,15.5M19.43,12.97C19.47,12.65 19.5,12.33 19.5,12C19.5,11.67 19.47,11.34 19.43,11L21.54,9.37C21.73,9.22 21.78,8.95 21.66,8.73L19.66,5.27C19.54,5.05 19.27,4.96 19.05,5.05L16.56,6.05C16.04,5.66 15.5,5.32 14.87,5.07L14.5,2.42C14.46,2.18 14.25,2 14,2H10C9.75,2 9.54,2.18 9.5,2.42L9.13,5.07C8.5,5.32 7.96,5.66 7.44,6.05L4.95,5.05C4.73,4.96 4.46,5.05 4.34,5.27L2.34,8.73C2.21,8.95 2.27,9.22 2.46,9.37L4.57,11C4.53,11.34 4.5,11.67 4.5,12C4.5,12.33 4.53,12.65 4.57,12.97L2.46,14.63C2.27,14.78 2.21,15.05 2.34,15.27L4.34,18.73C4.46,18.95 4.73,19.03 4.95,18.95L7.44,17.94C7.96,18.34 8.5,18.68 9.13,18.93L9.5,21.58C9.54,21.82 9.75,22 10,22H14C14.25,22 14.46,21.82 14.5,21.58L14.87,18.93C15.5,18.67 16.04,18.34 16.56,17.94L19.05,18.95C19.27,19.03 19.54,18.95 19.66,18.73L21.66,15.27C21.78,15.05 21.73,14.78 21.54,14.63L19.43,12.97Z"/>
        </svg>
        <h3>Infinite Yield</h3>
      </div>
      <div class="code-preview">
loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
      </div>
      <button class="copy-btn" data-script="infinite-yield">Copy Script</button>
    </div>

    <div class="script-card">
      <div class="script-header">
        <svg class="script-icon" viewBox="0 0 24 24">
          <path d="M9,5V9H21V5M9,19H21V15H9M9,14H21V10H9M4,9H8V5H4M4,19H8V15H4M4,14H8V10H4V14Z"/>
        </svg>
        <h3>Dex Explorer</h3>
      </div>
      <div class="code-preview">
loadstring(game:HttpGet("https://raw.githubusercontent.com/ForlornWindow46/Roblox-Scripts/refs/heads/main/customDEX.lua"))()
      </div>
      <button class="copy-btn" data-script="dex">Copy Script</button>
    </div>
  </div>
</div>

<div class="notification" id="notification">
  Script copied to clipboard!
</div>

<script>
document.querySelectorAll('.copy-btn').forEach(button => {
    button.addEventListener('click', () => {
        const scriptContent = button.previousElementSibling.textContent;
        navigator.clipboard.writeText(scriptContent.trim());
        
        const notification = document.getElementById('notification');
        notification.classList.add('show');
        
        setTimeout(() => {
            notification.classList.remove('show');
        }, 2000);
    });
});
</script>
</body></html>
