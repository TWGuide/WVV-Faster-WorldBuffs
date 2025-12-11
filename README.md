# Winter Veil Vale - Faster World Buffs Guide

### This guide will show how you can hand in snowballs to Tiny Timflake at the Winter Veil Vale during the Winter Veil christmas event.

## Step 1 - LazyPig
Download [LazyPig](https://github.com/Otari98/_LazyPig) directly from the TurtleWoW Launcher under the `ADDONS` tab.  
Alternatively, if using [GitAddonsManager](https://woblight.gitlab.io/overview/gitaddonsmanager/), by pasting `https://github.com/Otari98/_LazyPig.git` into it.

> [!NOTE]
> LazyPig adds and changes the functionality of a lot of things in-game, so I suggest checking it's config via /lp in case there's any strange behavior that occurs as a result of installing LazyPig

## Step 2 - Interact
Download and install the [Interact](https://github.com/luskanek/Interact) client mod. If using the TurtleWoW launcher, make sure to enable the mod under the `MODS` tab as well.

<details>   
<summary>Detailed installation steps (from Interact's github)</summary>
  
1. Download the latest release from [here](https://github.com/luskanek/Interact/releases/latest/download/Interact.zip)
2. Move the content of the `.zip` file to your World of Warcraft folder (overwrite if prompted)
3. In your World of Warcraft folder, open `dlls.txt` (included with [VanillaFixes](https://github.com/hannesmann/vanillafixes)) and add `Interact.dll` on a new line at the end of the `dlls.txt` file. Save and close the file.

> If you are using a launcher that has built-in mods support you can skip the next steps

4. Launch the game using `VanillaFixes.exe`
5. Once in-game, open the keybindings menu and assign a key to either `Interact` or `Interact (auto-loot)`
</details>

> [!IMPORTANT]
> Once Interact is installed, you must set a keybind as your interact key.  
> The Keybinds must be `Alt + Mouse Wheel Up` and `Alt + Mouse Wheel Down` for either `Interact` or `Interact (auto-loot)`.  
> Without the Alt + Scrollwheel bind, LazyPig won't auto-complete the snowball hand-in quest at Tiny Timflake.  

<details>
  <summary>Key Bindings Menu</summary>
    
  ![Keybinds](https://i.imgur.com/HKAnUzg.png)
    
</details>

Once the keybinds are set up, you are technically already done, now just visit Tiny Timflake with snowballs in your inventory, hold Alt, then scroll up/down quickly to hand in up to around 30 snowballs per second :)

## Step 3 - Vendor Macro
To speed things up at the snowball vendor, you can use this macro:  
```lua
/script BuyMerchantItem(2, 8)
```
> [!IMPORTANT]
> This will purchase two stacks (40x) of Snowball (8x of whatever's in slot 2 of the vendor frame)  
> The nature of this macro means it will buy 8x of whatever is in slot 2 for **ANY** vendor, this could be useful to some, but it's worth mentioning, so that you don't buy random stuff accidentally.  

An alternative (and more safe) macro which scans the vendor for the `Snowball` item specifically, can also be used:
```lua
/run local a={"Snowball",8} for i=1,GetMerchantNumItems() do if GetMerchantItemInfo(i)==a[1] then BuyMerchantItem(i,a[2]) end end 
``` 

This macro will scan the vendor for `Snowball` and buy two stacks (8x of Snowball x5), similar to the first macro, but this macro can never buy anything other than `Snowball` specifically, unless you change the `{"Snowball",8}` to something else.

And with that, the guide is over, thanks for checking it out! Happy world buff spamming, folks!

Made by Peachoo/Ieaiaio/Shadorei/Entertragedy
