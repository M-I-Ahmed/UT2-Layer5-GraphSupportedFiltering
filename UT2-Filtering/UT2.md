This folder contains the scripts to conduct unit test 2 and this file contains a description of what is being tested.

The purpose of this test is to evaluate the difference between a system that uses purely GenAI to create cypher queries and a system that uses the AI to extraxt intent and have an intermediary translation step before the cypher query.

This experiment is conducted in isolation of UT1 and the results of it because we need to ensure the trap apps are passed into this layer to prove it can successfully filter them out.

If layer 1 doesn't let them pass through then it will appear as though this test has been successful and they have been filtered out, when in reality they weren't even in the pool in the first place. Cascading error

To evaluate this, we will use 6 LLMs to create the cypher queries and then use these same models for the JSON translation stage. 

Need a script that lists all of the relationship types