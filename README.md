
# Canvacord Rank Card with Gradient Colors

This project provides a customizable rank card template for use with Canvacord,a Discord bot that generates images dynamically.
With this template, you can create visually appealing rank cards for your Discord server members,
with the added feature of gradient colors for a more dynamic and eye-catching design.

## Features

- **Customizable**: Easily customize the rank card template to match the style and branding of your Discord server.
- **Gradient Colors**: Add gradient colors to the rank card background for a more visually striking appearance.
- **Dynamic Generation**: Use Canvacord to dynamically generate rank cards for server members based on their ranks and statistics.

## Installation

1. Clone or download this repository to your local machine.
2. Install Canvacord using npm:
   ```
   npm install canvacord
   ```
3. Customize the `index.js` file to define the rank card template and gradient colors.
4. Run the script using Node.js:
   ```
   node index.js
   ```

## Usage

Once you have customized the rank card template and gradient colors, you can integrate it with your Discord bot powered by Canvacord. Here's how you can use it:

1. Set up your Discord bot and integrate Canvacord with it.
2. Use the Canvacord API to generate rank cards for server members.
3. Pass the member's rank and statistics to the rank card template.
4. Generate the rank card image using Canvacord and send it to the Discord server.

## Examples

```javascript
const Canvacord = require('canvacord');
const fs = require('fs');

// Define rank and statistics
const rank = 5;
const username = 'ExampleUser';

// Generate rank card with gradient background
const rankCard = new Canvacord.Rank()
    .setAvatar('avatar_url')
    .setCurrentXP(500)
    .setRequiredXP(1000)
    .setLevel(10)
    .setRank(rank)
    .setUsername(username)
    .setStatus('dnd')
    .setBackground('gradient', 'color1', 'color2');

rankCard.build()
    .then(buffer => fs.writeFileSync('rank_card.png', buffer))
    .catch(console.error);
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Canvacord for providing the framework for dynamic image generation.
- Discord for providing the platform for building and hosting communities.

