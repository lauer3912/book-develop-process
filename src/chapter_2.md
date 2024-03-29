# 软件测试理论

引文参照 [Software Testing on Wikipedia](https://en.wikipedia.org/wiki/Software_testing)

## 1. 软件测试分类

### 1.1. Testing levels(测试级别)

#### 1.1.1. Unit testing(单元测试)

[https://en.wikipedia.org/wiki/Unit_testing](https://en.wikipedia.org/wiki/Unit_testing)

> Unit testing refers to tests that verify the functionality of a specific section of code, usually at the function level. In an object-oriented environment, this is usually at the class level, and the minimal unit tests include the constructors and destructors.
>
> These types of tests are usually written by developers as they work on code (white-box style), to ensure that the specific function is working as expected. One function might have multiple tests, to catch corner cases or other branches in the code. Unit testing alone cannot verify the functionality of a piece of software, but rather is used to ensure that the building blocks of the software work independently from each other.
>
> Unit testing is a software development process that involves a synchronized application of a broad spectrum of defect prevention and detection strategies in order to reduce software development risks, time, and costs. It is performed by the software developer or engineer during the construction phase of the software development life cycle. Unit testing aims to eliminate construction errors before code is promoted to additional testing; this strategy is intended to increase the quality of the resulting software as well as the efficiency of the overall development process.
>
> Depending on the organization's expectations for software development, unit testing might include static code analysis, data-flow analysis, metrics analysis, peer code reviews, code coverage analysis and other software testing practices.

> 单元测试是对软件组成单元进行测试。其目的是检验软件基本组成单位的正确性。测试的对象是软件设计的最小单位：模块，所以又称为模块测试。

* 测试阶段：编码后
* 测试对象：最小模块
* 测试人员：白盒测试工程师或开发工程师
* 测试依据：代码和注释+详细设计文档
* 测试方法：白盒测试
* 测试内容：模块接口测试、局部数据结构测试、路径测试、错误处理测试、边界测试
* 测试扩展内容：静态代码分析、数据流分析、度量分析、结对代码审查、代码覆盖度分析

#### 1.1.2. Integration testing(集成测试)

[https://en.wikipedia.org/wiki/Integration_testing](https://en.wikipedia.org/wiki/Integration_testing)

> 集成测试也称`联合测试`、`组装测试`，将程序模块采用适当的集成策略组装起来，对系统的接口及集成后的功能进行正确性检测的测试工作。主要目的是检查软件单位之间的接口是否正确。

* 测试阶段：一般单元测试之后进行
* 测试对象：模块间的接口
* 测试人员：白盒测试工程师或开发工程师
* 测试依据：单元测试的模块+概要设计文档
* 测试方法：黑盒测试与白盒测试相结合
* 测试内容：模块之间数据传输、模块之间功能冲突、模块组装功能正确性、全局数据结构、单模块缺陷对系统的影响

#### 1.1.3. System testing(系统测试)

[https://en.wikipedia.org/wiki/System_testing](https://en.wikipedia.org/wiki/System_testing)

> 将软件系统看成是一个系统的测试。包括对功能、性能以及软件所运行的软硬件环境进行测试。时间大部分在系统测试执行阶段。

* 测试阶段：集成测试通过之后
* 测试对象：整个系统（软、硬件）
* 测试人员：黑盒测试工程师
* 测试依据：需求规格说明文档
* 测试方法：黑盒测试
* 测试内容：功能、界面、可靠性、易用性、性能、兼容性、安全性等

#### 1.1.4. Acceptance testing(验收测试)

[https://en.wikipedia.org/wiki/Acceptance_testing](https://en.wikipedia.org/wiki/Acceptance_testing)

> 验收测试是部署软件之前的最后一个测试操作。它是技术测试的最后一个阶段，也称为`交付测试`。验收测试的目的是确保软件准备就绪，按照项目合同、任务书、双方约定的验收依据文档，向软件购买都展示该软件系统满足原始需求。

* 测试阶段：系统测试通过之后
* 测试对象：整个系统（包括软硬件）
* 测试人员：主要是最终用户或者需求方
* 测试依据：用户需求、验收标准
* 测试方法：黑盒测试
* 测试内容：同系统测试(功能...各类文档等)

### 1.2. Testing approach(测试方法)

#### 1.2.1. Static, dynamic, and passive testing(静态、动态、被动)

#### 1.2.2. Exploratory approach(探索测试)

#### 1.2.3. The "box" approach(盒子测试)

##### 1.2.3.1. White-box testing(白盒子测试)

[https://en.wikipedia.org/wiki/White-box_testing](https://en.wikipedia.org/wiki/White-box_testing)

> 白盒测试又称结构测试、透明盒测试、逻辑驱动测试或基于代码的测试。白盒指的打开盒子，去研究里面的源代码和程序结果。

一般包括：

* [API testing(接口测试)](https://en.wikipedia.org/wiki/API_testing)
* [Code coverage(代码覆盖度)](https://en.wikipedia.org/wiki/Code_coverage)
* [Fault injection(故障注入)](https://en.wikipedia.org/wiki/Fault_injection)
* [Mutation testing(突变测试)](https://en.wikipedia.org/wiki/Mutation_testing)
* [Static testing(静态测试)](https://en.wikipedia.org/wiki/Static_testing)
  
##### 1.2.3.2. Black-box testing(黑盒子测试)

[https://en.wikipedia.org/wiki/Black-box_testing](https://en.wikipedia.org/wiki/Black-box_testing)

> 黑盒测试也称功能测试，测试中把被测的软件当成一个黑盒子，不关心盒子的内部结构是什么，只关心软件的输入数据与输出数据。

一般包括：

* Component interface testing(组件接口测试)
* Visual testing(可视化测试)
  * Graphical user interface testing(图形化用户交互测试)

##### 1.2.3.3. Grey-box testing(灰盒子测试)

[https://en.wikipedia.org/wiki/Gray_box_testing](https://en.wikipedia.org/wiki/Gray_box_testing)

> 灰盒测试，是介于白盒测试与黑盒测试之间的一种测试，灰盒测试多用于集成测试阶段，不仅关注输出、输入的正确性，同时也关注程序内部的情况。

### 1.3. Testing types(测试类型)

#### 1.3.1. Installation testing(安装测试)

[https://en.wikipedia.org/wiki/Installation_testing](https://en.wikipedia.org/wiki/Installation_testing)

#### 1.3.2. Compatibility testing(兼容性测试)

[https://en.wikipedia.org/wiki/Compatibility_testing](https://en.wikipedia.org/wiki/Compatibility_testing)

#### 1.3.3. Smoke and sanity testing(冒烟测试)

* [https://en.wikipedia.org/wiki/Smoke_testing_(software)](https://en.wikipedia.org/wiki/Smoke_testing_(software))
* [https://en.wikipedia.org/wiki/Sanity_testing](https://en.wikipedia.org/wiki/Sanity_testing)

> 冒烟测试目的是确认软件基本功能正常，冒烟测试的执行者是版本编译人员/开发人员。

> 在《微软项目求生法则》一书第14章“构建过程”关于冒烟测试，就是开发人员在个人版本的软件上执行目前的冒烟测试项目，确定新的程序代码不出故障

> 现基本执行对象为测试人员，在正规测试一个新版本之前，投入较少的人力和时间验证基本功能，通过则测试准入。

#### 1.3.4. Regression testing(回归测试)

> 回归测试是指修改了旧代码后，重新进行测试以确认修改没有引入新的错误或导致其他代码产生错误。自动回归测试将大幅降低系统测试、维护升级等阶段的成本。

> 在整个软件测试过程中占有很大的工作量比重，软件开发的各个阶段都会进行多次回归测试。通过选择正确的回归测试策略来改进回归测试的效率和有效性是很有意义的。

#### 1.3.5. Acceptance testing(验收测试)

[https://en.wikipedia.org/wiki/Acceptance_testing](https://en.wikipedia.org/wiki/Acceptance_testing)

#### 1.3.6. Alpha testing(α测试)

> α测试是由一个用户在开发环境下进行的测试，也可以是公司内部的用户在模拟实际操作环境下进行的测试。α测试的目的是评价软件产品的FLURPS(即功能、局域化、可使用性、可靠性、性能和支持)。

大型通用软件，在正式发布前，通常需要执行α测试和β测试。α测试不能由程序员或测试员完成。

#### 1.3.7. Beta testing(β测试)

> β测试是一种验收测试。β测试由软件的最终用户们在一个或多个客房场所进行。

α测试与β测试的区别：

测试的场所不同：α测试是指把用户请到开发方的场所来测试,β测试是指在一个或多个用户的场所进行的测试。

α测试的环境是受开发方控制的,用户的数量相对比较少,时间比较集中。β测试的环境是不受开发方控制的,用户数量相对比较多,时间不集中。

α测试先于beta测试执行。通用的软件产品需要较大规模的β测试,测试周期比较长。

#### 1.3.8. Functional vs non-functional testing(功能及非功能测试)

* [https://en.wikipedia.org/wiki/Functional_testing](https://en.wikipedia.org/wiki/Functional_testing)
* [https://en.wikipedia.org/wiki/Non-functional_testing](https://en.wikipedia.org/wiki/Non-functional_testing)

> 功能测试是指验证代码的特定操作或功能的活动。 这些通常在代码要求文档中找到，尽管某些开发方法从用例或用户故事中工作。 功能测试倾向于回答“用户可以做到这一点”或“这个特定的功能工作。”的问题。

> 非功能测试是指软件的方面可能与特定函数或用户动作（例如可伸缩性或其他性能），在某些约束或安全性下的缩放性或其他性能。 测试将确定断裂点，可扩展性或性能极低的点导致不稳定执行。 非功能性要求往往是反映产品质量的那些，特别是在其用户的适用性视角的背景下。

#### 1.3.9. API testing(接口测试)

[https://en.wikipedia.org/wiki/API_testing](https://en.wikipedia.org/wiki/API_testing)

#### 1.3.10. Continuous testing(持续测试)

[https://en.wikipedia.org/wiki/Continuous_testing](https://en.wikipedia.org/wiki/Continuous_testing)

> 持续测试是作为软件交付管道的一部分执行自动测试的过程，以获得关于与软件发布候选人相关的业务风险的直接反馈。持续测试测试包括验证功能要求和非功能性要求; 测试范围扩展了验证自下而上要求或用户故事，以评估与总体业务目标相关的系统要求。

#### 1.3.11. Destructive testing(破坏性测试)

[https://en.wikipedia.org/wiki/Destructive_testing](https://en.wikipedia.org/wiki/Destructive_testing)

> 破坏性测试尝试导致软件或子系统失败。 即使在收到无效或意外输入的情况下，它验证软件是否正常运行，从而建立输入验证和错误管理例程的稳健性。软件故障注入，以模糊的形式是故障测试的一个例子。 各种商业非功能性测试工具与软件故障注入页面相关联; 还有许多开源和可用的免费软件工具，可提供破坏性测试。

一般测试内容包括：

  * [Exception handling(异常处理)](https://en.wikipedia.org/wiki/Exception_handling)
  * [Recovery testing(恢复测试)](https://en.wikipedia.org/wiki/Recovery_testing)

#### 1.3.12. Software performance testing(软件性能测试)

[https://en.wikipedia.org/wiki/Software_performance_testing](https://en.wikipedia.org/wiki/Software_performance_testing)

> 通常执行性能测试以确定系统或子系统如何在特定工作负载下的响应性和稳定性方面执行。 它还可以用于调查，测量，验证或验证系统的其他质量属性，例如可伸缩性，可靠性和资源使用情况。

> 负载测试主要关注测试系统可以在特定负载下继续运行，无论是大量数据还是大量用户。 这通常被称为软件可伸缩性。 当非功能性活动的相关负载测试活动通常被称为耐久性测试。 卷测试是一种测试软件功能的方法，即使某些组件（例如文件或数据库）大小而增加。 压力测试是在意外或罕见工作负载下测试可靠性的一种方式。 稳定性测试（通常称为负载或耐久性测试）检查，看看软件是否可以在可接受的时间内或高于可接受的时段中持续运行。

> 关于性能测试的具体目标几乎没有一致。 术语负载测试，性能测试，可扩展性测试和音量测试通常常用。

> 实时软件系统具有严格的计时约束。 要测试是否满足时序约束，则使用实时测试。

#### 1.3.13. Usability testing(易用性测试)

[https://en.wikipedia.org/wiki/Usability_testing](https://en.wikipedia.org/wiki/Usability_testing)

> 可用性测试是检查用户界面是否易于使用和理解。 它主要涉及应用程序的使用。 这不是一种可以自动化的测试; 需要实际的用户，由熟练的UI设计人员监控。

#### 1.3.14. Accessibility testing(可访问性测试)

[https://en.wikipedia.org/wiki/Accessibility](https://en.wikipedia.org/wiki/Accessibility)

可访问性测试可能包括符合标准，例如：

* [Americans with Disabilities Act of 1990](https://en.wikipedia.org/wiki/Americans_with_Disabilities_Act_of_1990)
* [Section 508 Amendment to the Rehabilitation Act of 1973](https://en.wikipedia.org/wiki/Section_508_Amendment_to_the_Rehabilitation_Act_of_1973)
* [Web Accessibility Initiative (WAI)](https://en.wikipedia.org/wiki/Web_Accessibility_Initiative) of the [World Wide Web Consortium (W3C)](https://en.wikipedia.org/wiki/World_Wide_Web_Consortium)

#### 1.3.15. Security testing(安全测试)

[https://en.wikipedia.org/wiki/Security_testing](https://en.wikipedia.org/wiki/Security_testing)

> 安全测试对于处理机密数据的软件至关重要，以防止黑客系统入侵。

#### 1.3.16. Internationalization and localization(国际化和本地化测试)

> 用于国际化和本地化的测试验证了该软件可以与不同的语言和地理区域一起使用。 [Pseudolocalization](https://en.wikipedia.org/wiki/Pseudolocalization)的过程用于测试应用程序将应用程序转换为另一种语言的能力，并更容易识别当本地化过程可能将新错误引入产品。

> 全球化测试验证软件适用于新的文化（如不同的货币或时区）。

> 一般需要测试的情况：
>  * 软件通常是通过转换上下文的字符串列表，而翻译器可能为模糊源字符串选择了错误的转换。
>  * 如果项目由几个人翻译，则在没有适当的协调的情况下或转换员不谨慎的话，技术术语可能会变得不一致。
>  * 文字词语翻译可能听起来不当，人为或过于技术的目标语言。
>  * 原始语言中的未转换消息可能在源代码中硬编码。
>  * 可以在运行时自动创建某些消息，并且生成的字符串可以是不正确的，功能不正确，误导或混淆。
>  * 软件使用源语言键盘布局没有函数的键盘快捷键，用于了在目标语言的布局中键入字符。
>  * 软件可能缺乏对目标语言的字符编码的支持。
>  * 在源语言中适用的字体和字体大小可能在目标语言中不合适; 例如，如果字体太小，CJK字符可能会变得不可读。
>  * 目标语言中的字符串可能比软件可以句柄长。 这可能会使字符串对用户部分不可见，或使软件崩溃或故障。
>  * 软件可能缺乏对读取或写作双向文本的适当支持。
>  * 软件可能会显示未本地化的文本的图像。
>  * 本地化操作系统可能具有不同命名的系统配置文件和环境变量以及日期和货币的不同格式。

#### 1.3.17. Development testing(开发测试)

[https://en.wikipedia.org/wiki/Development_testing](https://en.wikipedia.org/wiki/Development_testing)

> 开发测试是一种软件开发过程，涉及广泛的缺陷预防和检测策略的同步应用，以减少软件开发风险，时间和成本。 它由软件开发人员或工程师在软件开发生命周期的施工阶段进行。 开发测试旨在消除代码促进到其他测试之前的施工错误; 该策略旨在提高所得软件的质量以及整体开发过程的效率。

> 根据组织对软件开发的期望，开发测试可能包括静态代码分析，数据流分析，指标分析，对等代码评价，单元测试，代码覆盖分析，可追溯性和其他软件测试实践。

#### 1.3.18. A/B testing(A/B测试)

[https://en.wikipedia.org/wiki/A/B_testing](https://en.wikipedia.org/wiki/A/B_testing)

> A/B测试是运行受控实验的方法，以确定提出的变化是否比当前方法更有效。 客户被路由到特征的当前版本（控制），或者收集到修改的版本（处理），并收集数据以确定哪个版本更好地实现所需结果。

#### 1.3.19. Concurrent testing(并发测试)

[https://en.wikipedia.org/wiki/Concurrent_testing](https://en.wikipedia.org/wiki/Concurrent_testing)

> 并发测试评估使用并发计算的软件和系统的行为和性能，通常在正常使用条件下。

> 典型问题这种类型的测试将暴露是死锁，种族条件和共享内存/资源处理的问题。

#### 1.3.20. Conformance testing or type testing(一致性和类型测试)

[https://en.wikipedia.org/wiki/Conformance_testing](https://en.wikipedia.org/wiki/Conformance_testing)

> 在软件测试中，一致性测试验证了产品根据其指定标准执行。 例如，编译器被广泛测试以确定它们是否符合该语言的公认标准。

#### 1.3.21. Output comparison testing(输出比较测试/快照测试)

> 创建显示预期输出，无论是UI的文本或屏幕截图的数据比较，有时被称为快照测试，不同于许多其他形式的测试，这不能自动检测失败，而是要求测试人员评估输出不一致。

#### 1.3.22. Property testing(属性测试)

> Property testing is a testing technique where, instead of asserting that specific inputs produce specific expected outputs, the practitioner randomly generates many inputs, runs the program on all of them, and asserts the truth of some "property" that should be true for every pair of input and output. For example, every input to a sort function should have the same length as its output. Every output from a sort function should be a monotonically increasing list.
> Property testing libraries allow the user to control the strategy by which random inputs are constructed, to ensure coverage of degenerate cases, or inputs featuring specific patterns that are needed to fully exercise aspects of the implementation under test.
> Property testing is also sometimes known as "generative testing" or "QuickCheck testing" since it was introduced and popularized by the Haskell library "[QuickCheck](https://hackage.haskell.org/package/QuickCheck)."

> 基于属性的测试技术（ Property-based testing），是指编写对你的代码来说为真的逻辑语句（即“属性”），然后使用自动化工具来生成测试输入（一般来说，是指某种特定类型的随机生成输入数据），并观察程序接受该输入时属性是否保持不变。 如果某个输入违反了某一条属性，则用户证明程序存在一处错误，并找到一个能够演示该错误的便捷示例。 基于属性的测试技术的一个经典示例是测试一个sort（排序）函数，具体代码如下所示。 这个测试过程假定，给定一列整数，对其进行排序 - 保持元素的集合不变 - 生成一个有序输出 随后，测试框架将针对一些输入序列的集合自动化执行上述代码，并报告是否发现反例。

#### 1.3.23. VCR testing(记录重放测试/播放测试)

> VCR testing, also known as "playback testing" or "record/replay" testing, is a testing technique for increasing the reliability and speed of regression tests that involve a component that is slow or unreliable to communicate with, often a third-party API outside of the tester's control. It involves making a recording ("cassette") of the system's interactions with the external component, and then replaying the recorded interactions as a substitute for communicating with the external system on subsequent runs of the test.

VCR测试，也称为“播放测试”或“记录/重放”测试，是提高回归测试的可靠性和速度的测试技术，涉及与之通信的组件，通常是第三方API的速度慢或不可靠 在测试人员的控制之外。 它涉及制作系统与外部组件的交互的录制（“盒式”），然后将记录的交互重播为与外部系统在后续运行中与外部系统进行通信的替代。

#### 1.3.24. Ad-hoc Testing(随机测试)

> 随机测试主要是根据测试者的经验对软件进行功能和性能抽查。
>
> 根据测试说明书执行用例测试的重要补充手段，是保证测试覆盖完整性的有效方式和过程。
>
> 随机测试主要是对被测软件的一些重要功能进行复测，也包括测试那些当前的测试用例(TestCase)没有覆盖到的部分。

#### 1.3.25. Exploratory testing(探索性测试)

> 探索性测试可以说是一种测试思维技术。它没有很多实际的测试方法、技术和工具，但是却是所有测试人员都应该掌握的一种测试思维方式。探索性强调测试人员的主观能动性，抛弃繁杂的测试计划和测试用例设计过程，强调在碰到问题时及时改变测试策略。

## 2. 软件测试分类边界划分

### 2.1. 按开发阶段划分

* 单元测试(Unit Testing)
* 集成测试(Integration Testing)
* 系统测试(System Testing)
* 验收测试(Acceptance Testing)

### 2.2. 按是否运行划分

* 静态测试(Static Testing)
* 动态测试(Dynamic Testing)

### 2.3. 按是否查看代码划分

* 白盒测试(White-box Testing)
* 黑盒测试(Black-box Testing)
* 灰盒测试(Gray-box Testing)

### 2.4. 按是否手工操作执行

* Manual Testing(手工测试)
  > 手工测试就是由人去一个一个的输入用例，然后观察结果，和机器测试相对应，属于比较原始但是必须的一个步骤。
  > 优点：自动化无法替代探索性测试、发散思维类无既定结果的测试
  > 缺点：执行效率慢，量大易错。
* Automation Testing(自动化测试)
  > 就是在预设条件下运行系统或应用程序，评估运行结果，预先条件应包括正常条件和异常条件。简单说自动化测试是把以人为驱动的测试行为转化为机器执行的一种过程。
  > 自动化测试比如功能测试自动化、性能测试自动化、安全测试自动化。
  > 通常所说的自动化是指功能测试自动化
  > AI技术的兴起发展，类似可预见工作都有可能会被伪AI代替.

### 2.5. 其他

* 随机测试(Ad-hoc Testing)
* 冒烟测试(Smoke Testing)
* 安全测试(Security Testing)
* 探索性测试(Exploratory Testing)
* 回归测试(Regression Testing)
* α测试(Alpha Testing)
* β测试(Beta Testing)
* ...

## 3. 软件测试流程

### 3.1. 传统的瀑布开发模式下的测试

瀑布开发中的一个常见实践是测试是由一组独立的测试人员执行的。

* [能力成熟度模型集成](https://en.wikipedia.org/wiki/Capability_Maturity_Model_Integration)
* [瀑布开发模式](https://en.wikipedia.org/wiki/Waterfall_model)

### 3.2. 敏捷/极限开发模式下的测试

相反，一些新兴的软件学科，如[极限编程](https://en.wikipedia.org/wiki/Extreme_programming)和[敏捷软件](https://en.wikipedia.org/wiki/Agile_software_development)开发运动，坚持“[测试驱动的软件开发](https://en.wikipedia.org/wiki/Test-driven_development)”模型。

在这个过程中，软件工程师首先编写单元测试(通常使用极端编程方法中的结对编程)。预计测试最初会失败。每次失败的测试之后都编写足够的代码使其通过。

这意味着当发现新的故障条件和角落用例时，测试套件会不断更新，并且与开发的任何回归测试集成。单元测试与软件源代码的其余部分一起维护，通常集成到构建过程中(固有的交互性测试被归入部分手工的构建验收过程)。

这个测试过程的最终目标是支持[持续集成](https://en.wikipedia.org/wiki/Continuous_integration)和减少缺陷率。

这种方法增加了开发完成的测试工作，在到达任何正式的测试团队之前。在其他一些开发模型中，大多数测试执行发生在定义了需求并完成了编码过程之后。

### 3.3. 测试的生命周期

一般测试的生命周期，包括：

* 需求分析：测试应在软件开发生命周期的需求阶段开始。 在设计阶段，测试人员可以确定设计的哪些方面是可测试的，并且需要哪些参数。
* 测试计划: 测试策略，测试计划，测试台创建。由于在测试期间将执行许多活动，因此需要一个计划。
* 测试开发: 测试过程，测试场景，测试用例，测试数据集，测试脚本。
* 测试执行: 测试人员根据计划和测试文档执行软件，然后报告开发团队中的任何错误。 在缺乏编程知识的运行测试时，此部分可能是复杂的。
* 输出测试报告: 一旦测试完成，测试人员生成量度，并对他们的测试工作以及被测试的软件是否准备好发布做出最终报告。
* 测试结果分析: 或者缺陷分析，通常是由开发团队和客户一起完成的，为了决定哪些缺陷应该被分配、修复、拒绝(即发现的软件正常工作)或者推迟到以后处理。
* 缺陷重新测试: 一旦开发团队处理了一个缺陷，测试团队就会重新测试它。
* 回归测试: 为了确保最新的交付没有破坏任何东西，并且软件产品作为一个整体仍然正确地工作，一个由测试子集构建的小测试程序是很常见的。
* 测试结束: 一旦测试符合退出标准，捕获关键输出，经验教训，结果，日志，与项目相关的文档等活动将被归档，并将其作为未来项目的参考。

## 4. 软件测试组成部分

### 4.1. Test plan(测试计划)

> 测试计划是一份详细说明将用于预期测试活动的方法的文档。计划可以包括目标、范围、过程和程序、人员要求和应急计划等方面测试计划可能是一个计划,包括所有形式的测试类型(如接受或系统测试计划)和规划考虑,或者它可能是发行主测试计划,概述了一个以上的详细测试计划(计划)的计划。在某些情况下，测试计划可以是广泛的“测试策略”的一部分，它记录了整个测试策略

### 4.2. Traceability matrix(追溯矩阵)

> 追溯矩阵是将需求或设计文档与测试文档关联起来的表格。它用于在相关源文档被更改时更改测试，在计划回归测试时通过考虑需求覆盖率来选择测试用例以执行。

### 4.3. Test case(测试用例)

> 测试用例通常由唯一的标识符组成，从设计规范，前提条件，事件，一系列步骤（也称为动作）来组成，以遵循，输入，输出，预期结果和实际结果。 临床定义，测试用例是输入和预期结果。这可以像“条件x的条件x一样”，尽管通常测试案例更详细地描述了输入方案以及可能预期的结果。 它偶尔可以是一系列步骤（但通常阶梯通常包含在单独的测试程序中，该测试程序可以根据经济问题而无法对多个测试用例进行），但具有一个预期的结果或预期结果。 可选字段是测试用例ID，测试步骤或执行编号，相关要求，深度，测试类别，作者以及复选框，以及是否自动化。 较大的测试用例也可能包含先决条件状态或步骤和描述。 测试案例还应包含实际结果的地方。 这些步骤可以存储在字处理器文档，电子表格，数据库或其他常见存储库中。 在数据库系统中，您还可以看到生成结果的过去的测试结果以及系统配置用于生成这些结果的测试结果。 这些过去的结果通常将存储在单独的表中。

### 4.4. Test script(测试脚本)

> 测试脚本是复制用户操作的过程或编程代码。最初，这个术语来源于自动回归测试工具创建的工作产品。测试用例将是使用工具或程序创建测试脚本的基线。

### 4.5. Test suite(测试套件)

> 测试用例的集合最常见的术语是测试套件。测试套件通常还包含每个测试用例集合的更详细的说明或目标。它肯定包含测试人员识别测试期间使用的系统配置的部分。一组测试用例也可能包含先决条件状态或步骤，以及对以下测试内容的描述。

### 4.6. Test fixture(测试夹具)/data

> 在大多数情况下，使用多个值或数据集来测试特定特性的相同功能。所有的测试值和变化的环境成分收集在单独的文件中，并作为测试数据存储。为客户端和产品或项目提供这些数据也很有用。有一些技术可以生成测试数据。

### 4.7. Test harness(测试工具)

> 软件、工具、数据输入和输出的样本，以及配置都被统称为测试工具。

### 4.8. Test run(测试运行/测试运行器)

> 运行测试用例或测试套件的结果报告

## 5. 软件测试质量度量

[https://en.wikipedia.org/wiki/Software_quality](https://en.wikipedia.org/wiki/Software_quality)

> 质量措施包括正确，完整性，安全性和ISO / IEC 9126要求等主题，例如能力，可靠性，效率，可移植性，可维护性，兼容性和可用性等要求。

有许多常用的软件指标或措施，用于帮助确定软件的状态或测试的充分性。
