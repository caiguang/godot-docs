:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/4.2/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/4.2/doc/classes/AnimationNodeTransition.xml.

.. _class_AnimationNodeTransition:

AnimationNodeTransition
=======================

**继承：** :ref:`AnimationNodeSync<class_AnimationNodeSync>` **<** :ref:`AnimationNode<class_AnimationNode>` **<** :ref:`Resource<class_Resource>` **<** :ref:`RefCounted<class_RefCounted>` **<** :ref:`Object<class_Object>`

:ref:`AnimationTree<class_AnimationTree>` 中连接两个 :ref:`AnimationNode<class_AnimationNode>` 的过渡。

.. rst-class:: classref-introduction-group

描述
----

适用于不需要更高级 :ref:`AnimationNodeStateMachine<class_AnimationNodeStateMachine>` 的情况的简单状态机。可以将动画连接到输入，还可以指定过渡时间。

设置请求并更改动画播放后，过渡节点会在下一个处理帧中通过将其 ``transition_request`` 值设置为空，来自动清除请求。

\ **注意：**\ 使用交叉淡入淡出时，\ ``current_state`` 和 ``current_index`` 在交叉淡入淡出开始后立即更改为下一个状态。


.. tabs::

 .. code-tab:: gdscript

    # 播放连接到 “state_2” 端口的子动画。
    animation_tree.set("parameters/Transition/transition_request", "state_2")
    # 替代语法（与上述结果相同）。
    animation_tree["parameters/Transition/transition_request"] = "state_2"
    
    # 获取当前状态名称（只读）。
    animation_tree.get("parameters/Transition/current_state")
    # 替代语法（与上述结果相同）。
    animation_tree["parameters/Transition/current_state"]
    
    # 获取当前状态索引（只读）。
    animation_tree.get("parameters/Transition/current_index"))
    # 替代语法（与上述结果相同）。
    animation_tree["parameters/Transition/current_index"]

 .. code-tab:: csharp

    // 播放连接到 “state_2” 端口的子动画。
    animationTree.Set("parameters/Transition/transition_request", "state_2");
    
    // 获取当前状态名称（只读）。
    animationTree.Get("parameters/Transition/current_state");
    
    // 获取当前状态索引（只读）。
    animationTree.Get("parameters/Transition/current_index");



.. rst-class:: classref-introduction-group

教程
----

- :doc:`使用 AnimationTree <../tutorials/animation/animation_tree>`

- `3D 平台跳跃演示 <https://godotengine.org/asset-library/asset/125>`__

- `第三人称射击演示 <https://godotengine.org/asset-library/asset/678>`__

.. rst-class:: classref-reftable-group

属性
----

.. table::
   :widths: auto

   +---------------------------+--------------------------------------------------------------------------------------------------+-----------+
   | :ref:`bool<class_bool>`   | :ref:`allow_transition_to_self<class_AnimationNodeTransition_property_allow_transition_to_self>` | ``false`` |
   +---------------------------+--------------------------------------------------------------------------------------------------+-----------+
   | :ref:`int<class_int>`     | :ref:`input_count<class_AnimationNodeTransition_property_input_count>`                           | ``0``     |
   +---------------------------+--------------------------------------------------------------------------------------------------+-----------+
   | :ref:`Curve<class_Curve>` | :ref:`xfade_curve<class_AnimationNodeTransition_property_xfade_curve>`                           |           |
   +---------------------------+--------------------------------------------------------------------------------------------------+-----------+
   | :ref:`float<class_float>` | :ref:`xfade_time<class_AnimationNodeTransition_property_xfade_time>`                             | ``0.0``   |
   +---------------------------+--------------------------------------------------------------------------------------------------+-----------+

.. rst-class:: classref-reftable-group

方法
----

.. table::
   :widths: auto

   +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`bool<class_bool>` | :ref:`is_input_reset<class_AnimationNodeTransition_method_is_input_reset>` **(** :ref:`int<class_int>` input **)** |const|                                               |
   +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`bool<class_bool>` | :ref:`is_input_set_as_auto_advance<class_AnimationNodeTransition_method_is_input_set_as_auto_advance>` **(** :ref:`int<class_int>` input **)** |const|                   |
   +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | void                    | :ref:`set_input_as_auto_advance<class_AnimationNodeTransition_method_set_input_as_auto_advance>` **(** :ref:`int<class_int>` input, :ref:`bool<class_bool>` enable **)** |
   +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | void                    | :ref:`set_input_reset<class_AnimationNodeTransition_method_set_input_reset>` **(** :ref:`int<class_int>` input, :ref:`bool<class_bool>` enable **)**                     |
   +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

属性说明
--------

.. _class_AnimationNodeTransition_property_allow_transition_to_self:

.. rst-class:: classref-property

:ref:`bool<class_bool>` **allow_transition_to_self** = ``false``

.. rst-class:: classref-property-setget

- void **set_allow_transition_to_self** **(** :ref:`bool<class_bool>` value **)**
- :ref:`bool<class_bool>` **is_allow_transition_to_self** **(** **)**

如果为 ``true``\ ，允许过渡到当前状态。当在输入中启用重置选项时，动画将重新启动。如果为 ``false``\ ，则在过渡到 当前状态时不会发生任何事情。

.. rst-class:: classref-item-separator

----

.. _class_AnimationNodeTransition_property_input_count:

.. rst-class:: classref-property

:ref:`int<class_int>` **input_count** = ``0``

.. rst-class:: classref-property-setget

- void **set_input_count** **(** :ref:`int<class_int>` value **)**
- :ref:`int<class_int>` **get_input_count** **(** **)**

这个动画节点启用的输入端口的数量。

.. rst-class:: classref-item-separator

----

.. _class_AnimationNodeTransition_property_xfade_curve:

.. rst-class:: classref-property

:ref:`Curve<class_Curve>` **xfade_curve**

.. rst-class:: classref-property-setget

- void **set_xfade_curve** **(** :ref:`Curve<class_Curve>` value **)**
- :ref:`Curve<class_Curve>` **get_xfade_curve** **(** **)**

确定如何缓动动画之间的淡入淡出。如果为空，过渡将是线性的。

.. rst-class:: classref-item-separator

----

.. _class_AnimationNodeTransition_property_xfade_time:

.. rst-class:: classref-property

:ref:`float<class_float>` **xfade_time** = ``0.0``

.. rst-class:: classref-property-setget

- void **set_xfade_time** **(** :ref:`float<class_float>` value **)**
- :ref:`float<class_float>` **get_xfade_time** **(** **)**

连接到输入的每个动画之间的交叉渐变时间（秒）。

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

方法说明
--------

.. _class_AnimationNodeTransition_method_is_input_reset:

.. rst-class:: classref-method

:ref:`bool<class_bool>` **is_input_reset** **(** :ref:`int<class_int>` input **)** |const|

返回当动画从另一个动画过渡时，该动画是否重新开始。

.. rst-class:: classref-item-separator

----

.. _class_AnimationNodeTransition_method_is_input_set_as_auto_advance:

.. rst-class:: classref-method

:ref:`bool<class_bool>` **is_input_set_as_auto_advance** **(** :ref:`int<class_int>` input **)** |const|

如果为给定的 ``input`` 索引启用了自动前进，则返回 ``true``\ 。

.. rst-class:: classref-item-separator

----

.. _class_AnimationNodeTransition_method_set_input_as_auto_advance:

.. rst-class:: classref-method

void **set_input_as_auto_advance** **(** :ref:`int<class_int>` input, :ref:`bool<class_bool>` enable **)**

为给定的 ``input`` 索引启用或禁用自动前进。如果启用，状态会在播放一次动画后更改为下一个输入。如果为最后一个输入状态启用，它会循环到第一个。

.. rst-class:: classref-item-separator

----

.. _class_AnimationNodeTransition_method_set_input_reset:

.. rst-class:: classref-method

void **set_input_reset** **(** :ref:`int<class_int>` input, :ref:`bool<class_bool>` enable **)**

如果为 ``true``\ ，则目标动画在动画过渡时重新启动。

.. |virtual| replace:: :abbr:`virtual (本方法通常需要用户覆盖才能生效。)`
.. |const| replace:: :abbr:`const (本方法没有副作用。不会修改该实例的任何成员变量。)`
.. |vararg| replace:: :abbr:`vararg (本方法除了在此处描述的参数外，还能够继续接受任意数量的参数。)`
.. |constructor| replace:: :abbr:`constructor (本方法用于构造某个类型。)`
.. |static| replace:: :abbr:`static (调用本方法无需实例，所以可以直接使用类名调用。)`
.. |operator| replace:: :abbr:`operator (本方法描述的是使用本类型作为左操作数的有效操作符。)`
.. |bitfield| replace:: :abbr:`BitField (这个值是由下列标志构成的位掩码整数。)`
