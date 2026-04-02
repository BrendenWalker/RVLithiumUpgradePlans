Phase 1 - upgrade charging systems to support LI or Lead Acid

Stock OEM: time-delay relay paralleled house + chassis (removed for this design).
One physical Victron Orion XS; connections split below for clarity.

        ENGINE BAY / CHASSIS SIDE
        --------------------------

   [Chassis Battery +]
            |
            |  (short cable, ≤12")
            |
        [100A MIDI Fuse]
            |
            |  4 AWG +
            |
            |------------------------------.
                                           |
                                           |
                              [Victron Orion XS 50A]
                              (mounted under seat)
                                           |
                                           |
            |------------------------------'
            |
            |  4 AWG -
            |
   [Chassis Ground]  (or battery negative)



        COACH / HOUSE SIDE
        -------------------

                              [Victron Orion XS 50A]
                                           |
                                           |
            |------------------------------.
            |                              |
            |  4 AWG +                     |
        [80A MIDI Fuse]                   |
            |                              |
            |                              |
     [House Battery +]                     |
                                           |
                                           |
                                   4 AWG -
                                           |
                                           |
                                 [Chassis Ground]
                                 (or house battery -)
