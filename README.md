# babelOnNextJS

This is a concise guide on how to get babbel set up on NextJS so that debugging styled components is far more readable in browser inspect.

## Install Babel in your Project 

In the terminal:
```yarn add -D babel-plugin-styled-components```

## Create a .babelrc file

In the terminal:
touch .babelrc

## Finally, write this to your .babelrc file

Navigate to .babelrc in your file explorer and open it. Then add:
```
{
  "presets": [
    "next/babel"
  ],
  "plugins": [
    [
      "styled-components",
      {
        "ssr": true,
        "displayName": true,
        "preprocess": false
      }
    ]
  ]
}
```

# You're done!

When you inspect your styled-components should be far more readable when inspected in your browser!

