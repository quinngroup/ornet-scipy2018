:author: Andrew Durden
:email: andrewdurden@uga.edu
:institution: Department of Computer Science, University of Georgia, Athens, GA 30602 USA

:author: Allyson T Loy
:email: allyson.loy@uga.edu
:institution: Department of Microbiology, University of Georgia, Athens, GA 30602 USA

:author: Barbara Reaves
:email: bjreaves@uga.edu
:institution: Department of Infectious Diseases, University of Georgia, Athens, GA 30602 USA

:author: Mojtaba Fazli
:email: Mojtaba@uga.edu
:institution: Department of Computer Science, University of Georgia, Athens, GA 30602 USA

:author: Abigail Courtney
:email: abigail.courtney@uga.edu
:institution: Department of Microbiology, University of Georgia, Athens, GA 30602 USA

:author: Frederick D Quinn
:email: fquinn@uga.edu
:institution: Department of Infectious Diseases, University of Georgia, Athens, GA 30602 USA

:author: S Chakra Chennubhotla
:email: chakracs@pitt.edu
:institution: Department of Computational and Systems Biology, University of Pittsburgh, Pittsburgh, PA 15232 USA

:author: Shannon P Quinn
:email: spq@uga.edu
:institution: Department of Computer Science, University of Georgia, Athens, GA 30602 USA
:institution: Department of Cellular Biology, University of Georgia, Athens, GA 30602 USA


-------------------------------------------------------------------
Dynamic Social Network Modeling of Diffuse Subcellular Morphologies
-------------------------------------------------------------------

.. class:: abstract

The use of fluorescence microscopy has led to the development of new technologies and quantitative modeling approaches as biomedical imaging data has become amenable to analysis through computer vision and machine learning methods. Extracting and modeling quantitative knowledge of biological systems has become more common, and many molecular and cellular phenotypes can now be automatically characterized. However, much of this work is still nascent; in particular, there are a number of approaches to modeling spatial patterns of solid morphologies, such as cell membranes or nuclei, but considerably fewer approaches to modeling diffuse organellar patterns such as mitochondria or actin. Furthermore, little work has focused on the development of spatiotemporal models that capture the relationships between spatial quantities--size, shape, and distribution--as functions of time. Such models are extremely useful for characterizing conditional events, such as the addition of a toxin or invasion by a pathogen.

Here, we discuss initial work into building spatiotemporal models of diffuse subcellular morphologies, specifically the mitochondrial protein patterns of alveolar cells. We leverage principles of graph theory and consider the mitochondrial patterns an instance of a social network: a collection of vertices interconnected by edges, indicating spatial relationships. By studying the changing topology of the social networks over time, we gain a statistical understanding of the types of stresses imposed on the mitochondria by external stimuli, and can relate these effects in terms of graph theoretic quantities such as centrality, connectivity, and flow. We demonstrate how the gradients of the graph Laplacian underlying the social network, and the changes in its principal components, can yield biologically-meaningful interpretations of the evolving morphology. Our primary goal is the development of a bioimaging toolbox, built from existing open source packages in the scientific Python ecosystem (SciPy, NumPy, scikit-image, OpenCV), which builds dynamic social network models from time series fluorescence images of diffuse subcellular protein patterns, enabling a direct quantitative comparison of network structure over time and between cells exposed to different conditions.

.. class:: keywords

Biomedical Imaging, Graph Theory, Social Networks

Introduction
------------

Given the rise of fluorescence microscopy, live cell footage has become much more accessible. This increase in subcellular biomedical imaging data has lead to a heavy analysis of organelles with solid structure. However, the growth in modeling and classification of solid morphologies has created a large and growing gap in our ability to autonomously quantify subcellular structures of diffuse morphology, organelles and proteins like mitochondria and actin.

Being able to not only quantify the structure of a protein, but also it’s change over time can lead to understanding the protein’s relationship with environmental variables like toxins or bacteriophages. We look to achieve this goal of quantification through the novel employ of social network analogues. There are many advantages of using a social network metric to model diffuse structures. It allows for not only the overall form of the morphology to impact the quantitative analysis, but also for the diffuseness property to influence the connectivity of the network. The heavily studied field of social network and graph theory also opens opportunity for a varied analysis of the analogue once it is modeled.

This is the point in most introductions I’ve read where they talk about previous research that the paper is built off of...
