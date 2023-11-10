# ProjectDescriptionDocument


OS Hybrid Intent Bus: 应用场景类似于为跨端（PC、Ipad）应用程序框架，Intent Bus 为跨端应用程序框架提供了数据信息、视觉的交互服务。

Intent: 在操作系统中，"Intent" 是一个重要的概念，是一种用于指示要执行的操作和传递数据的机制，可以用来启动服务、调用服务、发送/接收广播等。以及用于不同运行时环境的服务间传递数据。

原子服务：淡化软件概念，将每一个软件的服务拆分成一个一个最小粒度的原子服务。

OS Hybrid Intent Bus 是一个通信架构，其核心概念是意图（Intent）。意图代表了用户或程序在执行操作时的目的或意图。它是高度抽象的，用于描述用户希实现的特定任务、操作或功能。在操作系统中，意图充当了执行者的角色，类似于经过自然语言处理（NLP）的指令，以满足用户的特定需求。它是连接操作系统内部各个组件的纽带，具备命令、API、通用链接、数据通信、数据共享和事件回调等多种功能。
在架构中，意图不仅是一种命令，也是一种通向智能化处理的最终通道。它粘接了视觉连接性与数据连接性的两个方面，在N层原子服务中扮演了重要的角色。视觉连接性代表了应用之间的模态关系，而数据连接性代表了情境关系。而意图，作为这两者的粘接剂，负责将用户需求、数据和操作有机地结合在一起。
带来了的好处：

自然交互: 这种方式使用户与操作系统之间的交互更加自然，类似于人与人之间的对话，用户可以以更直观的方式表达其需求。
智能响应: 意图使操作系统能够更好地理解用户的意图和需求，从而更智能地提供服务和响应。它可以根据用户的意图自动选择最合适的操作和资源。
简化操作: 意图使用户能够更直接地表达其所需操作，从而减少了冗长的操作步骤。用户可以通过简单的意图触发复杂的操作。
个性化服务: 通过捕捉用户的个性和偏好，意图允许系统提供更加个性化的服务和建议，满足不同用户的不同需求。

通过意图作用域的精确调节，Hybrid Intent Bus 可以实现即时响应用户的需求。这确定了一个原子服务内意图可以影响和操作的范围，以及在该范围内意图可以执行的操作和访问的资源。通过改变原子服务的意图作用域，可以动态调整原子服务的颗粒度，实现灵活性和性能的最佳平衡。这还包括上下文界定、资源管理、异常处理和个性化体验等支持，以优化原子服务之间的数据与视觉连接关系。
Hybrid Intent Bus 将作为操作系统通信的中心枢纽，使得跨不同应用、不同运行时和不同设备的通信变得更加自然和高效。

Hybrid Intent Bus ： 为操作系统中用于连接不同的运行时环境，实现在不同的运行时环境及运行于不同运行时环境下的服务之间分发和传递 intent 的混合意图总线。它充当了各运行时环境下的 Intent Bus 的调度中心，管理了意图的传递和调用。各运行时环境下的 Intent Bus 通过 Bus Bridge 与 Hybrid Intent Bus 进行连接。

Bus Bridge ： Hybrid Intent Bus 通过 Bus Bridge 与各个运行时环境下的 Intent Bus 连接，这些 Bus Bridge 充当了翻译器的角色，确保不同运行时环境的意图可以互通。

Web Intent Bus（Web Runtime） ： 是专门为 Web 运行时环境设计的意图总线，它用于管理和分发 Web 应用及服务之间的意图通信。在基于原子服务运行时规范的 DingOS 的新 Web Runtime 中，意图是原子服务及其组件间的基本通信方式。code>Web Intent Bus 将为以意图驱动的原子服务框架提供直接的能力支撑。

Native Intent Bus(Native Runtime) ： 为 Native 运行时环境下的意图总线，用于实现 Native 应用及服务之间 intent 通信的管理及分发传递。需要注意的是 Native 运行时环境为 DingOS 的基础运行环境，所以 Native Intent Bus 可只在逻辑上与 Hybrid Intent Bus 分离，物理上可不做分离。

Other VM Intent Bus(Other Runtime) ： 为其他 VM (如 Android 虚拟机等) 运行时环境下的意图总线，用于实现运行于特定 VM 运行时环境中应用及服务之间 intent 通信的管理及分发传递。现阶段 操作系统 混合意图总线系统的设计暂不涉及该总线的设计，但在未来可能会引入，以支持更广泛的虚拟机环境

Intent Register 为 Hybrid Intent Bus 的注册器，负责意图申明信息的注册及数据管理。

Intent Router 为 Hybrid Intent Bus 的路由器，负责意图的分发、执行与调度控制。

Bus Bridge 为 Hybrid Intent Bus 链接下一层意图总线的桥接器，允许 Hybrid Intent Bus 扩展到更多的平台或设备，实现跨设备协同能力。

DSD： 一种新型描述语言，格式为json, 类似于 manifest, 通过 web应用/Navtive 信息生成，可通过手动生成/自动生成两种组合方式， 用于 web应用/Native之间一对一、多对多之间的通信使用。 内容含web应用/Native应用的各种信息，例如外观描述，通信条件描述，自身信息等等。

组合服务：服务可以通过拼接组合成一个应用程序服务。
