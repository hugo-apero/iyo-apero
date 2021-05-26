---
title: "Lorem Star Wars"
subtitle: "How to add panelsets in plain markdown posts."
excerpt: "Add tabbed sections to your posts."
date: 2021-05-25
author: "Alison Hill"
draft: false
# layout options: single, single-sidebar
layout: single
categories:
- Theme features
---

{{< here >}}

## But first, a shortcode trick

Courtesy of panelset.js by Garrick Aden-Buie, from his xaringanExtra package: https://pkg.garrickadenbuie.com/xaringanExtra/#/panelset

For example, this panelset:

{{< panelset class="greetings" >}}
{{< panel name="Hello! :wave:" >}}
  hello
{{< /panel >}}
{{< panel name="Goodbye :dash:" >}}
  goodbye
{{< /panel >}}
{{< /panelset  >}}

Was created by combining this theme's `panelset` and `panel` shortcodes:

```go
{{</* panelset class="greetings" */>}}
{{</* panel name="Hello! :wave:" */>}}
  hello
{{</* /panel */>}}
{{</* panel name="Goodbye :dash:" */>}}
  goodbye
{{</* /panel */>}}
{{</* /panelset */>}}
```

## Escape is not his plan. I must face him, alone.

I'm surprised you had the courage to take the responsibility yourself. I don't know what you're talking about. I am a member of the Imperial Senate on a diplomatic mission to Alderaan-- Kid, I've flown from one side of this galaxy to the other. I've seen a lot of strange stuff, but I've never seen anything to make me believe there's one all-powerful Force controlling everything. There's no mystical energy field that controls my destiny. It's all a lot of simple tricks and nonsense.

What good is a reward if you ain't around to use it? Besides, attacking that battle station ain't my idea of courage. __It's more like…suicide.__ *I have traced the Rebel spies to her.* Now she is my only link to finding their secret base.

## Still, she's got a lot of spirit. I don't know, what do you think?

Still, she's got a lot of spirit. I don't know, what do you think? Dantooine. They're on Dantooine. I'm trying not to, kid. You are a part of the Rebel Alliance and a traitor! Take her away! A tremor in the Force. The last time I felt it was in the presence of my old master.

1. You don't believe in the Force, do you?
2. Don't be too proud of this technological terror you've constructed. The ability to destroy a planet is insignificant next to the power of the Force.
3. Don't act so surprised, Your Highness. You weren't on any mercy mission this time. Several transmissions were beamed to this ship by Rebel spies. I want to know what happened to the plans they sent you.

### You don't believe in the Force, do you?

I need your help, Luke. She needs your help. I'm getting too old for this sort of thing. In my experience, there is no such thing as luck. What!? I suggest you try it again, Luke. This time, let go your conscious self and act on instinct.

* Hey, Luke! May the Force be with you.
* I care. So, what do you think of her, Han?
* She must have hidden the plans in the escape pod. Send a detachment down to retrieve them, and see to it personally, Commander. There'll be no one to stop us this time!

The more you tighten your grip, Tarkin, the more star systems will slip through your fingers. Obi-Wan is here. The Force is with him. Remember, a Jedi can feel the Force flowing through him. What!?

But with the blast shield down, I can't even see! How am I supposed to fight? Don't be too proud of this technological terror you've constructed. The ability to destroy a planet is insignificant next to the power of the Force.

Hokey religions and ancient weapons are no match for a good blaster at your side, kid. I have traced the Rebel spies to her. Now she is my only link to finding their secret base. The plans you refer to will soon be back in our hands.

Hokey religions and ancient weapons are no match for a good blaster at your side, kid. Leave that to me. Send a distress signal, and inform the Senate that all on board were killed. Look, I can take you as far as Anchorhead. You can get a transport there to Mos Eisley or wherever you're going.

Obi-Wan is here. The Force is with him. Oh God, my uncle. How am I ever gonna explain this? Partially, but it also obeys your commands. Kid, I've flown from one side of this galaxy to the other. I've seen a lot of strange stuff, but I've never seen anything to make me believe there's one all-powerful Force controlling everything. There's no mystical energy field that controls my destiny. It's all a lot of simple tricks and nonsense.

I call it luck. I need your help, Luke. She needs your help. I'm getting too old for this sort of thing. Ye-ha! You're all clear, kid. Let's blow this thing and go home! In my experience, there is no such thing as luck.

The Force is strong with this one. I have you now. What?! But with the blast shield down, I can't even see! How am I supposed to fight? You don't believe in the Force, do you? Ye-ha!

The Force is strong with this one. I have you now. He is here. A tremor in the Force. The last time I felt it was in the presence of my old master. I'm surprised you had the courage to take the responsibility yourself.

I have traced the Rebel spies to her. Now she is my only link to finding their secret base. Oh God, my uncle. How am I ever gonna explain this? What?! A tremor in the Force. The last time I felt it was in the presence of my old master.

Kid, I've flown from one side of this galaxy to the other. I've seen a lot of strange stuff, but I've never seen anything to make me believe there's one all-powerful Force controlling everything. There's no mystical energy field that controls my destiny. It's all a lot of simple tricks and nonsense. Don't underestimate the Force.

I don't know what you're talking about. I am a member of the Imperial Senate on a diplomatic mission to Alderaan-- The more you tighten your grip, Tarkin, the more star systems will slip through your fingers.
