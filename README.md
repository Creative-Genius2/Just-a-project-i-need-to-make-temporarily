The name “Xoleon” comes from a corruption and combination of the terms xor and rol (for context, Xor (also called “exclusive or” where bits get compared to eachother to see if the result is either true (one.) or false (zero.).) and rol (specifically in the context of Pokémon, rol is the process that comes after xor, where bits get rotated to the left within a 16 or 15 bit field.) together make the cipher that help to obfuscate the text layer of Pokémon games in Gen IV-VII), which is combined with eon as a suffix. Xoleon itself serves as the spiritual successor to ndspy, but this can be also likened to Eevee, the Evolution Pokémon.

---

methodology on Pokémon text decryption for DS and 3DS ROMS:
- Gen IV: compared to future generations, Gen IV contains the full character map (tradition carried from gens 1-3), along with 9-bit packed trainer names and control codes, which are all locked by a XOR that shifts within a 16 bit field. (this is then added to a MULT of 0x91BD3. This ultimately scrambles the character map and trainer names until the xor is decrypted properly. The 9-bit packing uses 15 usable bits per word, but that's a separate layer after decryption.)  
- Gen V–VII: Is ultimately similar to Gen IV, but is stripped down, with the xor now shifting within a 16-bit field, which is multiplied (instead of being added to.) by a MULT of 0x2983

also contains support for:  
- The container in the 3DS filesystem
- NCCH header parsing 
- Navigation of RomFS 
- GARC parsing 
- LZ11 compression and decompression 
- ExeFS parsing (includes code.bin and ARM11 support)  
- CRO/CRS module parsing (Equivalent to the overlays in the Nintendo DS)  
- MSBT (Meant for support of any video games that use text outside of Pokémon, which uses Game Freak's/Nintendo's encryption layer)  
—  
Planned aspects of Xoleon:

- CGFX/BCH: (resources related to the models on the 3ds)  
- BCSAR/BCSTM/BCWAV: (deferred until audio within Gen IV/V ends up being tackled)  
—  
Not fucking needed:
- ARM9 (now systems-related processing that was formerly used natively in the DS filesystem but was abstracted outward)
