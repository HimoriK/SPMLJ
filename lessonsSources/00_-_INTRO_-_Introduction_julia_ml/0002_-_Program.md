# [Program](@id course_program)



## Course content:

- **Introduction unit**: (a) motivations, highlights of the main Julia  characteristics; (b) guidance in setting up a Julia development environment and a crash course on git, (c) modules, packages, environments and the wider topic of reproducible results; (d) introduction to the topic of Machine Learning (scope, examples, clarification of the terminology)

- **1ˢᵗ thematic unit `JULIA1`**: (a) a gentle but rather deep introduction to the Julia programming language (syntax, provided data structures, custom types, control flows and functions); (b) advanced topics (meta-programming, code optimisation, interface with C/Python/R code, hints to parallel computation);

- **2ⁿᵈ thematic unit `JULIA2`**: (a) data wrangling with the DataFrame package for in-memory tabular data, including the split-apply-combine strategy; (b) the Distributions package for making probabilistic models, (c) the LsqFit package for fitting any generic curve with data, (d) the Plots package for visualisation, (e) the JuMP algebraic modelling language for implementing and solving  complex constrained optimisation models (à la GAMS);

- **3ʳᵈ thematic unit `ML1`**:  (a) intuitions of machine learning concepts (supervised learning, cross-validation and regularisation); (b) implementation of the perceptron linear classifier;

- **4ᵗʰ thematic unit `NN`**:  (a) neural network models: how they work, what they are good for and how to train them; (b) specific neural network architectures: convolutional neural networks and recurrent neural networks; (c) implementation of neural network workflos using Julia packages.

## Course organisation:

- 9 runnable Julia files in public GitHub repository and 7 MarkDown files with embedded Julia code;
- 15 hours of videos, 15 interactive quizzes with 52 questions and 7 guided exercises;
- Discussion forum embedded at the bottom of each page


## List of available videos:


The following videos (14h:52':22'') are available. All except the introduction follow very close the pages in this site.

Videos are hosted on YouTube.

!!! tip
    Note that the links below will bring you directly to YouTube. [Click here to start the course on this site](@ref introduction_julia) (with the YouTube videos embedded in the page) or use the menu to jump to the desired content.

### 00 KOM: Kick-off meeting (2h:34:46)

Note that this introduction has been partially recorded before the rest of the course has been implemented, so that the organisation of the course, and the way it is delivered, are not exactly as described in the videos below.

Take-home tip: in your projects, implement the introduction and the conclusions as the last elements ;-)

The slides used in the videos below are available [here](https://github.com/sylvaticus/SPMLJ/blob/main/lessonsSources/00_-_INTRO_-_Introduction_julia_ml/assets/00_KOMEETING.pdf).

- [Course introduction](https://www.youtube.com/watch?v=82IbUHUgzLo&list=PLDIpPSqVuMmLGUNGMXL2eO2pqKlzdPfxa&index=1) (6:03)
- [Julia overview](https://www.youtube.com/watch?v=uW8iyTjSaJk&list=PLDIpPSqVuMmLGUNGMXL2eO2pqKlzdPfxa&index=2) (36:25)
- Hands on (42:09)
  - [Part A: Creating a git repository on GitHub, installing Julia and the VSCode Julia plugin](https://www.youtube.com/watch?v=kT9Vm8Ov6qo&list=PLDIpPSqVuMmLGUNGMXL2eO2pqKlzdPfxa&index=3) (20:15)
  - [Part B: Working with a git repository](https://www.youtube.com/watch?v=51AwIJzxtgw&list=PLDIpPSqVuMmLGUNGMXL2eO2pqKlzdPfxa&index=4) (21:54)
- [Pkgs, modules and environments](https://www.youtube.com/watch?v=_qTLSrk1ICA&list=PLDIpPSqVuMmLGUNGMXL2eO2pqKlzdPfxa&index=5) (20:56)
- [ML Terminology](https://www.youtube.com/watch?v=l9ls2yssKiE&list=PLDIpPSqVuMmLGUNGMXL2eO2pqKlzdPfxa&index=6) (21:19)
- [A first ML Example](https://www.youtube.com/watch?v=SclPPNvYEAI&list=PLDIpPSqVuMmLGUNGMXL2eO2pqKlzdPfxa&index=7) (7:00)
- [ML application areas](https://www.youtube.com/watch?v=bIApDXIhm1k&list=PLDIpPSqVuMmLGUNGMXL2eO2pqKlzdPfxa&index=8) (14:24)
- [Further ML Examples](https://www.youtube.com/watch?v=9Kni5XkQV5M&list=PLDIpPSqVuMmLGUNGMXL2eO2pqKlzdPfxa&index=9) (6:34)


### 01 JULIA1: Basic Julia programming (5h:52:33)
- Basic syntax elements (46:45)
  - [Part A - Introduction and setup of the environment](https://www.youtube.com/watch?v=fRv3vAmzHS8&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=1) (8:37)
  - [Part B - Comments, code organisation, Unicode support, broadcasting](https://www.youtube.com/watch?v=1SVA6woAq18&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=2) (12:04)
  - [Part C - Math operators, quotation marks](https://www.youtube.com/watch?v=1AVb-92QmPg&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=3) (6:49)
  - [Part D - Missing values](https://www.youtube.com/watch?v=UGlJlH1BbjM&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=4) (10:04)
  - [Part E - Stochasticity in programming](https://www.youtube.com/watch?v=Hi_a7YWA_j8&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=5) (9:14)
- Types and objects (26:38)
  - [Part A - Types, objects, variables and operators](https://www.youtube.com/watch?v=tOqojCvpAuE&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=6) (13:05)
  - [Part B - Object mutability and effects on copying objects](https://www.youtube.com/watch?v=yeaTNPKqRTo&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=7) (13:34)      
- Predefined types (1h:39:50)
  - [Part A - Primitive types, char and strings](https://www.youtube.com/watch?v=kEb50RK1sK0&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=8) (9:37)
  - [Part B - One dimensional arrays](https://www.youtube.com/watch?v=4nR1rI8_hug&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=9) (30:42)
  - [Part C - Multidimensional arrays](https://www.youtube.com/watch?v=WJcikzhIr7Y&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=10) (23:37)
  - [Part D - Tuples and named tuples](https://www.youtube.com/watch?v=79kRlC5dbAo&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=11) (7:50)
  - [Part E - Dictionaries and sets](https://www.youtube.com/watch?v=KwY_dfvzByk&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=12) (8:57)
  - [Part F - Date and times](https://www.youtube.com/watch?v=y4Ty2Wx_lC4&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=13) (19:11)
- Control flow and functions (44:47)
  - [Part A - Variables scope](https://www.youtube.com/watch?v=S8HcWitIRZg&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=14) (9:47)
  - [Part B - Loops and conditional statements](https://www.youtube.com/watch?v=DGh_5aNKghI&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=15) (9:2)   
  - [Part C - Functions](https://www.youtube.com/watch?v=oejR6LKvFXY&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=16) (25:57)
- Custom Types (40:02)
  - [Part A - Types of types, composite types](https://www.youtube.com/watch?v=-tuVyAixoXE&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=17) (17:56)
  - [Part B - Parametric types](https://www.youtube.com/watch?v=UCybSmhURIE&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=18) (7:37)
  - [Part C - Inheritance and composition paradigms](https://www.youtube.com/watch?v=gv8ZIThsHTo&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=19) (14:28)  
- Further Topics (1:34:30)
  - [Part A - Metaprogramming and macros](https://www.youtube.com/watch?v=Q3Fx6pFLCFk&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=20) (23:46)
  - [Part B - Interoperability with other languages](https://www.youtube.com/watch?v=xK_Ug2gtQvU&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=21) (23:6)
  - [Part C - Performances and errors: profiling, debugging, introspection and exceptions](https://www.youtube.com/watch?v=vg8v_6oX2DM&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=22)(27:33)
  - [Part D - Parallel computation: multithreading, multiprocessing](https://www.youtube.com/watch?v=L849oXXCXFM&list=PLDIpPSqVuMmK1poGUS7nuAXXILxHxmV2O&index=23) (20:3)


### 02 JULIA2: Scientific Julia programming (2h:39:34)
- Data Wrangling (1h:31:15)
  - [Part A - Introduction and data import](https://www.youtube.com/watch?v=o3TiuZlxMKI&list=PLDIpPSqVuMmI4Dhiekw2y1wakzsaMSJVG&index=1) (18:28)
  - [Part B - Getting insights of the data](https://www.youtube.com/watch?v=_iQh9dddIUY&list=PLDIpPSqVuMmI4Dhiekw2y1wakzsaMSJVG&index=2) (25:26)
  - [Part C - Edit data and dataframe structure](https://www.youtube.com/watch?v=qhhT-Ckyvag&list=PLDIpPSqVuMmI4Dhiekw2y1wakzsaMSJVG&index=3) (23:40)
  - [Part D - Pivot, Split-Apply-Combine and data export](https://www.youtube.com/watch?v=w1KcD8sJLok&list=PLDIpPSqVuMmI4Dhiekw2y1wakzsaMSJVG&index=4) (23:39)
- Further topics (1h:08:19)
  - [Part A - Plotting](https://www.youtube.com/watch?v=b-WkKMLd-Ws&list=PLDIpPSqVuMmI4Dhiekw2y1wakzsaMSJVG&index=5) (15:18)
  - [Part B - Probability distributions and data fitting](https://www.youtube.com/watch?v=cfNXk2eiIFE&list=PLDIpPSqVuMmI4Dhiekw2y1wakzsaMSJVG&index=6) (11:55)
  - [Part C - Constrained optimisation, the transport problem](https://www.youtube.com/watch?v=vxo7nOpnFSs&list=PLDIpPSqVuMmI4Dhiekw2y1wakzsaMSJVG&index=7) (24:59)
  - [Part D - Nonlinear constrained optimisation, the optimal portfolio allocation](https://www.youtube.com/watch?v=_ypOlSwCC7U&list=PLDIpPSqVuMmI4Dhiekw2y1wakzsaMSJVG&index=8) (16:04)

### 03 ML1: Introduction to Machine Learning (1h:29:43)
- Main concepts in Machine Learning(44:45)
  - [Part A - Introduction, perceptron overall idea](https://www.youtube.com/watch?v=JuqCxqLik0s&list=PLDIpPSqVuMmL9JsL_hDdciDvreAOtQg3v&index=1) (11:23)
  - [Part B - Hyperparameters and cross-validation](https://www.youtube.com/watch?v=agi2dKxClec&list=PLDIpPSqVuMmL9JsL_hDdciDvreAOtQg3v&index=2) (15:18)
  - [Part C - The perceptron algorithm](https://www.youtube.com/watch?v=2otq8KEMp8Y&list=PLDIpPSqVuMmL9JsL_hDdciDvreAOtQg3v&index=3) (9:53)
  - [Part D - SVM and non-linear classification with linear classifiers](https://www.youtube.com/watch?v=KsOubVwDcjY&list=PLDIpPSqVuMmL9JsL_hDdciDvreAOtQg3v&index=4) (8:9)
- The Perceptron algorithm for linear classification (44:58)
  - [Part A - A first version](https://www.youtube.com/watch?v=kOGSvdgd_3Y&list=PLDIpPSqVuMmL9JsL_hDdciDvreAOtQg3v&index=5) (13:22)
  - [Part B - A better version](https://www.youtube.com/watch?v=g0yz7La53Vc&list=PLDIpPSqVuMmL9JsL_hDdciDvreAOtQg3v&index=6) (10:28)
  - [Part C - Cross-validation implementation](https://www.youtube.com/watch?v=ieIZFF6RYQo&list=PLDIpPSqVuMmL9JsL_hDdciDvreAOtQg3v&index=7) (21:7)

### 03 NN: Neural Networks (2h:15:36)
- Introduction to Neural Networks (1h:25:17)
  - [Part A - Introduction and motivations](https://www.youtube.com/watch?v=4m_BzDV15XQ&list=PLDIpPSqVuMmIvTA3w7ATUKHzq82uey8pP&index=1) (5:32)
  - [Part B - Feed-forward neural networks](https://www.youtube.com/watch?v=MMrM5X4gxqY&list=PLDIpPSqVuMmIvTA3w7ATUKHzq82uey8pP&index=2) (18:57)
  - [Part C - How to train a neural network](https://www.youtube.com/watch?v=FNVfRwqT120&list=PLDIpPSqVuMmIvTA3w7ATUKHzq82uey8pP&index=3) (18:4)
  - [Part D - Convolutional neural networks](https://www.youtube.com/watch?v=hFaOeSLEqpI&list=PLDIpPSqVuMmIvTA3w7ATUKHzq82uey8pP&index=4) (13:21)
  - [Part E - Multiple layers in convolutional neural networks](https://www.youtube.com/watch?v=zWQ8-voVW78&list=PLDIpPSqVuMmIvTA3w7ATUKHzq82uey8pP&index=5) (10:33)
  - [Part F - Recurrent neural networks](https://www.youtube.com/watch?v=oeyfFrgcW5c&list=PLDIpPSqVuMmIvTA3w7ATUKHzq82uey8pP&index=6) (17:49)
- Neural Network workflows in Julia (50:18)
  - [Part A - Binary classification](https://www.youtube.com/watch?v=IFVz0jsy5AQ&list=PLDIpPSqVuMmIvTA3w7ATUKHzq82uey8pP&index=7) (15:54)
  - [Part B - Multinomial classification](https://www.youtube.com/watch?v=fqROq7B6nyY&list=PLDIpPSqVuMmIvTA3w7ATUKHzq82uey8pP&index=8) (15:1)
  - [Part C - Regression](https://www.youtube.com/watch?v=jO-mfgzo7VY&list=PLDIpPSqVuMmIvTA3w7ATUKHzq82uey8pP&index=9) (6:3)
  - [Part D - Convolutional neural network](https://www.youtube.com/watch?v=mSUdLu9HAd4&list=PLDIpPSqVuMmIvTA3w7ATUKHzq82uey8pP&index=10) (13:19)

---------
```@raw html
<div id="pd_rating_holder_8962705"></div>
<script type="text/javascript">
const pageURL = window.location.href;
PDRTJS_settings_8962705 = {
"id" : "8962705",
"unique_id" : "/home/lobianco/CloudFiles/lef-nancy-sync/Documents/Teaching/2021-2022/Introduction to Scientific Programming and Machine Learning with Julia/SPMLJ/lessonsSources/00_-_INTRO_-_Introduction_julia_ml/0002_-_Program.md",
"title" : "0002_-_Program.md",
"permalink" : pageURL
};
</script>
```
```@raw html
<div class="addthis_inline_share_toolbox"></div>
```

---------
```@raw html
<script src="https://utteranc.es/client.js"
        repo="sylvaticus/SPMLJ"
        issue-term="title"
        label="💬 website_comment"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>
```
```@raw html
<script type="text/javascript" charset="utf-8" src="https://polldaddy.com/js/rating/rating.js"></script>
```
```@raw html
<!-- Go to www.addthis.com/dashboard to customize your tools -->
<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-6256c971c4f745bc"></script>
```

---------
```@raw html
<div id="pd_rating_holder_8962705"></div>
<script type="text/javascript">
const pageURL = window.location.href;
PDRTJS_settings_8962705 = {
"id" : "8962705",
"unique_id" : "/home/lobianco/CloudFiles/lef-nancy-sync/Documents/Teaching/2021-2022/Introduction to Scientific Programming and Machine Learning with Julia/SPMLJ/lessonsSources/00_-_INTRO_-_Introduction_julia_ml/0002_-_Program.md",
"title" : "0002_-_Program.md",
"permalink" : pageURL
};
</script>
```
```@raw html
<div class="addthis_inline_share_toolbox"></div>
```

---------
```@raw html
<script src="https://utteranc.es/client.js"
        repo="sylvaticus/SPMLJ"
        issue-term="title"
        label="💬 website_comment"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>
```
```@raw html
<script type="text/javascript" charset="utf-8" src="https://polldaddy.com/js/rating/rating.js"></script>
```
```@raw html
<!-- Go to www.addthis.com/dashboard to customize your tools -->
<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-6256c971c4f745bc"></script>
```

---------
```@raw html
<div id="pd_rating_holder_8962705"></div>
<script type="text/javascript">
const pageURL = window.location.href;
PDRTJS_settings_8962705 = {
"id" : "8962705",
"unique_id" : "/home/lobianco/CloudFiles/lef-nancy-sync/Documents/Teaching/2021-2022/Introduction to Scientific Programming and Machine Learning with Julia/SPMLJ/lessonsSources/00_-_INTRO_-_Introduction_julia_ml/0002_-_Program.md",
"title" : "0002_-_Program.md",
"permalink" : pageURL
};
</script>
```
```@raw html
<div class="addthis_inline_share_toolbox"></div>
```

---------
```@raw html
<script src="https://utteranc.es/client.js"
        repo="sylvaticus/SPMLJ"
        issue-term="title"
        label="💬 website_comment"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>
```
```@raw html
<script type="text/javascript" charset="utf-8" src="https://polldaddy.com/js/rating/rating.js"></script>
```
```@raw html
<!-- Go to www.addthis.com/dashboard to customize your tools -->
<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-6256c971c4f745bc"></script>
```

---------
```@raw html
<div id="pd_rating_holder_8962705"></div>
<script type="text/javascript">
const pageURL = window.location.href;
PDRTJS_settings_8962705 = {
"id" : "8962705",
"unique_id" : "/home/lobianco/CloudFiles/lef-nancy-sync/Documents/Teaching/2021-2022/Introduction to Scientific Programming and Machine Learning with Julia/SPMLJ/lessonsSources/00_-_INTRO_-_Introduction_julia_ml/0002_-_Program.md",
"title" : "0002_-_Program.md",
"permalink" : pageURL
};
</script>
```
```@raw html
<div class="addthis_inline_share_toolbox"></div>
```

---------
```@raw html
<script src="https://utteranc.es/client.js"
        repo="sylvaticus/SPMLJ"
        issue-term="title"
        label="💬 website_comment"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>
```
```@raw html
<script type="text/javascript" charset="utf-8" src="https://polldaddy.com/js/rating/rating.js"></script>
```
```@raw html
<!-- Go to www.addthis.com/dashboard to customize your tools -->
<script type="text/javascript" src="//s7.addthis.com/js/300/addthis_widget.js#pubid=ra-6256c971c4f745bc"></script>
```
