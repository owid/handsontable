---
title: IME support
metaTitle: IME support - Guide - Handsontable Documentation
permalink: /ime-support
canonicalUrl: /ime-support
tags:
  - input method editor
  - korean
  - japanese
  - chinese
  - latin
---

# IME support

[[toc]]

## What is IME

An **Input Method Editor** (IME) is a component that is part of the Operating System (OS) that enables users to generate characters that are not natively available on their keyboard by using input sequences from keystrokes or mouse movements. An example scenario would be to add Chinese characters using a Latin Keyboard; IME support would enable you to generate the characters you need.

## IME support in Handsontable

IME support is built-in to the OS, and therefore, there's no need or ability to enable/disable it. It is **always on** and is activated when a user switches to one of the three supported languages. Upon activation, the IME will appear below the text editor (subject to the correct configuration in the OS). When using IME with Handsontable, it **always** applies to the **entire grid**.

## Testing IME support

To test the IME support, you will need to change your language preferences for your keyboard in your OS. Next, set up the input source as **Korean, Japanese, or Chinese** and then start to edit any of the cell editors within Handsontable.

## Watch IME in action

<video controls loop v-bind:src="'/docs/'+ $page.currentVersion + '/img/pages/ime-support/ime-support-in-handsontable.mp4'" width="100%"></video>

## Related API reference

- Configuration options:
  - [`language`](@/api/options.md#language)
  - [`layoutDirection`](@/api/options.md#layoutdirection)
  - [`locale`](@/api/options.md#locale)
- Core methods:
  - [`getDirectionFactor()`](@/api/core.md#getdirectionfactor)
  - [`getTranslatedPhrase()`](@/api/core.md#gettranslatedphrase)
  - [`isLtr()`](@/api/core.md#isltr)
  - [`isRtl()`](@/api/core.md#isrtl)
- Hooks:
  - [`afterLanguageChange`](@/api/hooks.md#afterlanguagechange)
  - [`beforeLanguageChange`](@/api/hooks.md#beforelanguagechange)
