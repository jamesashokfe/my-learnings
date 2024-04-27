Wordpress Themes
- On activating a theme, `theme.json` is parsed for various config settings set by the developer.
- Any settings manually updated by the user from Global styles (through Wordpress UI) is stored in the database.
- The settings in the db overrides the initial settings present in the `theme.json`
- Any block specific settings will override the Global styles.
- `theme.json < Global Styles < Block level settings`
