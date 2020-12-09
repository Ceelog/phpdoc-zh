Periodic watcher operation modes
================================

<span class="classname">EvPeriodic</span> watcher works in different
modes depending on the `offset` , `interval` and `reschedule_cb`
parameters.

1.  *Absolute timer* . In this mode `interval` = **`0`** ,
    `reschedule_cb` = **`null`**. This time simply fires at the
    wallclock time `offset` and doesn't repeat. It will not adjust when
    a time jump occurs, that is, if it is to be run at *January 1st
    2014* then it will run when the system time reaches or surpasses
    this time.

2.  *Repeating interval timer* . In this mode `interval` \> **`0`** ,
    `reschedule_cb` = **`null`**; the watcher will always be scheduled
    to timeout at the next `offset` + **`N`** \* `interval` time(for
    some integer **`N`** ) and then repeat, regardless of any time
    jumps.

    This can be used to create timers that do not drift with respect to
    system time:

    ``` php
    <?php
    $hourly = EvPeriodic(0, 3600, NULL, function () {
      echo "once per hour\n";
    });
    ?>
    ```

    That doesn't mean there will always be **`3600`** seconds in between
    triggers, but only that the callback will be called when the system
    time shows a full hour( *UTC* ).

    <span class="classname">EvPeriodic</span> will try to run the
    callback in this mode at the next possible time where `time` =
    `offset` ( *mod* `interval` ), regardless of any time jumps.

3.  *Manual reschedule mode* . In this mode `reschedule_cb` is a <span
    class="type">callable</span> .

    `interval` and `offset` are both being ignored. Instead, each time
    the periodic watcher gets scheduled, the reschedule callback (
    `reschedule_cb` ) will be called with the watcher as first, and the
    current time as second argument.

    This callback *must not* stop or destroy this or any other periodic
    watchers, ever, and *must not* call any event loop functions or
    methods. To stop it return **`1e30`** and stop it afterwards. An
    <span class="classname">EvPrepare</span> watcher may be used for
    this task.

    It must return the next time to trigger, based on the passed time
    value (that is, the lowest time value larger than or equal to the
    second argument). It will usually be called just before the callback
    will be triggered, but might be called at other times, too.

    **示例 \#1 Using reschedule callback**

    ``` php
    <?php
    // Tick each 10.5 seconds

    function reschedule_cb ($watcher, $now) {
       return $now + (10.5. - fmod($now, 10.5));
    }

    $w = new EvPeriodic(0., 0., "reschedule_cb", function ($w, $revents) {
       echo time(), PHP_EOL;
    });

    Ev::run();
    ?>
    ```
