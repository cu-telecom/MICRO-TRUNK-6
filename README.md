# Micro Trunk 6

This adapter breaks out the telephone lines on an RJ21 connector into 6 "trunk" ports made up of 4 lines, presented as 8p8c (RJ45) connectors using the [T568A wiring scheme](https://docs.cutel.net/technical/wiring/).

It's primarily designed for use with the Cisco VG224 Voice Gateways and has been designed in such a way that it won't foul devices above or below the gateway when racked, but may work with other devices.

It was created for a couple reasons:

1) Smaller, less dense deployments might not want all 24 lines broken out in one location. This adapter lets you use standard 4 pair "CAT5" cable to distribute telephone lines over longer distances, and potentially daisy chain subscriber break outs.
2) It removes the need for an RJ21 cable. These can be expensive and hard to come by, or just too bulky and unwieldy when you want to lab something.

To keep costs down, the connectors are sourced from AliExpress. You may find you can procure connectors with the same footprint from other more reputable vendors.

# Revisions

## v0.1

### Construction

You'll need:

- 2x 2mm M3 Nylon Spacer
- 2x 4mm M3 Nylon Spacer
- 2x Bolts:
	- 13-15mm M3 or 4-40 UNC bolts for friction fit mounting
	- 3/4" 4-40 UNC bolts for screw mounting
- 2x Nuts
- 6x Vertical 8p8c - https://www.aliexpress.com/item/32918645271.html
- 1x 50 pin Male RJ21 - https://www.aliexpress.com/item/1005006204411796.html
 
### Quirks

The first revision has a few "quirks" that might be positives or negatives depending on your application.

 #### The 8p8c connector pins are exposed on the back
 
 Whilst the VG224 will be protected against short circuits and other transients, a curious or misplaced finger might come into contact with "Ring Voltage" which is known to give a painful but usually non-lethal shock. This probably isn't appropriate for situations where "the public" might have access to the adapter.

On the plus side, the lack of rear insulator plate simplifies construction and lowers the cost, and will probably be fine for lab use.

#### Screwing the adapter into the VG224 can be challenging

Due to the layout of the insulator board, spacers, and connector, it can be difficult to line everything up to screw the adapter into the mounts on the VG224.

If you have a strong desire to screw it into the mounts, I'd suggest doing it once, ideally with the VG224 removed from the rack, and leaving it on there.

Alternatively, the adapter will remain in place with friction perfectly well if its not going to have the cables yanked.

#### Size

The above "quirks" mean the board is relatively compact. Fixing the quirks will require a larger board, although it'll still fit in the 1U footprint. 


## v0.2

The v0.2 attempts to address some of the above quirks by adding a rear insulator and modifying the spacers and mounting to make it easier to screw into the VG224 connector.

It's still in the design phase.

# License 

This project is licensed under the MIT license

