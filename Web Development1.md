# Web Development: Browsers -

Cross browser testing is the practice of making sure that the web sites and web apps that you create work across an acceptable number of web browsers. As a web developer, it is your responsibility to make sure that not only your projects work, but they work for all your users, no matter what browser, device, or added more helping tools they are using.

We should explain a few bits of words/word choices here. To start with, when we talk about places/locations "working cross browser", we are really saying that they should provide an acceptable user experience across different browsers. It is possibly OK for a site to not deliver the same experience on all browsers, as long as the basic ability to do things is (easy to get to, use, or understand) in some way. On modern browsers you might get something (full of life and energy/moving), 3D and shiny, whereas on older browsers you might just get a flat graphic representing the same information. As long as the site owner is happy with this, then you have done your job.
On the other hand, it is not OK for a site to work fine for sighted users, but be completely (unable to be used or understood) for visually damaged/weakened users because their screen reader computer program can't read any of the information stored on it.

Second, when we say "across an acceptable number of web browsers", we don't mean 100% of the browsers in the world -- this is just about impossible. You can make some (based on knowledge and learning) calls as to what browsers and devices your users will be using (as we'll discuss in the second article in the series -- see Gotta test them all?), but you can't (promise that something will definitely happen or that something will definitely work as described) everything. As a web developer, you need to agree a range of browsers and devices that the code definitely needs to work on with the site owner, but beyond that, you need to code (in a way that protects against harm) to give other browsers the best chance possible of being able to use your content. This is one of the great challenges of web development.


# Issues-

There are many different reasons why cross browser issues happen, and note that here we are talking about issues where things behave different across different browsers / devices / (looking at websites on) preferences. Before you even get to cross browser issues, you should have already fixed out bugs in your code (see (finding and correcting mistakes in) HTML, (finding and correcting mistakes in) CSS, and What went wrong? (finding the source of problems) JavaScript from previous topics to refresh your memory if needed).

Sometimes browsers have bugs, or put into use features differently. This situation is a lot less bad than it used to be; back when IE4 and Netscape 4 were competing to be the most in control/most common browser in the 1990s, browser companies (in a carefully-planned way)used things differently to each other to try to gain competitive advantage, which made life hell for developers. Browsers are much better at following standards these days, but differences and bugs still creep through sometimes.

Some browsers may have different levels of support for technology features to others. This is unavoidable when you are dealing with bleeding edge features that browsers are just getting round to put into using, or if you have to support really old browsers that are no longer being developed, which may have been frozen (i.e. no more new work done on them) a long time before a new feature was even invented. As an example, if you want to use cutting edge JavaScript features in your site, they might not work in older browsers. If you need to support older browsers, you might have to not use those, or convert your code to old fashioned (the set of rules for forming language) using some kind of cross-collector/maker where needed.

Some devices may have restrictions that cause a web site to run slowly, or display badly. For example, if a site has been designed to look nice on a desktop PC, it will probably look tiny and be hard to read on a mobile device. If your site includes a load of big animations, it might be ok on a high spec tablet, but might be slow or jerky on a low end device.


# Planning-

In the first planning phase, you will probably have (more than two, but not a lot of) planning meetings with the site owner/client (this might be your boss, or someone from an external company you are building a website for), in which you decide/figure out exactly what the website should be -- what content and ability to do things should it have, what should it look like, etc. At this point you'll also want to know how much time you have to develop the site --what is their deadline, and how much are they going to pay you for your work? We won't going to much detail about this, but cross-browser issues can have a serious effect on such planning.

Once you've got an idea of the needed/demanded featureset, and what technologies you will likely build these features with, you should start exploring the target audience -- what browsers, devices, etc. will the target audience for this site be using? The client might already have data about this from previous research they've done, e.g. from other websites they own, or from previous versions of the web site you are now working on. If not, you will be able to get a good idea by looking at other sources, such as usage stats for competitors, or countries the site will be serving. You can also use a bit of (gut feeling or deep-down opinion).

So for example, you might be building a (buying things online) site that serves customers in North America. the site should work completely in the last few versions of the most popular desktop and mobile (iOS, Android, Windows phone) browsers -- this should include Chrome(and Opera as it is based on the same making/giving engine as Chrome), Firefox, IE/Edge, andSafari. It should also provide an acceptable experience on IE 8 and 9, and be (easy to get to, use, or understand) with WCAG AA (following the law/doing as you're told).

Now you know your target testing (raised, flat supporting surfaces), you should go back and review the needed/demanded featureset and what technologies you are going to use. For example, if the (buying things online) site owner wants a WebGL-powered 3D tour of each product built into the product pages, they will need to accept that this just won't work in IE versions before 11. You'd have to agree to provide a version of the site without this feature to users of older IE versions.


# Development-

Now on to the development of the site. You should split the different parts of the development into modules, for example you might split the different site areas up -- homepage, product page, shopping cart, payment workflow, etc. You might then further subdivide these -- put into use common site header and footer, put into use product page detail view, put into use (constant/not going away) shopping cart widget, etc.

There are multiple general (success plans/ways of reaching goals) to cross browser development, for example:

Get all the ability to do things working as closely as possible in all target browsers. This may involve writing different code paths that reproduce ability to do things in different ways aimed at different browsers, or using a Polyfill to imitate any missing support using JavaScript or other technologies, or using a library that allows you to write a single bit of code and then does different things in the background depending on what the browser supports.

Accept that some things aren't going to work the same on all browsers, and provide different(acceptable) solutions in browsers that don't support the full ability to do things. Sometimes this is unavoidable due to device restrictions -- a movies widescreen isn't going to give the same visual experience as a 4" mobile screen, (without any concern about/having nothing to do with) how you program your site. Accept that your site just isn't going to work in some older browsers, and move on. This isOK, if your client/user base is OK with it.
(usually/ in a common and regular way) your development will involve a combination of the above three approaches. The most important thing is that you test each small part before committing it -- don't leave all the testing till the end!

# Testing-

After each putting into use phase, you will need to test the new ability to do things. To start with, you should make sure there are no general issues with your code that are stopping your feature from working:

Test it in a couple of stable browsers on your system, like Firefox, Safari, Chrome, or IE/Edge.
Do some low fi (how easy something is to get to, use, or understand) testing, such as trying to use your site with only the keyboard, or using your site via a screen reader to see if it is able to be traveled through.
Test on a mobile (basic technology that runs a computer), such as Android or iOS.

At this point, fix any problems you find with your new code.

Next, you should try expanding your list of test browsers to a full list of target audience browsers and start (focusing mental and physical effort) on weeding out cross browser issues (see the next article for more information on deciding/figuring out your target browsers). For example:

Try to test the latest change on all the modern desktop browsers you can -- including Firefox, Chrome, Opera, IE, Edge, and Safari on desktop (Mac, Windows, and Linux, in a perfect world).
Test it in common phone and tablet browsers (e.g. iOS Safari on iPhone/iPad, Chrome and Firefox on iPhone/iPad/Android),
Also do tests in any other browsers you have included inside your target list.

The most low fi option is to just do all the testing you can by yourself (pulling in team mates to help out if you are working in a team). You should try to test it on real physical devices where possible.

If you haven't got the means to test all those different browser, operating system, and device combinations on physical hardware, you can also make use of emulators (copy a device using software on your desktop computer) and virtual machines (software that allows you to copy multiple operating system/software combinations on your desktop computer). This is avery popular choice, especially in some situations -- for example, Windows doesn't let you have many versions of Windows installed simultaneously on the same machine, so using multiple virtual machines is often the only option here.

Another option is user groups -- using a group of people outside your development team to test your site. This could be a group of friends or family, a group of other workers, a class ata local university, or a professional user testing setup, where people are paid to test out yoursite and provide results.

Finally, you can get smarter with your testing using auditing or automation tools; this is a(reasonable/showing good judgment) choice as your projects get bigger, as doing all this testing by hand can start to take a really long time. You can set up your own testing automation system (Selenium being the popular app of choice) that could for example load your site in some different browsers, and:

see if a button click causes something to happen successfully (like for example, a map displaying), displaying the results once the tests are completed
take a (picture made by a computer of its screen) of each, allowing you to see if a layout is the same across the different browsers.

You can also go further than this, if wished. There are commercial tools available such as Sauce Labs, Browser Stack, and LambdaTest that do this kind of thing for you, without you having to worry about the setup, if you wish to invest some money in your testing. It is also possible to set up a (surrounding conditions) that automatically runs tests for you, and then only lets you check in your changes to the central code storage place if the tests still pass.

# The Fixes-

Once you've discovered a bug, you need to try to fix it.

The first thing to do is to narrow down where the bug happens as much as possible. Get as much information as you can from the person reporting the bug -- what (raised, flat supporting surface)(s), device(s), browser version(s), etc. Try it on almost the same setups (e.g. the same browser version on different desktop (raised, flat supporting surfaces), or a few different versions of the same browser on the same (raised, flat supporting surface)) tosee how widely the bug (continues to exist/continues to do hard or annoying things).

It might not be your fault -- if a bug exists in a browser, then hopefully the vendor will quickly fix it. It might have already been fixed -- for example if a bug is present in Firefox release 49, but it is no longer there in Firefox Nightly (version 52), then they have fixed it. If it is not fixed, then you may want to file a bug (see Reporting bugs, below).

If it is your fault, you need to fix it! Finding out the cause of the bug involves the same(success plan(s)/way(s) of reaching goals) as any web development bug (again, see (finding and correcting mistakes in) HTML, (finding and correcting mistakes in) CSS, and What went wrong? (finding the source of problems) JavaScript). Once you've discovered what is causing your bug, you need to decide how to work around it in the particular browser it is causing problems in -- you can't just change the problem code completely/total, as this may break the code in other browsers. The general approach is usually to fork the code in some way, for example use JavaScript feature detection code to detect situations in which a problem feature doesn't work, and run some different code in those cases that does work.

Once a fix has been made, you'll want to repeat your testing process to make sure your fix is working OK, and hasn't caused the site to break in other places or in other browsers.
