---
layout: post
category : software
tags : [java, announce, benchmark]
tagline: Java sparse matrix package
---
{% include JB/setup %}

It is with great pleasure that I am able announce the release of CSparseJ
*version 1.1*. The main feature of this release is **complex number support**.
Solving sparse sets of complex linear equations is a common practice in
electric power system analysis, as well as in many other areas of scientific
computing.

### Overview

CSparseJ is a Java port of [CSparse](http://www.cise.ufl.edu/research/sparse/CSparse/)
(a Concise Sparse matrix package). CSparse is a sparse matrix package written
in C by [Tim Davis](http://www.cise.ufl.edu/~davis). CSparseJ version 1.0 was
released by [Piotr Wendykier](http://sites.google.com/site/piotrwendykier/software/csparsej)
on June 13, 2009. It featured single and double precision real number support.

This release adds double precision complex number support for all of the same
functions. Complex numbers are represented using arrays of primitive doubles,
where the real and imaginary components are stored alternately, for optimal
performance.

### Benchmarks

CSparseJ 1.1 was benchmarked against [CXSparse](http://www.cise.ufl.edu/research/sparse/CXSparse/)
2.2.6 using the testbed:

* IBM Thinkpad T61p,
* Intel Core 2 Duo CPU T9300 (2.5GHz),
* 8 Gb RAM,
* Ubuntu 12.04 (Precise Pangolin) 64-bit,
* Linux Kernel 3.2.0-24-generic,
* OpenJDK 64-Bit Server VM (1.6.0_24),
* GCC version 4.6.3,
* Java flags: `-d64 -server -Xms2g -Xmx2g -XX:+UseParallelGC`
* C compiler flags: `-O2`

### Maven

With this release CSparseJ is available from Maven's [central repository](http://search.maven.org/).
CSparseJ can be used in your project by adding this to your Maven POM:

    <dependency>
      <groupId>net.sourceforge.csparsej</groupId>
      <artifactId>csparsej</artifactId>
      <version>1.1.1</version>
    </dependency>

The artifacts are synced with Maven Central using [Sonatype OSS](http://oss.sonatype.org/).
New releases can be staged using the commands:

    $ mvn release:prepare
    $ mvn release:perform

### License

Copyright &copy; 2006-2011, Timothy A. Davis  
Copyright &copy; 2009, Piotr Wendykier  
Copyright &copy; 2011-2012, Richard W. Lincoln

CSparseJ is available under the terms of the GNU [Lesser General Public License](http://www.gnu.org/licenses/lgpl-2.1.txt)
(LGPL) version 2.1, or (at your option) any later version.

CSparseJ is distributed in the hope that it will be useful, but *WITHOUT ANY WARRANTY*;
without even the implied warranty of *MERCHANTABILITY* or *FITNESS FOR A PARTICULAR PURPOSE*.
See the GNU [Lesser General Public License](http://www.gnu.org/licenses/lgpl-2.1.txt)
for more details.

### Download

The source code for CSparseJ is available from my [GitHub](http://www.github.com/rwl/CSparseJ)
page. Alternatively, CSparseJ may be downloaded as a Java archive:

* [csparsej-1.1.1.jar](https://oss.sonatype.org/service/local/repositories/releases/content/net/sourceforge/csparsej/csparsej/1.1.1/csparsej-1.1.1.jar)
* [csparsej-1.1.0-sources.jar](https://oss.sonatype.org/service/local/repositories/releases/content/net/sourceforge/csparsej/csparsej/1.1.1/csparsej-1.1.1-sources.jar)
* [csparsej-1.1.0-javadoc.jar](https://oss.sonatype.org/service/local/repositories/releases/content/net/sourceforge/csparsej/csparsej/1.1.1/csparsej-1.1.1-javadoc.jar)

