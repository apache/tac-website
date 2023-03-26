<!--                                                                                                                                                                                                    
Licensed to the Apache Software Foundation (ASF) under one or more
contributor license agreements.  See the NOTICE file distributed with
this work for additional information regarding copyright ownership.
The ASF licenses this file to You under the Apache License, Version 2.0
(the "License"); you may not use this file except in compliance with
the License.  You may obtain a copy of the License at
   
    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->
# Apache Travel Assistance Committee website

This is the source code for the website of the [Apache Travel Assistance Committee website](https://tac.apache.org/)

## How to publish the website

Changes to the `main` branch of this repository trigger the
[tac-website Jenkins Job](https://ci-builds.apache.org/job/TAC/job/tac-website/job/main/)
which generates the website content and commits it to the `asf-site` branch of this repository.

The [ASF's gitpubsub mechanism](https://blogs.apache.org/infra/entry/git_based_websites_available)
then synchronizes that content to [https://tac.apache.org/](https://tac.apache.org/), usually within a few seconds. 
More details about the publication process can be found in the
[ASF Documentation about Project sites](https://infra.apache.org/project-site.html). 
If for some reason this process fails, you can use [the self-service page from ASF Infra](https://selfserve.apache.org/)
to trigger a resync of the git repo.

## Powered by Hugo!

The website uses Hugo as static website generator, see [their website](https://gohugo.io/) for more information
and for how to install and run it if needed.

Other Apache websites that are built with Hugo should be listed by
[this GitHub query for the 'hugo' tag](https://github.com/search?q=topic%3Ahugo+org%3Aapache&type=Repositories).

## How to test the website and changes on your own computer

To generate the static website, execute `hugo` to generate the website under `target/content`

During development, it may be useful to run an incremental build.
For this to work, execute `hugo server -D` to 
continuously (re)generate and serve the website on `localhost:1313`. (-D means include draft pages)

