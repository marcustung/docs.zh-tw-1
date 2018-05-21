---
title: 'F # 樣式指南'
description: '了解五個很好的 F # 程式碼的原則。'
ms.date: 05/14/2018
ms.openlocfilehash: 6d8c1336ca991040a8f6e13290d209cb3b70054d
ms.sourcegitcommit: 22c3c8f74eaa138dbbbb02eb7d720fce87fc30a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/17/2018
---
# <a name="f-style-guide"></a><span data-ttu-id="ab538-103">F # 樣式指南</span><span class="sxs-lookup"><span data-stu-id="ab538-103">F# style guide</span></span>

<span data-ttu-id="ab538-104">下列文章描述格式化 F # 程式碼的語言功能的主題是指導和它們的使用方式的指導方針。</span><span class="sxs-lookup"><span data-stu-id="ab538-104">The following articles describe guidelines for formatting F# code and topical guidance for features of the language and how they should be used.</span></span>

<span data-ttu-id="ab538-105">本指南已成形，根據 F # 中的使用大型程式碼基底與不同的程式設計人員群組。</span><span class="sxs-lookup"><span data-stu-id="ab538-105">This guidance has been formulated based on the use of F# in large codebases with a diverse group of programmers.</span></span> <span data-ttu-id="ab538-106">本指南通常會導致成功使用 F # 的而且程式的需求會隨時間變更時，最小化麻煩。</span><span class="sxs-lookup"><span data-stu-id="ab538-106">This guidance generally leads to successful use of F# and minimizes frustrations when requirements for programs change over time.</span></span>

## <a name="five-principles-of-good-f-code"></a><span data-ttu-id="ab538-107">五個很好的 F # 程式碼原則</span><span class="sxs-lookup"><span data-stu-id="ab538-107">Five principles of good F# code</span></span>

<span data-ttu-id="ab538-108">您應該記住下列原則您撰寫 F # 程式碼，尤其是在系統將會隨著時間變更的任何時間。</span><span class="sxs-lookup"><span data-stu-id="ab538-108">You should keep the following principles in mind any time you write F# code, especially in systems that will change over time.</span></span> <span data-ttu-id="ab538-109">指南進一步文件中的每個片段都源自於這些五個點。</span><span class="sxs-lookup"><span data-stu-id="ab538-109">Every piece of guidance in further articles stems from these five points.</span></span>

1. <span data-ttu-id="ab538-110">**簡潔且具表達性，是很好的 F # 程式碼**</span><span class="sxs-lookup"><span data-stu-id="ab538-110">**Good F# code is succinct and expressive**</span></span>

    <span data-ttu-id="ab538-111">F # 具有許多功能，讓您表示較少的程式碼行中的動作，並重複使用的一般功能。</span><span class="sxs-lookup"><span data-stu-id="ab538-111">F# has many features that allow you to express actions in fewer lines of code and reuse generic functionality.</span></span> <span data-ttu-id="ab538-112">F # 核心程式庫也包含許多有用的型別和使用通用的資料集合的功能。</span><span class="sxs-lookup"><span data-stu-id="ab538-112">The F# core library also contains many useful types and functions for working with common collections of data.</span></span> <span data-ttu-id="ab538-113">一般而言，如果你可以解決問題，以較少的行程式碼，其他開發人員 （或您未來自助） 將感激。</span><span class="sxs-lookup"><span data-stu-id="ab538-113">As a general rule, if you can express a solution to a problem in fewer lines of code, other developers (or your future self) will be appreciative.</span></span> <span data-ttu-id="ab538-114">也強烈建議您使用的程式庫，例如 FSharp.Core， [vast 的.NET 程式庫](https://docs.microsoft.com/dotnet/api/)F # 執行，或第三方封裝上的[NuGet](https://www.nuget.org/)當您需要執行重要的工作。</span><span class="sxs-lookup"><span data-stu-id="ab538-114">It is also highly recommended that you use a library such as FSharp.Core, the [vast .NET libraries](https://docs.microsoft.com/dotnet/api/) that F# runs on, or a third-party package on [NuGet](https://www.nuget.org/) when you need to do a nontrivial task.</span></span>

2. <span data-ttu-id="ab538-115">**良好的 F # 程式碼具有互通性**</span><span class="sxs-lookup"><span data-stu-id="ab538-115">**Good F# code is interoperable**</span></span>

    <span data-ttu-id="ab538-116">互通性可以有多個形式，包括使用不同語言的程式碼。</span><span class="sxs-lookup"><span data-stu-id="ab538-116">Interoperation can take multiple forms, including consuming code in different languages.</span></span> <span data-ttu-id="ab538-117">與交互操作的其他呼叫端程式碼的界限是正確的重要片段。</span><span class="sxs-lookup"><span data-stu-id="ab538-117">The boundaries of your code that other callers interoperate with are critical pieces to get right.</span></span> <span data-ttu-id="ab538-118">在撰寫 F #，您應該一律想成有關如何其他程式碼會呼叫您要撰寫，包括若從另一個語言，例如 C# 程式碼。</span><span class="sxs-lookup"><span data-stu-id="ab538-118">When writing F#, you should always be thinking about how other code will call into the code you are writing, including if they do so from another language like C#.</span></span> <span data-ttu-id="ab538-119">[F # 元件的設計指導方針](component-design-guidelines.md)說明詳細的互通性。</span><span class="sxs-lookup"><span data-stu-id="ab538-119">The [F# Component Design Guidelines](component-design-guidelines.md) describe interoperability in detail.</span></span>

3. <span data-ttu-id="ab538-120">**良好 F # 程式碼會使用程式設計物件，不是物件的方向**</span><span class="sxs-lookup"><span data-stu-id="ab538-120">**Good F# code makes use of object programming, not object orientation**</span></span>

    <span data-ttu-id="ab538-121">F # 的程式設計物件的完整支援已在.NET 中，包括[類別](../language-reference/classes.md)，[介面](../language-reference/interfaces.md)，[存取修飾詞](../language-reference/access-control.md)，[抽象類別](../language-reference/abstract-classes.md)，依此類推。</span><span class="sxs-lookup"><span data-stu-id="ab538-121">F# has full support for programming with objects in .NET, including [classes](../language-reference/classes.md), [interfaces](../language-reference/interfaces.md), [access modifiers](../language-reference/access-control.md), [abstract classes](../language-reference/abstract-classes.md), and so on.</span></span> <span data-ttu-id="ab538-122">對於更複雜功能的程式碼，例如函式，必須了解內容，物件可以輕鬆地將封裝內容的資訊函式不能儲存方式。</span><span class="sxs-lookup"><span data-stu-id="ab538-122">For more complicated functional code, such as functions that must be context-aware, objects can easily encapsulate contextual information in ways that functions cannot.</span></span> <span data-ttu-id="ab538-123">這類功能[選擇性參數](../language-reference/members/methods.md#optional-arguments)和[多載](../language-reference/members/methods.md#overloaded-methods)也有助於讓呼叫端的耗用量的這項功能。</span><span class="sxs-lookup"><span data-stu-id="ab538-123">Features such as [optional parameters](../language-reference/members/methods.md#optional-arguments) and [overloading](../language-reference/members/methods.md#overloaded-methods) also aid consumption of this functionality for callers.</span></span>

4. <span data-ttu-id="ab538-124">**良好的 F # 程式碼執行也而不會暴露變動**</span><span class="sxs-lookup"><span data-stu-id="ab538-124">**Good F# code performs well without exposing mutation**</span></span>

    <span data-ttu-id="ab538-125">若要撰寫高效能程式碼，您必須使用變動沒有密碼它。</span><span class="sxs-lookup"><span data-stu-id="ab538-125">It's no secret that to write high-performance code, you must use mutation.</span></span> <span data-ttu-id="ab538-126">它是電腦的運作方式，在所有。</span><span class="sxs-lookup"><span data-stu-id="ab538-126">It's how computers work, after all.</span></span> <span data-ttu-id="ab538-127">這類程式碼通常是容易出錯且難度增加正確。</span><span class="sxs-lookup"><span data-stu-id="ab538-127">Such code is often error-prone and difficult to get right.</span></span> <span data-ttu-id="ab538-128">避免公開給呼叫端的變化。</span><span class="sxs-lookup"><span data-stu-id="ab538-128">Avoid exposing mutation to callers.</span></span> <span data-ttu-id="ab538-129">透過變動為基礎的實作搜尋功能的介面。</span><span class="sxs-lookup"><span data-stu-id="ab538-129">Seek a functional interface over a mutation-based implementation.</span></span>

5. <span data-ttu-id="ab538-130">**良好的 F # 程式碼是 toolable**</span><span class="sxs-lookup"><span data-stu-id="ab538-130">**Good F# code is toolable**</span></span>

    <span data-ttu-id="ab538-131">在大型程式碼基底的工具是重要的您可以撰寫 F # 程式碼，它可更有效地與 F # 語言工具。</span><span class="sxs-lookup"><span data-stu-id="ab538-131">Tools are invaluable for working in large codebases, you can write F# code such that it can be used more effectively with F# language tooling.</span></span> <span data-ttu-id="ab538-132">其中一個範例確定您不要過量使用點可用樣式的程式設計，以便可以進行偵錯工具檢查中繼值。</span><span class="sxs-lookup"><span data-stu-id="ab538-132">One example is making sure you don't overdo it with a point-free style of programming, so that intermediate values can be inspected with a debugger.</span></span> <span data-ttu-id="ab538-133">另一個範例使用[XML 文件註解](../language-reference/xml-documentation.md)描述建構，以便在編輯器中的工具提示可以顯示這些註解位於呼叫位置。</span><span class="sxs-lookup"><span data-stu-id="ab538-133">Another example is using [XML documentation comments](../language-reference/xml-documentation.md) describing constructs such that tooltips in editors can display those comments at the call site.</span></span> <span data-ttu-id="ab538-134">一律思考如何您的程式碼將會讀取、 巡覽、 偵錯，以及操作工具與其他程式設計人員的。</span><span class="sxs-lookup"><span data-stu-id="ab538-134">Always think about how your code will be read, navigated, debugged, and manipulated by other programmers with their tools.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ab538-135">後續步驟</span><span class="sxs-lookup"><span data-stu-id="ab538-135">Next steps</span></span>

<span data-ttu-id="ab538-136">[F # 程式碼格式化方針](formatting.md)提供如何格式化程式碼，使其更易讀的指引。</span><span class="sxs-lookup"><span data-stu-id="ab538-136">The [F# code formatting guidelines](formatting.md) provide guidance on how to format code so that it is easy to read.</span></span>

<span data-ttu-id="ab538-137">[F # 編碼慣例](conventions.md)F # 的程式設計語言，有助於長期維護較大的 F # 程式碼基底提供指引。</span><span class="sxs-lookup"><span data-stu-id="ab538-137">The [F# coding conventions](conventions.md) provide guidance for F# programming idioms that will help the long-term maintenance of larger F# codebases.</span></span>

<span data-ttu-id="ab538-138">[F # 元件的設計指導方針](component-design-guidelines.md)提供指導方針撰寫 F # 元件，例如文件庫。</span><span class="sxs-lookup"><span data-stu-id="ab538-138">The [F# component design guidelines](component-design-guidelines.md) provide guidance for authoring F# components, such as libraries.</span></span>