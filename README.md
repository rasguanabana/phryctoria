# Phryctoria
Event-driven stuff

## What?
Distributed event-driven automation, CI/CD, scheduler, or something around that. I don't have a good term for that for now. Generally, you define tasks and tell the system when to run them by subscribing them to specific events emitted by other tasks. Since it's distributed it probably will use Kubernetes for managing compute resources and for exposing components resposible for interacting with outside world. We'll see how it goes.

## Why?
* I hated Jenkins a few years ago and wanted to build something *better* (yeah, right)
* Extending Jenkins is not trivial; I want to make extending Phryctoria dead-simple. I was very frustrated with Jenkins when a plugin was useless just because it lacked a single knob
* I wanted to learn Erlang
* Now I need a side project and still want to learn Erlang and to brush up on K8s

### Why Erlang?
It promises resiliency, easy concurrency and distribution. Messages should get event handling fairly easy, too.

### Why not Elixir?
Dunno, might switch.

### Why the name?
Fire signals over some distance sound quite event-driven to me.

## How?
Hmm. I have a lot of thoughts written down on paper in 2017. The simplest explanation I can't think of is that there will be a central scheduler/dependency resolver listening for events coming from tasks or system. It will start tasks which are subscribed to an event. Subscription requires a selector which tells what kind of series of events you want to happen before triggering a task.
For clean env tasks are going to always run in containers (I dind't say Docker!).
Phryctoria shall provide facilities to record results. K8s might be helpful for getting files persisted.

## When?
It'll be a success if I even start. Until recently I was anxious about publishing anything until something works and about someone stealing the idea. Why should I? Now I commit from scratch publicly to motivate myself to do something besides my day job.
