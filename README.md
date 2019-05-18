# Scoped Theme Package Issue in Gatsby

Scoped packages (@bkegley/scoped-theme) don't seem to allow component shadowing.

To reproduce:

1. Clone the repo
2. Bootstrap the dependencies - `npx lerna bootstrap`
3. Start the site - `yarn workspace gatsby-starter-default run develop`
4. Toggle the `__experimentalThemes` config in `gatsby-config.js` adn the import statement in `pages/index.js` in `packages/gatsby-starter-default` to test scoped v. non-scoped themes.

The default theme is configured for a button with a green background. The scoped theme overrides it with a red background and the non-scoped theme overrides it with an orange background.