# Qwen3 Coder Playground

This project is a playground for experimenting with Qwen3 Coder, featuring a 3D game built with Three.js and Cannon.js that integrates with Supabase for high score tracking.

📹 Full YouTube Guide: [Youtube link](https://www.youtube.com/watch?v=f6sxu7--GDQ&list=PLE9hy4A7ZTmpGq7GHf5tgGFWh2277AeDR&index=16)

🚀 X Post: [X link](https://x.com/ShenSeanChen/status/1948749109894033593)

💻 Launch Full Stack Product: [Github Repo](https://github.com/ShenSeanChen/launch-mvp-stripe-nextjs-supabase)

☕️ Buy me a coffee: [Cafe Latte](https://buy.stripe.com/5kA176bA895ggog4gh)

## Project Structure

- `3d-game/` - Contains the 3D game implementation
  - `index.html` - The main game file with all HTML, CSS, and JavaScript
  - `supabase-setup.sql` - SQL script to set up the Supabase database
- `.env.local` - Environment variables for API keys and configuration

## 3D Game: Space Collector

The game is a simple 3D space collector where you control a spaceship to collect stars while avoiding red obstacles. 

Features:
- Arrow keys or WASD to move the spaceship
- Collect yellow stars to increase your score
- Avoid red obstacles that reduce your lives
- High score tracking with Supabase integration
- Physics-based movement with Cannon.js
- 3D graphics with Three.js

## Setup Instructions

### Prerequisites

- Node.js 20 or higher
- An Alibaba Cloud account for Qwen3 Coder API access

### Setting up Qwen3 Coder

Follow these guidelines based on the [official Qwen3 Coder blog post](https://qwenlm.github.io/blog/qwen3-coder/):

1. Install Node.js (version 20 or higher):
   ```bash
   curl -qL https://www.npmjs.com/install.sh | sh
   ```

2. Install Qwen Code globally:
   ```bash
   npm i -g @qwen-code/qwen-code
   ```

3. Set up environment variables in `.env.local` or your shell:
   ```bash
   export OPENAI_API_KEY="your_api_key_here"
   export OPENAI_BASE_URL="https://dashscope-intl.aliyuncs.com/compatible-mode/v1"
   export OPENAI_MODEL="qwen3-coder-plus"
   ```

### Getting Qwen API Keys

To use Qwen models, you need to get API keys from Alibaba Cloud DashScope:

1. Visit the [Alibaba Cloud website](https://www.aliyun.com/) and log in to your account (or register if you don't have one)
2. Navigate to the DashScope platform
3. Access the API Key Management section in your dashboard
4. Create a new API key or view an existing one
5. Securely store your API key and use it in your environment variables

For more detailed instructions, refer to the [API Key Management documentation](https://help.aliyun.com/zh/dashscope/developer-reference/api-key-management)

### Claude Code Integration (Optional)

If you want to use Claude Code alongside Qwen:

1. Install Claude Code:
   ```bash
   npm install -g @anthropic-ai/claude-code
   ```

2. Configure either the proxy API:
   ```bash
   export ANTHROPIC_BASE_URL=https://dashscope-intl.aliyuncs.com/api/v2/apps/claude-code-proxy
   export ANTHROPIC_AUTH_TOKEN=your-dashscope-apikey
   ```

3. Or use the router customization:
   ```bash
   npm install -g @musistudio/claude-code-router
   npm install -g @dashscope-js/claude-code-config
   ccr-dashscope
   ```

### Running the Project

1. Clone this repository
2. Set up your environment variables in `.env.local`
3. Open `3d-game/index.html` in a web browser
4. Optionally, run `qwen` in your terminal to access the Qwen3-Coder CLI

## Supabase Setup

The game uses Supabase for high score tracking. To set up your own Supabase instance:

1. Create a Supabase project at [supabase.com](https://supabase.com/)
2. Run the SQL script in `3d-game/supabase-setup.sql` in your Supabase SQL editor
3. Update the Supabase URL and key in `3d-game/index.html`:
   ```javascript
   const supabaseUrl = 'your_supabase_url';
   const supabaseKey = 'your_supabase_anon_key';
   ```

## Usage

After installation and configuration:

1. Open the 3D game by opening `3d-game/index.html` in your browser
2. Use arrow keys or WASD to control your spaceship
3. Collect yellow stars to increase your score
4. Avoid red obstacles to preserve your lives
5. Enter your name and save your score to the leaderboard
6. Run `qwen` in your terminal for access to the Qwen3-Coder CLI for coding assistance

## Contributing

This is a playground project for experimenting with Qwen3 Coder. Feel free to fork and modify as needed for your own experiments.
