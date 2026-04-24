---
title: Cycle5ense
---

## Table of contents

* [Overview](#overview)
* [Deployment](#deployment)
* [User Guide](#user-guide)
* [Community Feedback](#community-feedback)
* [Developer Guide](#developer-guide)
* [Development History](#development-history)
* [Team](#team)

## Overview

Recycling has an emphasis in Hawai’i with the common saying “malama i ka ‘aina,” meaning to care for and protect the land. UH Manoa is a large campus, and albeit convenient to toss bottles/cans into trash bins, this does not effectively help with protecting the environment. The Cycle5ense application allows for users on campus to easily locate recyclable locations through a map and provides additional information about recycling on other pages.

* [GitHub Organization](https://github.com/cycle5ense) of Cycle5ense conatining all its repositories

[![Current Project Status](https://github.com/cycle5ense/cycle5ense/actions/workflows/ci.yml/badge.svg)](https://github.com/cycle5ense/cycle5ense/actions/workflows/ci.yml)


## User Guide

This section provides a walkthrough of the Cycle5ense user interface.

### Landing Page

The landing page is presented to users when they visit the top-level URL to the site.

![](images/landing-page.png)

### Bottles4College Announcements

The Bottles4College Announcments page provides information about events and announcments from an organization called Bottles4College.

![](images/announcements-page.png)

### Map

The Map page uses an interactable map that showcases the manoa campus with pins that indicate where recycle bins are located.

![](images/map-page.png)

### Sorting Guide

The Sorting Guide page displays information about what can and cannot be recycled based on actual regulations.

![](images/sorting-guide-page.png)

### Recycling Impact Statistics

The Recycling Impact Statistics page shows real data about how many items are recycled per year, how much resources recycling has saved, etc.

![](images/statistics-page.png)

### Add Pin

The Add Pin page allows the user to fill out a form to add a recycling bin location.

![](images/add-pin-page.png)

### Edit Pins

The Edit Pins page allows the user to edit or remove exisitng pins' information.

![](images/edit-pins-page.png)

## Community Feedback

We are interested in your experience using the Cycle5ense application!  If you would like, please take a couple of minutes to fill out the [Cycle5ense Feedback Form]().

Feedback we have received:
* Foo: "This is the very best website I have ever seen! 10/10 would recommend to anyone in UH!"

## Developer Guide

This section provides information of interest to developers wishing to use this code base as a basis for their own development tasks.

### Installation

First, visit the [Cycle5ense github page](https://github.com/cycle5ense/cycle5ense), and click the "Use this template" button to create your own repository initialized with a copy of this application. Alternatively, you can download the sources as a zip file or make a fork of the repo. However you do it, download a copy of the repo to your local computer.

Second, install dependencies with:

```
$ npm install
```

Third, setup the database. This appliaction uses prisma so create a .env file with the following information:
```
DATABASE_URL="postgresql://johndoe:randompassword@localhost:5432/mydb?schema=public"
AUTH_SECRET=Xmtn263YTsiFyQufW7V5YmfYGa3pZMsc
AUTH_URL=http://localhost:3000 # Base URL of your app
```
The DATABASE_URL should contain information to your own PostgreSQL database.

Fourth, run the following commands one at a time:

```
$ npx prisma generate
$ npx prisma migrate dev
$ npm run seed
```

Once the database is setup, run:
```
$ npm run dev
```

If all goes well, the application will appear at [http://localhost:3000](http://localhost:3000).

### Application Design

Cycle5ense is based upon [nextjs-application-template](https://github.com/ics-software-engineering/nextjs-application-template). Please use the documentation at those sites to better acquaint yourself with the basic application design in Cycle5ense.

## Development History

Access our deployed appliaction [here](https://cycle5ense.vercel.app/).

The development process for Cycle5ense conformed to [Issue Driven Project Management](http://courses.ics.hawaii.edu/ics314f19/modules/project-management/) practices. In a nutshell:

* Development consists of a sequence of Milestones.
* Each Milestone is specified as a set of tasks.
* Each task is described using a GitHub Issue, and is assigned to a single developer to complete.
* Tasks should typically consist of work that can be completed in 2-4 days.
* The work for each task is accomplished with a git branch named "issue-XX", where XX is replaced by the issue number.
* When a task is complete, its corresponding issue is closed and its corresponding git branch is merged into master.
* The state (todo, in progress, complete) of each task for a milestone is managed using a GitHub Project Board.

The following sections document the development history of Cycle5ense.

### Milestone 1: Mockup development

The goal of Milestone 1 was to create a set of HTML pages providing a mockup of the pages in the system.

Milestone 1 was managed using [Cycle5ense GitHub Project Board M1](https://github.com/orgs/cycle5ense/projects/1):

### Milestone 2: Database and Pin System

The goal of Milestone 2 is to setup a database so that all pins are stored and loaded in the map. The pin form should provide the database with the information to be stored.

Milestone 2 was managed using [Cycle5ense GitHub Project Board M2](https://github.com/orgs/cycle5ense/projects/3)

## Team

Our [Team Contract](https://docs.google.com/document/d/1DC_14kH7sXwnWtqByaQi7bHruMDQrfc-3NLZaMm2dn0/edit?tab=t.0#heading=h.zi0hnn54eohk)

* [Au, Joshua](https://joshau124.github.io/)
* [Herradura, Riley](https://rileyherra.github.io/)
* [Lagazo, Julius](https://jslagazo.github.io/)
* [Knight, Danil](https://danilk09.github.io/)
* [Unger, Tyler](https://ungert.github.io/)