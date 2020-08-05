# HockEOS
Get realtime NHL stats pushed to EOS using OSC from NodeRed running on a separate machine.

!! THIS README IS NOT COMPLETE !!

<h1>About</h1>
This started off as a project for me to make a LAN based status board for NHL games. Then, Scott Tusing joked that I should make it also send the data to EOS. So, here we are.

<h2>What You Need</h2>
- Eos Family Console (or Nomad)
- Network
- Computer running NodeRED (must have internet connection)

<h2>Installation Instructions (COMING SOON)</h2>
- NodeRED Instructions Go Here
- Need OSC and MOMENT modules for NodeRED - Details here.
- Network Requirements Go Here
- EOS Network Settings Go Here

<h2>Eos Magic Sheet Setup</h2>

<h3>Subscribe to Team</h3>
  Tell: HockEOS which team you want to see game data for:
    <pre>/nhl/get/team=XXX
        where xxx= 3-digit team code</pre>

   
  Tells HockEOS how often to send you updates:
    <pre>/nhl/set/interval=YY
        where YY is a number of seconds</pre>



<h3>Things you can display</h3>
    <pre>/nhl/out/game/start/</pre>
