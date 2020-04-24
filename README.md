# hamster
Offline gitlab runner

**ALPHA**

Tired of having to 'register' runners?

Just want a runner that doesn't run in a container, but tries to just, you know, run the stuff?

# What does hamster honor?

`hamster stage_name` will run all targets in a stage.
`hamster target_name` will run that specific target.

E.g. with this for your `.gitlab-ci.yml`:
```
goodbye:
  stage: primary_stage
  variables:
    GOODBYE: "tara"
  script:
    - echo $GOODBYE a bit
```
then `hamster goodbye` would output `tara a bit`.
