# b-clothing-native-fix

Due to a recent FiveM build update, there is a bug in the `b-clothing` script that affects its functionality. Until `b-dev` releases an official fix, we are providing a quick workaround to resolve the issue. Please follow the instructions below to apply the fix.

## Quick Fix Instructions

1. **Open `fxmanifest.lua`**  
   Locate the line that contains `client_script` and add `'client/overwrite.lua'` to the list.  
   It should look like this:
   ```lua
   client_script { 'client/client.lua', 'client/overwrite.lua' }
   ```

2. **Create a new Lua file**  
   Open the `client` folder from the script and create a new file named `overwrite.lua`.

3. **Add the following code**  
   Open `overwrite.lua` and paste the following code:
   ```lua
   DrawMarker = function(a, b, c, d, e, f, g, h, i, j, k, l, m, o, p)
     DrawMarker_2(a, b, c, d, e, f, g, h, i, j, k, l, m, o, p)
   end
   ```

4. **Save and restart the script**  
   Save the changes and restart the script. The issue should now be resolved, and it should work perfectly again!

## Credits
This quick fix was provided by [LowBoBYT](https://github.com/LowBoBYT).  
Join the community on Discord: [https://discord.gg/xeonrp](https://discord.gg/xeonrp)
