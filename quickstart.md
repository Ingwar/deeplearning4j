---
title:
layout: default
---

#Quickstart

* First, test which version of Java you have (and whether you have it at all), by typing the following into the command line:

		java -version

* If you don't have Java 7 installed on your machine, download the [Java Development Kit (JDK) here](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html). The download will vary by operating system. For newer Macs, you'll want the file on the first line to mention Mac OS X (the number after *jdk-7u* increments with each update). It will look something like this:

		Mac OS X x64 185.94 MB -  jdk-7u67-macosx-x64.dmg

* Due to our reliance on Jblas for CPUs, native bindings for Blas are required.

		OSX
		Already Installed
		
		Fedora/RHEL
		yum -y install blas

		Ubuntu
		apt-get install libblas* (credit to @sujitpal)

		Windows
		See http://icl.cs.utk.edu/lapack-for-windows/lapack/

* Since DL4J uses cross-platform tooling to make Python calls for data visualization and debugging, you'll also want to download [Anaconda here](http://continuum.io/downloads). Once you have Anaconda installed, you can test whether you have the necessary libs by entering this in a Python window:

		import numpy
		import pylab as pl

![Alt text](../img/python_shot.png)

These tools will generate the visualizations that allow you to debug your neural nets as they train. Normalish distributions are a good sign. The visualizations occasionally generate a list of errors on Macs -- that does not stop the nets from training.

* Next, git clone the DL4J examples like so:

		git clone https://github.com/SkymindIO/dl4j-examples

You can then manually import the Maven project into [Eclipse](http://books.sonatype.com/m2eclipse-book/reference/creating-sect-importing-projects.html),  [Intellij](https://www.jetbrains.com/idea/help/importing-project-from-maven-model.html) or [Netbeans](http://wiki.netbeans.org/MavenBestPractices).

* Open up the dl4j-examples project in IntelliJ, find the MNIST example and press run. 

* This is the moment of truth. You should now see evidence in your terminal/cmd that the neural net has begun to train, as the net's iterations begin to scroll down your terminal window. (In some cases, the program may take a minute to locate resources.) Look at the second-to-rightmost number in the rows below. It should be decreasing with each new iteration. That’s the measure of the net’s error reconstructing a numeral-image. Less error means your net is learning. 

![Alt text](../img/learning.png)

* Throughout the training, you should see some numeral-images pop up in small windows in the upper lefthand corner of your screen. Those are the reconstructions that prove your net actually works, and they look similar to these. 

![Alt text](../img/numeral_reconstructions.png)

The way to judge whether your net has successfully learned the MNIST dataset is to look at the visualizations. They should gradually come to resemble handwritten numerals. Once they do, your net has been successfully trained, and that's what you need for deep learning to be worth anything.

By this point, you should have a net that produces relatively accurate reconstructions. Congratulations. (If you haven't, please [let us know](https://groups.google.com/forum/#!forum/deeplearning4j)!)

**NEXT STEP**: Here is a tutorial on [how to run any example on DL4J](../runexample.html). Go [here](https://github.com/SkymindIO/dl4j-examples/tree/master/src/main/java/org/deeplearning4j) to choose the next example to run. (You can choose examples for MNIST, Iris and Labeled Faces in the Wild.)

Once you've explored all our examples, you'll want to get the whole code base running by following the instructions on our  [Getting Started page](../gettingstarted.html).