The Boot Prompt
---------------

Usage: [LABEL [kernel options] [nuke="dwipe [dwipe options]"]]

Dwipe Options:

--autonuke Be really sure.
-m --method The wipe method to use.
-r --rounds The number of times to run the method.
--verify The verification level.

Dwipe Methods:

dod522022m American Department of Defense 5220.22-M standard wipe.
dodshort dod3pass DoD short wipe, passess 1,2,7 from the standard wipe.
gutmann Peter Gutmann's wipe.
ops2 RCMP TSSIT OPS-II standard wipe.
prng random PRNG stream wipe.
quick zero Quick erase.

Verification Levels:

0 off Do not read anything back from the device.
1 last Check whether the device is empty after wiping.
2 all Check whether all passes were written properly.

Notes:

* The rounds option does not apply to to the quick method. This method
always runs one round.

* Use at least four rounds with the prng method. Using eight rounds with
the prng method is recommended.

* The last pass of every method fills the device with zeros, except the
ops2 method which fills the device with a random stream on its last pass.

