# emailmagic

Take a `mailto:` link and make it better! Instead of just letting the browser deal with it, give your users a bit of a choice as to what system to use. Uses Bootstrap 4 -- if you want to style it a different way, just save `emailmagic.js` in your project and tweak `getModalContent`. BTW, the original usage of the `mailto:` link stays the same, so if this fails to load for some reason the link will follow the default behavior.

<p align="center">
    <img width="307" height="423" src="https://raw.githubusercontent.com/itsthejoker/emailmagic/master/images/openemailin.png">
</p>

I recently saw two new options for handling `mailto:` links: https://mailgo.dev/ and https://mailtoui.com/, though both options do roughly the same thing. I didn't really like either of them, and thought "I can write it so it looks best on my sites".

### So I did.

I use Bootstrap for most everything, and overal UI unity is important to me. Rather than try to bend one of the pre-existing solutions to my will, I decided to try and reimplement from the ground up. Here are some thoughts on the two solutions I found:

mailgo:

- uses JS to build the links when you click the buttons, so all you see in the link preview is `javascript:void(0);`, which is super not helpful
- very clean look, but sacrifices functionality because it's not clear that anything is a button
- forces `mailgo.dev` at the bottom of the modal

mailtoui:

- generates real links for each button so the link preview functions
- not as pretty, but much clearer styling shows what is clickable
- completely unrecognizable UI that doesn't fit in with anything
- forces `Powered by MailtoUI` at the bottom of the modal

I don't like that they both advertise themselves -- a library should unobtrusively add to an experience and the blurbs at the bottom make it _really obvious_ that this isn't actually part of the site.

This is / was a great opportunity to try and make something for myself as a JS learning project. I don't intend to maintain this, but I'm putting it out if someone wants to use it. Check out `example.html` if you'd like to see it in action; it should be able to handle any standard `mailto:` link. 
