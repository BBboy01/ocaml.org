---
title: 'An Overview of our Current Activities '
description: From the early days of OCamlPro, people have been curious about our plans;
  they were asking how we worked at OCamlPro and what we were doing exactly. Now that
  we have started releasing projects more regularly, these questions come again. They
  are very reasonable questions, and have resolved to be mo...
url: https://ocamlpro.com/blog/2013_02_18_overview_of_current_activities
date: 2013-02-18T13:19:46-00:00
preview_image: URL_de_votre_image
featured:
authors:
- "\n    \xC7agdas Bozman\n  "
source:
---

<p>From the early days of OCamlPro, people have been curious about our plans; they were asking how we worked at OCamlPro and what we were doing exactly. Now that we have started releasing projects more regularly, these questions come again. They are very reasonable questions, and have resolved to be more public and communicate more regularly. This post covers our activities from the beginning of 2013 and updates are scheduled on a monthly basis.</p>
<h2>OCamlPro ?</h2>
<p>OCamlPro has been created to promote the use of OCaml in the industry. In order to do so, we provide a wide range of services targeted at all stages of typical software projects: we train engineers and we improve the efficiency and usability of the OCaml compiler and tools, we help design new projects, advise on which open-source software components to use and how, we help deliver OCaml software projects and we do custom software development. One extra focus is the increase of the accessibility of OCaml for beginners and students.</p>
<p>Our customers are well-known industrial users such as <a href="http://www.janestreet.com/">Jane-Street</a>, <a href="http://www.citrix.com/">Citrix</a> and <a href="http://www.lexifi.com/">Lexifi</a> but we also help individual developers lost in the wild of non-OCaml environments inter-operate OCaml with other components. We also believe that collaborative R&amp;D projects are a great opportunity to make existing companies discover OCaml and its benefits to their products and we are involved in several of them (see below).</p>
<p>Our engineering team is steadily growing (currently 9 full-time engineers in a joint lab between OCamlPro and INRIA) located in Paris and Nice. We gather a wide range of technical skills and industrial world expertise as we are all coming from major academic and industrial actors such as <a href="http://www.inria.fr/">INRIA</a>, [text](Dassaut Syst&egrave;mes), <a href="http://www.mlstate.com/">MLstate</a> and <a href="http://www.citrix.com/">Citrix</a>. We also love the OCaml open-source ecosystem: we have been participating to the development of <a href="http://ocsigen.org/">ocsigen</a>, <a href="http://www.openmirage.org/">mirage</a>, <a href="http://www.xen.org/products/cloudxen.html">XCP</a>, <a href="http://mldonkey.sourceforge.net/">mldonkey</a>, <a href="http://www.marionnet.org/EN/">marionet</a> and so on. By the way, OCamlPro has some open <a href="https://ocamlpro.com/jobs">positions</a> and we are still looking to hire excellent software engineers!</p>
<h2>OCaml Distribution</h2>
<p>The first of our technical activities is related to work on the OCaml distribution itself. We are part of the OCaml compiler development team - our INRIA members are part of the <a href="http://gallium.inria.fr/">Gallium</a> project which develops OCaml at INRIA - and we regularly contribute patches to improve the usability and performance of the compiler itself.</p>
<p>We have recently proposed <a href="http://caml.inria.fr/mantis/view.php?id=5894">a series of patches</a> to improve the performance of functions with float arguments and we have started developing a <a href="https://github.com/chambart/ocp-bench">framework</a> to benchmark the efficiency of compiler optimizations.</p>
<p>We are also actively exploring the design-space for concurrency and distribution in OCaml, with an implementation of</p>
<ul>
<li>reentrant runtime
</li>
<li>way to instantiate different runtimes in separate system threads in the same process
</li>
<li>efficient multi-scale communication library, between threads and between processes.
</li>
</ul>
<p>We call this <strong>multi-runtime OCaml</strong> and a prototype is available on <a href="https://github.com/lucasaiu/ocaml/tree/master">github</a>.</p>
<p>Last, we are also making progress with the memory profiling tools. We work on a modified OCaml runtime which can store the location of each allocated block in the heap, with hooks to dump that heap on demand. External tools can then use that dump to produce useful statistics about memory usage of the program. The good news is that we now have a working and usable bytecode runtime and an external tool that produces basic memory information. We are preparing an alpha release in the next month, so stay tuned!</p>
<h2>Development Tools</h2>
<p>Our efforts to make OCaml more usable go further than looking at the compiler. We are improving the development tools already existing in the community, such as the recently released <a href="https://github.com/OCamlPro/ocp-indent">indentation tool</a> which was initially coming from an experiment from <a href="https://bitbucket.org/camlspotter/ocaml-indent">Jun Furuse</a>, and creating new ones when the lack is blatant.</p>
<p>Most recent news on that front concern <a href="http://opam.ocamlpro.com/">OPAM</a>, the package manager for OCaml that we are developing since mid-2012. For people not familiar with it yet, OPAM is a source-based package manager for OCaml. It supports resolution of complex dependency constraints between packages, multiple simultaneous compiler installations, flexible package constraints, and a Git-friendly development workflow. The beta release was announced in January, and we expect the first official release to happen in the next weeks. The OCaml community has gratefully welcomed OPAM, and the <a href="https://github.com/OCamlPro/opam-repository">repository of its package metadata</a> has already become the most forked OCaml project on github! Interestingly, two meetups have gathered more than fifty OPAM users in <a href="http://meetup.ocaml-lang.fr/">Paris</a> and Cambridge in January. We really hope this kind of meetup can be generalized: if you want to help us organize one in your area, feel free to contact us!</p>
<p>The other major part of our work around development tools for OCaml is TypeRex. TypeRex is a collection of tools which focus on improving developer efficiency, and lowering the entry barrier for experienced developers who are used to shiny IDEs in other languages. The first version of <a href="http://www.typerex.org/">TypeRex</a>, that was released last year, was a first step in this direction: it provided an enhanced emacs mode for OCaml code, with colorization, indentation, refactoring facilities, completion, code-navigation, documentation tooltips, etc. The next version of TypeRex (simply dubbed <strong>typerex2</strong>) is underway, with more independent tools (like ocp-indent), less tightly coupled to Emacs, and focused on better integration with various IDEs. If you are interested in following the progress of these tools, you can check the <strong>typerex2</strong> OPAM packages with 1.99.X+beta version numbers, which we release on a regular basis.</p>
<h2>R&amp;D projects</h2>
<p>The idea that OCaml is the right choice to create new innovative products is at the core of OCamlPro. We are very involved in the research community, especially on Functional Languages, with participation into the Program Committees of various conferences such as <a href="http://oud.ocaml.org/">the OCaml User and Developer (OUD)</a> workshop and <a href="http://cufp.org/">the Commercial User of Functional Programming (CUFP)</a> conference. We also joined two collaborative R&amp;D projects in 2012, the <a href="http://www.richelieu.pro/">Richelieu FUI</a> and <a href="http://bware.lri.fr/index.php/BWare_project">BWare ANR</a>. As part of the Richelieu project, we are developing a JIT compiler for the <a href="http://www.scilab.org/">Scilab language</a>. As part of the Bware project, we improve the efficiency of automatic theorem provers, with a specific focus on <a href="http://alt-ergo.lri.fr/">Alt-Ergo</a>, an SMT solver particularly suited to program verification. We are always interested in bringing our expertise in compiler technologies and knowledge of complex and distributed systems to new R&amp;D projects: contact us if you are interested!</p>
<p>In the Richelieu project, our combined technical and theoretical expertise proved particularly effective. The research consortium is led by <a href="http://www.scilab-enterprises.com/">Scilab Entreprises</a> which needed a safer and more efficient execution engine for Scilab in order to compete with Matlab. We joined the consortium to implement the early analysis required by the JIT compiler. The project started last December, and we have since specified the semantics of the language and implemented a working prototype of an interpreter that is already as fast as the current C++ engine of Scilab 6.</p>
<h2>Growing the Community</h2>
<p>Our last important domain of activity is geared towards the OCaml community. It is important to us that the community grows bigger, and to achieve this goal there are some basic blocks that we need to help build, together with the other main actors of the community.</p>
<p>The first missing block is a good reference documentation. This year will end with (at least) one new important book for the language: <a href="http://www.realworldocaml.org/">Real-World OCaml</a> which targets experienced software engineers who do not know OCaml yet. We collaborate with <a href="http://www.cl.cam.ac.uk/projects/ocamllabs/">OCamlLabs</a> to make the technical experience of this book a success. We also work to improve the general experience of using OCaml for complete beginners by creating a stable <a href="https://github.com/OCamlPro/ocp-edit-simple">replacement</a> to the broken <strong>ocamlwin</strong>, the simple editor distributed with OCaml on Windows.</p>
<p>It is also important to us that OCaml uses the web as a platform to attract new users, as is becoming the norm for modern programming languages. We are members of the <a href="http://www.ocaml.org/">ocaml.org</a> building effort and have created <a href="http://try.ocamlpro.com/">tryocaml</a> to let newcomers easily discover the language directly from their browser. TryOcaml has been welcomed as a great tool, already adopted and adapted: see for instance <a href="http://rtt.forge.ocamlcore.org/tryrtt.html">tryrtt</a> or <a href="http://rml.lri.fr/tryrml/">try ReactiveML</a>. We are in the process of simplifying the integration with other compiler variants.
Last, but not least, we collaborate very closely with OCamlLabs to create the OCaml Plateform: a consistent set of libraries, thoroughly tested and integrated, with a rolling release schedule of 6 months. The platform will be based on <a href="http://opam.ocamlpro.com/">OPAM</a> and we are currently designing and prototyping a testing infrastructure to improve and guarantee the quality of packages.</p>
