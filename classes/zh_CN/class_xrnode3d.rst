:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/4.2/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/4.2/doc/classes/XRNode3D.xml.

.. _class_XRNode3D:

XRNode3D
========

**继承：** :ref:`Node3D<class_Node3D>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

**派生：** :ref:`XRAnchor3D<class_XRAnchor3D>`, :ref:`XRController3D<class_XRController3D>`

空间节点，位置由 :ref:`XRServer<class_XRServer>` 自动更新。

.. rst-class:: classref-introduction-group

描述
----

这个节点可以绑定到 :ref:`XRPositionalTracker<class_XRPositionalTracker>` 的某个姿势，\ :ref:`XRServer<class_XRServer>` 会自动更新其 :ref:`Node3D.transform<class_Node3D_property_transform>`\ 。这类节点必须添加为 :ref:`XROrigin3D<class_XROrigin3D>` 节点的子节点。

.. rst-class:: classref-introduction-group

教程
----

- :doc:`XR 文档索引 <../tutorials/xr/index>`

.. rst-class:: classref-reftable-group

属性
----

.. table::
   :widths: auto

   +-------------------------------------+-------------------------------------------------+----------------+
   | :ref:`StringName<class_StringName>` | :ref:`pose<class_XRNode3D_property_pose>`       | ``&"default"`` |
   +-------------------------------------+-------------------------------------------------+----------------+
   | :ref:`StringName<class_StringName>` | :ref:`tracker<class_XRNode3D_property_tracker>` | ``&""``        |
   +-------------------------------------+-------------------------------------------------+----------------+

.. rst-class:: classref-reftable-group

方法
----

.. table::
   :widths: auto

   +-----------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`bool<class_bool>`     | :ref:`get_has_tracking_data<class_XRNode3D_method_get_has_tracking_data>` **(** **)** |const|                                                                                                                                                                                      |
   +-----------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`bool<class_bool>`     | :ref:`get_is_active<class_XRNode3D_method_get_is_active>` **(** **)** |const|                                                                                                                                                                                                      |
   +-----------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`XRPose<class_XRPose>` | :ref:`get_pose<class_XRNode3D_method_get_pose>` **(** **)**                                                                                                                                                                                                                        |
   +-----------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | void                        | :ref:`trigger_haptic_pulse<class_XRNode3D_method_trigger_haptic_pulse>` **(** :ref:`String<class_String>` action_name, :ref:`float<class_float>` frequency, :ref:`float<class_float>` amplitude, :ref:`float<class_float>` duration_sec, :ref:`float<class_float>` delay_sec **)** |
   +-----------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

信号
----

.. _class_XRNode3D_signal_tracking_changed:

.. rst-class:: classref-signal

**tracking_changed** **(** :ref:`bool<class_bool>` tracking **)**

当 :ref:`tracker<class_XRNode3D_property_tracker>` 开始或停止接收正被跟踪的 :ref:`pose<class_XRNode3D_property_pose>` 的更新跟踪数据时发出。\ ``tracking`` 参数指示跟踪器是否正在获取更新的跟踪数据。

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

属性说明
--------

.. _class_XRNode3D_property_pose:

.. rst-class:: classref-property

:ref:`StringName<class_StringName>` **pose** = ``&"default"``

.. rst-class:: classref-property-setget

- void **set_pose_name** **(** :ref:`StringName<class_StringName>` value **)**
- :ref:`StringName<class_StringName>` **get_pose_name** **(** **)**

我们绑定到的姿势的名称。设计时并不知道跟踪器支持哪些姿势。

Godot 定义了许多标准姿势名称，例如 ``aim`` 和 ``grip``\ ，但也可以在给定的 :ref:`XRInterface<class_XRInterface>` 中配置其他名称。

.. rst-class:: classref-item-separator

----

.. _class_XRNode3D_property_tracker:

.. rst-class:: classref-property

:ref:`StringName<class_StringName>` **tracker** = ``&""``

.. rst-class:: classref-property-setget

- void **set_tracker** **(** :ref:`StringName<class_StringName>` value **)**
- :ref:`StringName<class_StringName>` **get_tracker** **(** **)**

我们绑定到的追踪器的名称。设计时并不知道有哪些跟踪器可用。

Godot 定义了许多标准跟踪器，例如 ``left_hand`` 和 ``right_hand``\ ，但也可以在给定的 :ref:`XRInterface<class_XRInterface>` 中配置其他跟踪器。

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

方法说明
--------

.. _class_XRNode3D_method_get_has_tracking_data:

.. rst-class:: classref-method

:ref:`bool<class_bool>` **get_has_tracking_data** **(** **)** |const|

如果 :ref:`tracker<class_XRNode3D_property_tracker>` 中有被跟踪 :ref:`pose<class_XRNode3D_property_pose>` 的当前跟踪数据，则返回 ``true``\ 。

.. rst-class:: classref-item-separator

----

.. _class_XRNode3D_method_get_is_active:

.. rst-class:: classref-method

:ref:`bool<class_bool>` **get_is_active** **(** **)** |const|

如果 :ref:`tracker<class_XRNode3D_property_tracker>` 已注册，并且 :ref:`pose<class_XRNode3D_property_pose>` 正在被追踪，则返回 ``true``\ 。

.. rst-class:: classref-item-separator

----

.. _class_XRNode3D_method_get_pose:

.. rst-class:: classref-method

:ref:`XRPose<class_XRPose>` **get_pose** **(** **)**

返回包含被跟踪姿势的当前状态的 :ref:`XRPose<class_XRPose>`\ 。这可以访问此姿势的其他属性。

.. rst-class:: classref-item-separator

----

.. _class_XRNode3D_method_trigger_haptic_pulse:

.. rst-class:: classref-method

void **trigger_haptic_pulse** **(** :ref:`String<class_String>` action_name, :ref:`float<class_float>` frequency, :ref:`float<class_float>` amplitude, :ref:`float<class_float>` duration_sec, :ref:`float<class_float>` delay_sec **)**

在与此接口关联的设备上触发触觉脉冲。

\ ``action_name`` 是该脉冲的动作名称。

.. |virtual| replace:: :abbr:`virtual (本方法通常需要用户覆盖才能生效。)`
.. |const| replace:: :abbr:`const (本方法没有副作用。不会修改该实例的任何成员变量。)`
.. |vararg| replace:: :abbr:`vararg (本方法除了在此处描述的参数外，还能够继续接受任意数量的参数。)`
.. |constructor| replace:: :abbr:`constructor (本方法用于构造某个类型。)`
.. |static| replace:: :abbr:`static (调用本方法无需实例，所以可以直接使用类名调用。)`
.. |operator| replace:: :abbr:`operator (本方法描述的是使用本类型作为左操作数的有效操作符。)`
.. |bitfield| replace:: :abbr:`BitField (这个值是由下列标志构成的位掩码整数。)`
