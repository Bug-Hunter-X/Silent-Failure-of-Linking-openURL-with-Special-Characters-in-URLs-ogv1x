# Silent Failure of Linking.openURL with Special Characters

This repository demonstrates a bug in Expo's `Linking.openURL` function where it silently fails when provided with URLs containing certain special characters.  The issue is that no error is thrown, making debugging challenging.  This example focuses on the '+' character, but other special characters might cause similar issues.

## Steps to Reproduce

1. Clone this repository.
2. Run `expo start`.
3. Tap the button to open a URL with a '+' character.
4. Observe that the URL does not open and no error is reported in the console.  

## Solution

The solution involves URL encoding the URL before passing it to `Linking.openURL`. This ensures that special characters are properly handled.
