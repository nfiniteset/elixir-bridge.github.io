---
layout: page
title: Creating Votes
date: 2016-08-28 12:30:04 -0700
position: 10
---
### Voting On Topics

### Goals
* Create a model for votes

<table class="model-diagram">
<thead><tr><th>Votes</th></tr></thead>
<tbody>
<tr><td>id</td></tr>
<tr><td>topic_id</td></tr>
</tbody>
</table>

Every topic in suggestotron can be voted on. In order to count votes, we need to record votes. We'll add that table now.

## Steps
Type this in the terminal:
```
mix phoenix.gen.model Vote votes topic_id:integer
mix ecto.migrate
```

### Explanation

Just like before, we're creating a new model named "vote."
The only thing really different is the integer we added called topic_id.
topic_id is the data we need to draw the line between votes and topics.
We didn't generate a full scaffold this time because we aren't going to do the full CRUD for votes; they're just going to be considered part of topics as-is. After we've created the model and migrations, we run them so the database also has our changes.
