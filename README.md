# SwiftStyleSheet

Creates a StyleSheet to integrate in your Swift projects for easier, simpler, safer and consistent colors and fonts management. By providing it a JSON file listing all colours and fonts you are using in your app, this script generates enums and helper functions that you can easily include in your project.

## Installation

From the same folder in your Terminal, simply run:
~~~~
xcrun swift main.swift styleSheet.json StyleSheet.swift
~~~~
This will use the file `styleSheet.json` as input to generate the file `StyleSheet.swift` that you can straight away include in your project.

## Usage

Once the style sheet file is included in your project, you can use the generated enums to set a colour / font on your UILabels, UIButtons and any other UI element.

For example, if in your JSON file your declared a list of text styles and colours as such:
~~~~
{
  "textStyles": {
    "Body": {
      "font": "AvenirNext-Medium",
      "size": 14,
      "colour": "OffBlack"
    }
  },
  "colours": {
    "OffBlack": [
      20,
      20,
      20
    ]
  }
}
~~~~

In your code you can simply type:
~~~~
self.myLabel.font = TextStyle.body.font
self.myLabel.textColor = TextStyle.body.color
~~~~

For a UIView background color you can also type:
~~~~
self.myView.backgroundColor = UIColor(commonColor: .offBlack)
~~~~

## Author

Julien Ducret - <brocoo@gmail.com>

Follow me on Twitter [@jbrocoo](https://twitter.com/jbrocoo)

## License

This code is under Apache licence.
