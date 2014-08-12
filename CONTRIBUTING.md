Contributing a demo to JBoss Developer
======================================

For every demo, we need to know certain pieces of metadata. We recommend following the easiest approach:

1. Host the demo on github
2. Add a `README.md` describing how to use the demo
3. Adding some simple metadata to the README
4. Send a pull request, adding the demo to the list

Using a github repository
-------------------------

If you are using a github repository, we can pull quite a bit of the metadata from the repository. There is a template repository, including a `README.md` with extensive instructions on how to create a great `README.md`, at <https://github.com/jboss-developer/jboss-developer-demo-template>.

By default we will:

* point people at your [https://help.github.com/articles/creating-releases](latest release on github) for download and browse links
* set the published date as the date of your last release
* display the README.md as the homepage for your demo

Having created a github repository, and added a `README.md`, you need to metadata to the `README.md`. The metadata is read from `Name: Value` pairs, each located on a new line after the title. You *must* add:

* Title - read from the title of the `README.md`
* Author - e.g. `Author: Pete Muir`
* Summary - a short, one paragraph summary of the demo, used in search results

You can optionally add:

* Level - The level of difficulty, one of Beginner, Intermediate or Advanced, defaults to Beginner
* Technologies - A comma separated list of technologies the demo shows off, aids searches and related items links
* Target Product - The product the demo targets, causes the demo to show up in a particular product's developer materials

Having set up your repository, you need to send a pull request against <https://github.com/jboss-developer/jboss-developer-demos>, adding the URL to the repository to `demos.yaml`. Once your pull request has been merged, the next time the site is built, your demo will be included. We normally build the site at least once every day.

Note that if you don't have a release available, we will use the HEAD of master as the download.

Specifying the metadata manually
--------------------------------

Instead of specifying the metadata inside the `README.md` you can specify it in a standalone YAML file, and point `demos.yaml` to that YAML file. An example standalone YAML file can be found at <https://github.com/jboss-developer/jboss-developer-demos/blob/master/demo-template.yaml>. Most of the fields you can define are specified there, and the comment for the field defines whether it is required or not. 

If you need more control over the download, you can use the fields `download`, `browse` and `published` to specify the zip download URL, the URL to browse the SCM, and the publish date.

Having created this file, and published it somewhere, just send a pull request against `demos.yaml`, adding the URL of the YAML file to the list.

