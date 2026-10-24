Dependencies: customtkinter, selenium, python-chess, keyboard, edge-tts

Target: Chess.com (Bot / Computer Matches)

Overview
Haunted Stockfish is an atmospheric desktop assistant and Stockfish telemetry engine wrapper I built using CustomTkinter, Selenium DOM extraction, and Python.

Instead of just making a basic Stockfish wrapper, I built this to combine multi-line engine analysis with a custom-drawn Tkinter visualizer canvas, real-time threat/fear calculation based on evaluation swings, neural voice synthesis, and dynamic move quality tracking.

Features
Animated Haunted Scene Canvas:

Real-time vector-drawn canvas featuring drifting ghosts, bats, fog, flickering pumpkins, and dancing skeletons.

Fear Meter Dynamics: The canvas dynamically reacts to Stockfish's evaluation. When your position gets threatened, the sky turns red, bats speed up, and lightning strikes.

Interactive particles and click-to-burst bat effects.

DOM Overlay Injection:

Reads piece coordinates and board orientation directly from the page DOM using Selenium.

Renders color-coded target arrows (Green = Best, Yellow = 2nd, Red = 3rd) directly onto the chess board with adjustable opacity and style configurations (Arrows vs. Highlight Squares).

Neural TTS & Persona Voice Engine:

Multi-voice persona engine featuring Cryptkeeper, Dracula, and Witch personalities.

Asynchronous speech queue that prevents voice overlap during fast play.

Context-aware audio triggers for checks, captures, promotions, castling, and checkmate.

Opponent Move Analyzer & Persona Roaster:

Tracks evaluation differences on every turn.

Classifies move quality (Brilliant, Great, Inaccuracy, Mistake, Blunder).

Triggers the active voice persona to comment on or roast opponent blunders.

Thematic Opening Recognition:

Built-in opening recognition for aggressive tactical lines including the Halloween Gambit, Stafford Gambit, and Fried Liver Attack.

Engine Telemetry & Control Panel:

Full control over Stockfish engine parameters: Elo limiting (1320-3000), skill levels, depth limits, and search time.

Real-time spirit log displaying FEN coordinates, board state debug output, and evaluation swings.

Global Hotkeys & Controls:

Hotkey binding to replay move narration on demand.

Multi-mode arrow reveals (Instant, Delayed, or Step-by-step via keypress).

Installation & Usage
Dependencies:
Make sure you have Python 3.10+ and Google Chrome installed. Install required packages:

DOS
python -m pip install -U selenium python-chess customtkinter keyboard edge-tts
Engine Setup:
Put your stockfish.exe binary in the same folder as chess_assistant.py.

Running the Script:

DOS
python chess_assistant.py
Usage:

Hit "Awaken the Assistant" to attach/launch Chrome with debugging enabled.

Head over to [chess.com/play/computer](https://chess.com/play/computer) and start playing.

Settings
Settings automatically persist to assistant_settings.json:

color: Board orientation detection (Auto, White, Black).

lines: Engine PV lines to calculate (1-3).

time / depth: Stockfish calculation limits.

persona: Active TTS voice personality.

scene_level / sparks: Visual customizability options.
