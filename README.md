# Soccer Team Rotation Schedule Generator

A React-based web application that generates fair rotation schedules for 7-a-side intramural soccer games with 7-10 players.

**[Live Demo](https://jrozra200.github.io/seven_aside_intramural/)**

## Overview

This tool helps coaches and team organizers create balanced playing time schedules for soccer games with:
- 4 quarters divided into 8 half-quarters
- 6 field positions + 1 goalkeeper (7 players on field)
- Automatic rotation to ensure fair playing time
- Customizable player names and goalkeeper assignments

## Features

- **Flexible Team Sizes**: Support for 7-10 players
- **Fair Rotation Algorithm**: Automatically distributes playing time evenly across all players
- **Goalkeeper Management**: Assign different goalkeepers per quarter (plays entire quarter)
- **Visual Schedule**: Clear display of who plays, who's benched, and when substitutions occur
- **Playing Time Summary**: Track total half-quarters played per player

## How It Works

### Game Structure
- **4 Quarters** with substitutions at half-time (8 total half-quarters)
- **7 Players** on field at any time (6 field + 1 goalkeeper)
- **Goalkeepers** stay for the entire quarter (both half-quarters)
- **Field players** rotate at each half-quarter break

### Rotation Algorithm
The schedule prioritizes:
1. Players with fewer plays in the current quarter
2. Players with fewer total plays overall
3. Players who haven't played recently

This ensures everyone gets approximately equal playing time while minimizing consecutive benching.

## Usage

1. **Select Number of Players** (7-10)
2. **Enter Player Names** (optional, defaults to "Player 1", "Player 2", etc.)
3. **Assign Goalkeepers** for each quarter
4. **Generate Schedule** - Click the button to create the rotation

The schedule will display:
- Which players are on the field each half-quarter
- Who stays on the field vs who substitutes
- Who's on the bench
- Total playing time per player

## Quick Start

Visit the live application at: **https://jrozra200.github.io/seven_aside_intramural/**

No installation required - just open the link and start creating rotation schedules!

## Development Setup

This is a single-file React component. To run it locally or customize it:

1. Clone the repository:
   ```bash
   git clone https://github.com/jrozra200/seven_aside_intramural.git
   cd seven_aside_intramural
   ```

2. Set up a React project with Tailwind CSS
3. Install dependencies:
   ```bash
   npm install lucide-react
   ```
4. Import and use the `SoccerRotation` component

### Dependencies
- React (with hooks)
- Tailwind CSS (for styling)
- lucide-react (for icons)

## Deployment

This site is deployed on GitHub Pages. To deploy your own version:

1. Fork this repository
2. Enable GitHub Pages in repository Settings → Pages
3. Select the branch to deploy (usually `main`)
4. Your site will be available at `https://[your-username].github.io/seven_aside_intramural/`

## Example Output

For a 10-player game, the schedule shows:
- Each quarter with its designated goalkeeper
- First and second half lineups for each quarter
- Substitution indicators showing who comes on/off
- Players who remain on the bench for entire quarters
- Summary showing each player's total half-quarters played (out of 8)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve the rotation algorithm or add new features.
