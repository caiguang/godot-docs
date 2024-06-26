:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/4.2/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/4.2/modules/openxr/doc_classes/OpenXRHand.xml.

.. _class_OpenXRHand:

OpenXRHand
==========

**继承：** :ref:`Node3D<class_Node3D>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

在 OpenXR 中提供手指跟踪的节点。

.. rst-class:: classref-introduction-group

描述
----

该节点启用 OpenXR 的手部跟踪功能。该节点应该是 :ref:`XROrigin3D<class_XROrigin3D>` 节点的一个子节点，跟踪会将其位置更新为玩家的实际手所在的位置。该节点还更新了适当蒙皮的手部模型的骨架。手部网格应该是该节点的一个子节点。

.. rst-class:: classref-reftable-group

属性
----

.. table::
   :widths: auto

   +-------------------------------------------------+---------------------------------------------------------------+------------------+
   | :ref:`Hands<enum_OpenXRHand_Hands>`             | :ref:`hand<class_OpenXRHand_property_hand>`                   | ``0``            |
   +-------------------------------------------------+---------------------------------------------------------------+------------------+
   | :ref:`NodePath<class_NodePath>`                 | :ref:`hand_skeleton<class_OpenXRHand_property_hand_skeleton>` | ``NodePath("")`` |
   +-------------------------------------------------+---------------------------------------------------------------+------------------+
   | :ref:`MotionRange<enum_OpenXRHand_MotionRange>` | :ref:`motion_range<class_OpenXRHand_property_motion_range>`   | ``0``            |
   +-------------------------------------------------+---------------------------------------------------------------+------------------+

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

枚举
----

.. _enum_OpenXRHand_Hands:

.. rst-class:: classref-enumeration

enum **Hands**:

.. _class_OpenXRHand_constant_HAND_LEFT:

.. rst-class:: classref-enumeration-constant

:ref:`Hands<enum_OpenXRHand_Hands>` **HAND_LEFT** = ``0``

追踪玩家的左手。

.. _class_OpenXRHand_constant_HAND_RIGHT:

.. rst-class:: classref-enumeration-constant

:ref:`Hands<enum_OpenXRHand_Hands>` **HAND_RIGHT** = ``1``

追踪玩家的右手。

.. _class_OpenXRHand_constant_HAND_MAX:

.. rst-class:: classref-enumeration-constant

:ref:`Hands<enum_OpenXRHand_Hands>` **HAND_MAX** = ``2``

最大支持的手数。

.. rst-class:: classref-item-separator

----

.. _enum_OpenXRHand_MotionRange:

.. rst-class:: classref-enumeration

enum **MotionRange**:

.. _class_OpenXRHand_constant_MOTION_RANGE_UNOBSTRUCTED:

.. rst-class:: classref-enumeration-constant

:ref:`MotionRange<enum_OpenXRHand_MotionRange>` **MOTION_RANGE_UNOBSTRUCTED** = ``0``

玩家抓握时，手部骨架呈握拳状。

.. _class_OpenXRHand_constant_MOTION_RANGE_CONFORM_TO_CONTROLLER:

.. rst-class:: classref-enumeration-constant

:ref:`MotionRange<enum_OpenXRHand_MotionRange>` **MOTION_RANGE_CONFORM_TO_CONTROLLER** = ``1``

玩家抓握时，手部骨架遵循玩家所持的控制器。

.. _class_OpenXRHand_constant_MOTION_RANGE_MAX:

.. rst-class:: classref-enumeration-constant

:ref:`MotionRange<enum_OpenXRHand_MotionRange>` **MOTION_RANGE_MAX** = ``2``

最大支持的运动范围。

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

属性说明
--------

.. _class_OpenXRHand_property_hand:

.. rst-class:: classref-property

:ref:`Hands<enum_OpenXRHand_Hands>` **hand** = ``0``

.. rst-class:: classref-property-setget

- void **set_hand** **(** :ref:`Hands<enum_OpenXRHand_Hands>` value **)**
- :ref:`Hands<enum_OpenXRHand_Hands>` **get_hand** **(** **)**

指定该节点是追踪玩家的左手还是右手。

.. rst-class:: classref-item-separator

----

.. _class_OpenXRHand_property_hand_skeleton:

.. rst-class:: classref-property

:ref:`NodePath<class_NodePath>` **hand_skeleton** = ``NodePath("")``

.. rst-class:: classref-property-setget

- void **set_hand_skeleton** **(** :ref:`NodePath<class_NodePath>` value **)**
- :ref:`NodePath<class_NodePath>` **get_hand_skeleton** **(** **)**

设置一个\ :ref:`Skeleton3D<class_Skeleton3D>`\ 节点，该节点的姿势位置将被更新。

.. rst-class:: classref-item-separator

----

.. _class_OpenXRHand_property_motion_range:

.. rst-class:: classref-property

:ref:`MotionRange<enum_OpenXRHand_MotionRange>` **motion_range** = ``0``

.. rst-class:: classref-property-setget

- void **set_motion_range** **(** :ref:`MotionRange<enum_OpenXRHand_MotionRange>` value **)**
- :ref:`MotionRange<enum_OpenXRHand_MotionRange>` **get_motion_range** **(** **)**

设置限制手部运动的运动范围（前提是支持）。

.. |virtual| replace:: :abbr:`virtual (本方法通常需要用户覆盖才能生效。)`
.. |const| replace:: :abbr:`const (本方法没有副作用。不会修改该实例的任何成员变量。)`
.. |vararg| replace:: :abbr:`vararg (本方法除了在此处描述的参数外，还能够继续接受任意数量的参数。)`
.. |constructor| replace:: :abbr:`constructor (本方法用于构造某个类型。)`
.. |static| replace:: :abbr:`static (调用本方法无需实例，所以可以直接使用类名调用。)`
.. |operator| replace:: :abbr:`operator (本方法描述的是使用本类型作为左操作数的有效操作符。)`
.. |bitfield| replace:: :abbr:`BitField (这个值是由下列标志构成的位掩码整数。)`
