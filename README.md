Mini Circuit Lab ⚡

A tiny, minimal React lab to visualize Ohm's Law in a single loop. Built for teaching, not for complexity.

React
Size
License

🔗 Live Demo
Drop the single HTML file into Vercel / Netlify / GitHub Pages. No build step needed for the artifact version.



✨ What It Does

A simple series circuit:

[ Battery ] → [ Switch ] → [ Resistor ] → [ Bulb / LED ] → back to Battery

Interactive controls:
Voltage Slider: 1.5V – 12V (Battery)
Resistance Slider: 10Ω – 1000Ω
Switch: Click to open / close circuit

Live Physics:
Current: I = V / R
Power: P = V * I
Bulb brightness = proportional to current, with glow filter
Warning when I > 100mA → bulb blown (red)

When switch is open: Open Circuit – No Current



🚀 Getting Started

No install (artifact version)
Just open mini-circuit-lab.html in browser.

React version
git clone https://github.com/yourusername/mini-circuit-lab.git
cd mini-circuit-lab
npm install
npm start

Build:
npm run build



🧠 How It Works

Single component, SVG circuit drawing:

State: voltage, resistance, isSwitchClosed
Calculate:
  const current = isSwitchClosed ? voltage / resistance : 0; // Amps
   const power = voltage * current;
   const brightness = Math.min(1, current * 100);
SVG: 4 wires forming rectangle, components placed on each side
Bulb fill opacity + CSS filter: drop-shadow for glow

No external chart libs, no physics engine — just Ohm's Law.



🗂️ Project Structure
/src
  App.jsx      # Circuit SVG + sliders + calculations
  index.css    # Tailwind minimal
public
  index.html
README.md



🎯 Use Cases
School physics demo for Ohm's Law
First-day electronics class
Portfolio mini-project
Embed in blog / Notion via iframe



🔮 Ideas to Extend
Add parallel resistor switch
Add capacitor charging animation
Add multimeter probes
Save circuit as image




👨‍💻 Author
Made as a companion to WirelessNet Sim Lab — for teaching fundamentals before wireless.

V = I × R — that's it.
