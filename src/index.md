---
marp: true
theme: steve
footer: '@pepopowitz | pull-requests.stevenhicks.me'
---

<!-- _class: title -->

![bg opacity:50%](images/cover.jpg)

# Working Effectively<br/>With Pull Requests

### 👦 Steven Hicks

### 🌎 pull-requests.stevenhicks.me

### ✉️ stevenhicks.me/where/

---

<!-- _class: invert -->
<!-- _backgroundColor: black -->

![height:200px center](./images/Logo_White.svg)

<!--
I'm a Developer Experience Engineer at Camunda

Camunda builds a process orchestration platform

I work mainly on the infrastructure for our documentation

Camunda has a booth, come visit!
 -->

---

## 1. What even is a pull request (PR)?

## 2. Ground rules.

## 3. The work before the work.

## 4. Good pull requests.

## 5. Good PR reviews.

## 6. Getting it merged.

## 7. Following up.

---

<!-- section 1: What even is a PR? -->

<!-- _class: invert -->

# 1. What even is a pull request (PR)?

<!-- level-setting -->

---

<!-- _header: "**1: What even is a PR?** | 2 | 3 | 4 | 5 | 6 | 7"  -->

## A pull request (PR) is a request to **incorporate code changes**.

<!--

aka merge request

-->

---

<!-- _header: "**1: What even is a PR?** | 2 | 3 | 4 | 5 | 6 | 7"  -->

## A PR includes a **description**.

todo: image of description field

<!-- summarize the changes you'd like incorporated -->

---

<!-- _header: "**1: What even is a PR?** | 2 | 3 | 4 | 5 | 6 | 7"  -->

## A PR includes **the code changes**.

todo: image of code diff

<!-- represented in a diff format -->

---

<!-- _header: "**1: What even is a PR?** | 2 | 3 | 4 | 5 | 6 | 7"  -->

## A PR is a means to do a **code review**.

---

<!-- _header: "**1: What even is a PR?** _Code review._ | 2 | 3 | 4 | 5 | 6 | 7"  -->

todo: image of talking about the code

<!-- so we can talk about the code changes -->

---

<!-- _header: "**1: What even is a PR?** _Code review._ | 2 | 3 | 4 | 5 | 6 | 7"  -->

todo: image of suggesting changes

<!-- and a reviewer can suggest changes -->

---

<!-- _header: "**1: What even is a PR?** _Code review._ | 2 | 3 | 4 | 5 | 6 | 7"  -->

todo: image of approving

<!-- and in the end, hopefully, the changes are approved. -->

---

<!-- _header: "**1: What even is a PR?** _Code review._ | 2 | 3 | 4 | 5 | 6 | 7"  -->

todo: image of merging

<!-- so that the owner can incorporate the changes -->

---

<!-- _header: "**1: What even is a PR?** | 2 | 3 | 4 | 5 | 6 | 7"  -->

# A PR is **communication** and **collaboration**.

---

<!-- _header: "**1: What even is a PR?** _Communication and collaboration._ | 2 | 3 | 4 | 5 | 6 | 7"  -->

## A PR is an opportunity to **share knowledge**.

<!-- prettier-ignore -->
1) Build shared understanding.
<!-- prettier-ignore -->
2) Mentor.
<!-- prettier-ignore -->
3) Protect against risk.

<!--
an opportunity to share knowledge

1. of our system

2. mentor each other

3. in case one of us wins the lottery

-->

---

<!-- _header: "**1: What even is a PR?** _Communication and collaboration._ | 2 | 3 | 4 | 5 | 6 | 7"  -->

## A PR provides a historical record.

<!-- prettier-ignore -->
1) Explain decisions made.
<!-- prettier-ignore -->
2) For **others** and **future you**.

---

<!-- _header: "**1: What even is a PR?** | 2 | 3 | 4 | 5 | 6 | 7"  -->

# This is a **Pull Request (PR)** talk.

<!-- we'll talk about using pull requests specifically through GitHub  -->
<!-- most of what we're going to talk about is applicable to other source control platforms -->
<!-- there are a couple notes of GitHub specific tooling -->
<!-- you're in the right place if that's what you're looking for -->

---

<!-- _header: "**1: What even is a PR?** | 2 | 3 | 4 | 5 | 6 | 7"  -->

# This is a ~~Pull Request (PR)~~ **culture** talk.

<!-- but more than GitHub, more than pull requests or merge requests, this is a talk about culture -->
<!-- and more specifically, asynchronous collaborative culture -->

---

<!-- section 2: Ground rules -->

<!-- _class: invert -->

# 2. Ground rules.

<!-- we're starting with cultural ground rules for collaborative work -->
<!-- and then we're going to talk about specific actions you can take to improve collaborative coding -->
<!-- but you're going to see all sorts of the culture in the actions -->

---

<!-- _header: "1 | **2: Ground rules.** | 3 | 4 | 5 | 6 | 7"  -->

# Practice **curiosity** over judgement.

<!-- prettier-ignore -->
1) Ask, don't guess.
<!-- prettier-ignore -->
2) Don't make assumptions.

<!-- if something doesn't make sense or seems wrong, ask questions about it -->

---

<!-- _header: "1 | **2: Ground rules.** | 3 | 4 | 5 | 6 | 7"  -->

# ~~Assume positive intent.~~

<!-- ...
we want this slide to say "assume positive intent"
but in an environment that isn't psychologically safe,
"assume positive intent" puts the onus on the abused instead of the abuser.

We can't just magically wave our hands and say "this is now a safe space, you should assume everyone means well."


-->

---

<!-- _header: "1 | **2: Ground rules.** | 3 | 4 | 5 | 6 | 7"  -->

# **Act** with compassion.

1. Act with positive intent.
<!-- prettier-ignore -->

2) Call out bad acts.

<!-- So let's start with what we can control
and focus on building an environment
with enough psychological safety that people can feel more comfortable assuming positive intent

And that starts with you.

...

and it also means enforcing psychological safety by calling out bad acts

-->

---

<!-- _header: "1 | **2: Ground rules.** _Act with compassion._ | 3 | 4 | 5 | 6 | 7"  -->

TODO: image (carrots in a garden)

<!--
I said this is a talk about culture, and I want to share my favorite analogy

of culture as a community garden.

When you find a situation with good culture, it's like walking into a community garden that produces the best fruits and vegetables.

The carrots taste delicious, and you don't want to leave.

But the carrots don't grow themselves. The people in the community cultivate them.

When weeds start to take over, someone needs to pull them.

You can rely on someone else to do it, and still enjoy the carrots,

but you can also contribute.


Calling out bad acts in pull request reviews is a small but important contribution to the weeding of the carrots. It's critical to keeping the garden healthy.

-->

---

<!-- _header: "1 | **2: Ground rules.** | 3 | 4 | 5 | 6 | 7"  -->

# Be aware of **power dynamics**.

<!--
Power dynamics have a huge impact on collaboration, especially in the interpretation of ambiguous communication.

If you think "this doesn't affect me,"
-->

---

<!-- _header: "1 | **2: Ground rules.** _Be aware of power dynamics._ | 3 | 4 | 5 | 6 | 7"  -->

## If you aren't **aware** of a power dynamic, you're probably on the **strong** side of it.

<!--
Power dynamics appear in every relationship we have.
You certainly know about them when you're on the weaker side of it.
And when you don't know about a power dynamic in a relationship, there's a good chance it's because you're on the stronger side.
-->

---

<!-- _header: "1 | **2: Ground rules.** _Be aware of power dynamics._ | 3 | 4 | 5 | 6 | 7"  -->

## Power dynamics can be **conflicting**.

<!--
For example,

I interact with my boss in my PRs every day.
She's my boss - that's one power dynamic, in which I am on the weaker side.

On the other hand, she looks to me for many technical details and decisions.

That's a power dynamic in the opposite direction, and it also appears in the interactions we have in a PR.
-->

---

<!-- _header: "1 | **2: Ground rules.** | 3 | 4 | 5 | 6 | 7"  -->

# Be aware of **power dynamics**.

<!-- prettier-ignore -->
1) Choose words with care and intention.

<!-- prettier-ignore -->
2) Be explicit instead of implicit.

<!--
These exist in almost every relationship we have.

They can be problematic, but we can also navigate them successfully in a team.

We really just need to be aware of them.

...

And the weight of our words, especially when we're on the strong side of the dynamic.

...

I think the best way to avoid misinterpretation of words in a power dynamic

is to be explicit instead of implicit.

When something isn't that important, SAY SO.

When it is important, SAY SO.

Don't leave it up to the reader to interpret.

Feedback from the strong side takes on a very heavy weight. That weight can easily elevate something from "doesn't matter" to "matters very much," even if it doesn't.

-->

---

<!-- _header: "1 | **2: Ground rules.** | 3 | 4 | 5 | 6 | 7"  -->

# **Communicate** effectively.

<!--
this is probably a non-controversial statement
we're all trying to do this in a lot of ways
here are some communication tips that are critical to a good PR interaction.

...

...

If something is unclear, get more information.

...

Make it clear what you will do and what you won't;
what you're expecting and what you're not expecting.

...

Assumptions, context, conclusions...all of these things can easily be misinterpreted. State them explicitly.

...

Example: me saying "what do you think about..." when I meant "we should do make this change"

-->

<!-- prettier-ignore -->
1) Use clear, concise, and unambiguous language.

<!-- prettier-ignore -->
2) Ask clarifying questions.

<!-- prettier-ignore -->
3) Radiate intent.

<!-- prettier-ignore -->
4) State the unstated.

<!-- prettier-ignore -->
5) Be direct (compassionately).

---

<!-- _header: "1 | **2: Ground rules.** | 3 | 4 | 5 | 6 | 7"  -->

# Communicate effectively **asynchronously**.

<!-- prettier-ignore -->
1) Minimize round trips.

<!--
And we need to especially *focus* on asynchronous communication.
Collaborating through PRs is *inherently asynchronous*, and with that comes some *really great* things.
We can *collaborate across time and location*.
People can *respond when it's the right time* for them, because *right now might not be the best time.
So everyone can *take their time before responding*.

And that means we get their

- best focus
- best ideas
- best self

(pause)

But there is *slowness* to asynchronous communication. That can be really *frustrating*.

The most important thing you can do to *prevent that pain*,

...

is to minimize round trips.

And that means doing all the *things we've talked about*.

Providing context, clarity, radiating intent, removing ambiguity

giving the reader enough to go on so that they don't need to ask questions.

-->

---

<!-- _header: "1 | **2: Ground rules.** _Communicate effectively asynchronously._ | 3 | 4 | 5 | 6 | 7"  -->

todo: image of poor text exchange

<!--

Because this is the worst.

Especially when you're working across time zones and you have to wait until tomorrow to see a response.

-->

---

<!-- section 3: The work before the work -->

<!-- _class: invert -->

# 3. The work before the work.

---

<!-- _header: "1 | 2 | **3: The work before the work.** | 4 | 5 | 6 | 7"  -->

---

<!-- section 4: Good pull requests. -->

<!-- _class: invert -->

# 4. Good pull requests.

---

<!-- _header: "1 | 2 | 3 | **4: Good pull requests.** | 5 | 6 | 7"  -->

---

<!-- section 5: Good PR reviews. -->

<!-- _class: invert -->

# 5. Good PR reviews.

---

<!-- _header: "1 | 2 | 3 | 4 | **5: Good PR reviews.** | 6 | 7"  -->

---

<!-- section 6: Getting it merged. -->

<!-- _class: invert -->

# 6. Getting it merged.

---

<!-- _header: "1 | 2 | 3 | 4 | 5 | **6: Getting it merged.** | 7"  -->

---

<!-- section 7: Following up. -->

<!-- _class: invert -->

# 7. Following up.

---

<!-- _header: "1 | 2 | 3 | 4 | 5 | 6 | **7: Following up.**"  -->

---

<!-- _class: invert title -->

# Thank you!

##### 👦 Steven Hicks

##### 🌎 pull-requests.stevenhicks.me

##### ✉️ stevenhicks.me/where/

---

<!-- _class: invert -->

## everything past this is a sample layout

---

## Slide 1

- Item 1
- Item 2
- Item 3

<!-- HTML comment will recognize as presenter notes. -->

<!-- these are definitely notes!!! -->
<!-- are these notes 2? -->
<!-- is this a
really

really

long

note? -->

---

<!-- _class: invert -->

## Slide 2

![bg Image](https://picsum.photos/800/600)

---

<!-- _class: invert -->

## Slide 3

> This is a quote.

---

## Slide 4

| Column 1 | Column 2 |
| -------- | -------- |
| Item 1   | Item 2   |
| Item 3   | Item 4   |

---

## Slide 5

### With Some Subheadings

#### Like this
