# toastmaster-light
automate toastmaster timer lights
http://toastmasters.arizona.edu/sites/toastmasters/files/template_for_timer_role_and_responsibilities2.pdf

```
Feature: Toastmaster timer
In order indicate how much time the speaker has spoken
As a toastmasters timer
I want to indicate the 3 milestones (Green, Amber and Red)
```
# Generation 1
```
Scenario Outline: flick switch to change light color from Off to Green to Amber To Red and back again
  Given the light is <light-before-state>
  When I flick the switch
  Then the light turns <light-after-state>
  
  Examples:
    |light-before-state|light-aftetr-state|
    |Off               |Green             |
    |Green             |Amber             |
    |Amber             |Red               |
    |Red               |Off               |
```    
# Generation 2
```
Scenario Outline: set time to automatically change light color from Off to Green to Amber To Red and back again
```
