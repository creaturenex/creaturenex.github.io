---
layout: post
title:  "Meeting with Han Yu from Docker"
date:   2024-03-13 08:00:00 -0500
categories: docker
---

Today I got a change to speak with [Han Yu](https://www.linkedin.com/in/hanyu/). I reached out after attending her [presentation](https://shipyard.build/blog/2024-state-of-compose-recap/) on the 2024 State of Compose, which was hosted by [Shipyard](https://shipyard.build/).

_Bonus Points_ Han remembered me from the talk because I was a very engaged audience member and had a question regarding build time with rails containers.

I was interested in digging into...

- **What are some atypical usage of docker compose and are there any examples to learn from?**
  - Han:
    - CI - think workflows that test code in PR etc
    - massive compose configurations with multiple services
    - examples @ [Awesome Compose](https://github.com/docker/awesome-compose)

- **How can I contribute to docker compose**
  - Han:
    - docker compose is pretty much stable ie not a lot of new feature being added
      - Mostly documentation issue
    - That being said cool new features include
      - watch
      - include
      - dry run
    - Consider contributing to
      - [Awesome Compose](https://github.com/docker/awesome-compose)
      - This is good idea because it has examples for many different languages and frameworks

While my meeting was short I did gain some new information. Next time I will try to write down everything as I am pretty sure I am forgetting something.
