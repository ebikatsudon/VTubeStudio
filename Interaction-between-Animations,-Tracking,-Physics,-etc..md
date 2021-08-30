In VTube Studio, Live2D parameters can be controlled by various entities, such as Live2D Animations, face tracking or Live2D Expressions. But what happens when animations, face tracking and expressions try to write to the same Live2D parameter at the same time? That is explained in this chapter.

In VTube Studio, each Live2D parameter can be controlled by one of six "value-providers". In order of priority (lowest to highest), they are:


| Priority | Value-Provider | Notes |
| -------- | -------------- | ----- |
| **P0** | Default Live2D parameter value | Available for every Live2D parameter |
| **P1** | Value from Idle Animation | |
| **P2** | Value from Face Tracking | |
| **P3** | Value from One-Time Animation | As long as animation is active |
| **P4** | Value from Live2D Expression | As long as expression is active |
| **P5** | Value from Physics System | |

The final value of an individual Live2D parameter in your model will be determined by the highest-priority active value provider. For example, when a Live2D parameter called ParamA has a one-time animation (triggered by hotkey) writing to it, any values from the face tracking or idle animation are overwritten.

Once the one-time animation ends, control will be passed back to the active value-provider with the next highest priority.

Specifically, this means that the face tracking would now control ParamA if ParamA is set as an output parameter in your VTS model config. If not, ParamA will now be controlled by the idle animation. Or, if the idle animation also does not contain ParamA, it will be set to its default value, which every Live2D parameter has.

When control of a Live2D parameter is passed between value-providers, it is always faded smoothly and not just set instantly to prevent any ugly jumps.
