---
layout: post
title:  "Postgres Query Issue"
date:   2022-11-04 19:00:00 -0400
categories: Postgres Rails
---

During my first RubyConf I got a chance to meet Jim Remsik, founder of
[Flagrant](https://www.beflagrant.com/). He invited me to be a part of Flagrant
developer round table for external dev can come and learn. This past friday we
discuss an issue with a particular query taking a long time to execute.

We used Postgres through the interactive shell to view the query.
I learned how to use EXPLAIN, in both postgres and in active record for rails.
- [Thoughtbot - Postgres Explain](https://thoughtbot.com/blog/reading-an-explain-analyze-query-plan)
- [Rails - Active Record Explain](https://guides.rubyonrails.org/active_record_querying.html#running-explain)
- [GoRails - Active Record Explain](https://gorails.com/episodes/activerecord-explain)

I learned that postgres can change the type of scan performed based on the number
of items it is querying. For example if we are only querying 10 items it will
perform a index scan but if we were to scan over a 1000 record it switches over
to a sequential scan

**Index only Scan**
 - scans the data structure corresponding to the index involved in the query and locate required data clause with very minimal scans.

**Sequential Scan**
 - scans the whole table to select a record

to be continued...
