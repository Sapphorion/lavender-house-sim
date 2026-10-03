# Lavender House

A first-person life sim about chosen family, made for an LGBTQIA+ audience.

You've just moved into a queer share house in Gqeberha, South Africa. Four housemates already live there. They have their own needs, moods, routines, relationships and opinions, and they get on with their lives whether you're watching or not. Walk around in first person, look after yourself, and get to know them. When you talk to them, they talk back.

## Play

Open `index.html` in a browser, or enable GitHub Pages for this repo (Settings → Pages → deploy from the `main` branch, root folder).

| Action | Desktop | Phone |
| --- | --- | --- |
| Look around | Move the mouse (the game grabs it when you move in; click the view to grab it again), or drag | Drag on the screen |
| Move | `W` `A` `S` `D`, or `↑` `↓`; `Shift` to sprint | Joystick |
| Turn without the mouse | `←` `→` | — |
| Use an object or interact with a housemate | `E` | **Use** |
| Chat with a housemate | `T` | **Talk** |
| Stop what you're doing | Move, or `Space` | Move |
| Free the mouse / close a menu | `Esc` | — |

Game speed (pause, 1×, 3×, 8×) is in the clock panel. Time speeds up while you're busy with an activity, and a lot while you sleep. The game saves in your browser.

## The household

| Housemate | Pronouns | Who they are |
| --- | --- | --- |
| Thandi Mokoena | she/her | Trans lesbian ER nurse. The steady one. Early bird, bookworm. |
| Mia van Wyk | she/her | Bi line cook who dreams of her own bistro. Thandi's partner of three years. |
| Ren Adeyemi | they/them | Nonbinary, pansexual painter and part-time barista. Night owl. Single. |
| Kai Naidoo | he/him | Gay QA tester at a game studio. Shy, then fiercely loyal. Single. |

You create your own character: name, pronouns (including neopronouns or custom pronouns), gender, an optional "about you" line your housemates will know, and which Pride flag flies on the garden pole (12 to choose from).

## How it works

- **Needs.** Everyone (you included) has Hunger, Energy, Bladder, Hygiene, Fun and Social. They drop over time, and mood comes from them.
- **Utility AI.** Each object in the house advertises what it gives (the stove offers a lot of Hunger, the easel offers Fun). Housemates score every option by how much it would help their lowest needs, their personal likes, the time of day and the walking distance, then pick the best one. They path-find around the house on a tile grid.
- **Social life.** Housemates seek each other out when they're lonely, have conversations with speech bubbles, and grow their relationships. When they're lonely they may come and find you, too.
- **Conversation.** Chats with housemates use live AI when the game runs on claude.ai. Each reply is grounded in the housemate's personality, current needs and mood, the time of day, their recent memories and your pronouns. Outside claude.ai, housemates reply with built-in lines.
- **Relationships and romance.** Compliments, jokes, hugs and conversations change how a housemate feels about you. Flirting respects each housemate's orientation: Thandi and Mia are a committed couple, Ren is open to any gender, and Kai is into men.

## Roadmap

- [ ] Live AI replies outside claude.ai (a small server holding the API key, so the key never ships in public code)
- [ ] Multiplayer: friends join the same house as live housemates alongside the AI ones
- [ ] More rooms, objects and household events (Pride march prep, family dinners, load shedding nights)
- [ ] Customisable appearance for your character
- [ ] Careers, skills and longer-term goals

## Tech

A single HTML file with [three.js](https://threejs.org/) r128 loaded from cdnjs. No build step. Rendering uses tone-mapped physically based materials, real-time sun shadows through the windows, a day–night sky, and static geometry merged into a few draw calls so it runs on laptops with integrated graphics.

## License

Copyright © 2026 Sapphorion. All rights reserved. See [LICENSE](LICENSE).
