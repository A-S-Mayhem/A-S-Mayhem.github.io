---
title: "Molecular Communications"
excerpt: "Spatial Receptor Allocation for a Multiple Access Hub<br/><img src='/images/mol-comm-sys.png'>"
collection: projects
---

Molecular Communications via Diffusion (MCvD) is a communications scheme, where the information is transmitted through the free-diffusion of carrier molecules. In our research, the communications system was designed as On-Off Keying (OOK). That is, if the number of carrier molecules that arrive at the receiver during the specified time interval exceeds a threshold value, then the transmitted bit will be 1. Otherwise, it will be 0.

In this communications scheme, there are two major issues: Inter-symbol Interference (ISI) and Inter-link Interference (ILI). The former occurs when the carrier molecules arrive at the receiver later than the specified time interval for decision. The latter occurs, on the other hand, when carrier molecules of a receptor arrive at other receptor regions. Both ISI and ILI might cause misleading decisions; hence, should be reduced with changes in system design.

In our research, we designed a novel MCvD system, where there are multiple receptor regions in one spherical receiver, and each region is cone-shaped. I worked on the optimal receptor allocation problem, in which we found the optimal vertex angle for each cone-shaped receptor in the spherical receiver based on the signal-to-interference-difference (SILD). The definition of SILD and other details can be found in our paper.
* My Contribution: 

I led the project from the start, where, I designed the communications systems, implemented Monte Carlo simulations in MATLAB as well as worked with the postdoctoral researcher, Dr. Bayram Cevdet Akdeniz, on the definition of the optimization problem. In the end, we solved the optimization problem and published the results as a research article in IEEE Transactions on Molecular, Biological, and Multi-Scale Communications. 

<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
<link href="css/ba-slider.css" rel="stylesheet" />
<script src="js/ba-slider.min.js"></script>

<div class="comparison-slider-wrapper">
    <div id="ba-slider" class="comparison-slider">
            <div class="overlay">text</div>
            <img src="images/PT_makeup2_test5_256_with_var.png"/>
        <div class="resize">
            <div class="overlay">text</div>
            <img src="17926.png"/>
        </div>
        <div class="divider"></div>
    </div>
</div>

<script>
    $(document).ready(function () {
        baSlider("#ba-slider");
    });
</script>
