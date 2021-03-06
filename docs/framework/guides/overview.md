---
category: framework-guides
order: 10
---

# Overview

CKEditor 5 is a project which allows you to quickly and easily initialize one of the many types of editors it offers in your application. At the same time, it is a framework for creating custom tailored rich-text editing solutions. The former requirement is met thanks to {@link builds/guides/overview CKEditor 5 Builds}. The latter, thanks to CKEditor 5 Framework.

In this guide we will try to briefly explain how the framework is built and how to start using it.

## When to use the framework?

{@link builds/guides/development/custom-builds CKEditor 5 Builds can be customized} but certain types of customizations require using the framework.

* **Writing your own features.** Features are implemented using the framework.
* **Customizing existing features.** Changing behavior of look of existing features can be done using the framework capabilities.
* **Creating new types of editors.** Using the framework you can create new types of editors.

So, the answer is simple – you need to start using the framework as soon as existing builds do not meet your requirements or can't be customized to the extent you want.

## Design

The framework was designed to be a highly flexible and unopinionated platform for creating custom rich-text editing solutions. At the same time it meets several goals making implementing features as easy task as possible.

* **Plugin-based architecture.** Everything is a plugin – even such crucial features as support for typing or `<p>` elements. You can remove them or replace with your own implementations to achieve fully customized results.
* **Unopinionated core.** The core does minimal assumptions and can be controlled through the schema. This leaves maximum decisiveness to plugins and hence to you.
* **Collaboration ready editing engine.** The editing engine implements [Operational Transformation](https://en.wikipedia.org/wiki/Operational_transformation) algorithms which, accompanied with additional mechanisms, allows implementing real-time collaboration.
* **Custom data model.** The editing engine implements a custom data model, designed to best fit multiple requirements such as enabling real-time collaboration and complex editing features.
* **Virtual DOM.** The editing engine features a custom, editing oriented virtual DOM implementation, targeting hiding browser quirks from your sight.
* **Granular, reusable features.** Features are implemented in a granular way which allows reusing and recomposing them which, in turn, makes it possible to customize and extend the editor. For instance, the {@link features/image image feature} consists of over 10 plugins at the moment.
* **Extensibility.** The entire editor architecture was designed for maximum flexibility. The code is event-based and highly decoupled allowing you to plug in or replace pieces that you want to change. Features know minimum about themselves and communicate in standardized ways.
* **Quality.** All the official packages have extensive tests suites (100% code coverage is merely a stop to that). All the code have {@link api/index API docs}.
* **Minimal configuration.** To avoid bloat, features have minimal configuration. Deeper changes in their behavior can be done by recomposing them with custom features.

## Framework structure

The framework is made of several [npm packages](https://npmjs.com). Every package is developed in its own repository, making CKEditor 5 a multi-repository project. The main repository, which glues all of them and contains CKEditor 5's development environment is https://github.com/ckeditor/ckeditor5.

The full list of official packages which make the framework is available in the [main repository's README](https://github.com/ckeditor/ckeditor5#packages).

There are a couple of groups of packages:

* [Core libraries](https://github.com/ckeditor/ckeditor5#core-libraries) – a set of packages which are the root of the framework.
* [Editors](https://github.com/ckeditor/ckeditor5#editors) – packages which implement various types of editors.
* [Features](https://github.com/ckeditor/ckeditor5#features) – packages which implement end features.
* [Themes](https://github.com/ckeditor/ckeditor5#themes) – packages which implement editor themes.
* [Builds](https://github.com/ckeditor/ckeditor5#builds) – packages containing the {@link builds/guides/overview CKEditor 5 Builds}.

## What's next?

To start using the framework see the:

* {@link framework/guides/quick-start Quick start} guide.
* {@link framework/guides/architecture/intro Introduction to the framework's architecture} guide.
* {@linkTODO framework/guides/creating-plugin Creating a plugin} guide.
