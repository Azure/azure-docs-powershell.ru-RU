---
title: Использование экспериментальных модулей Azure PowerShell
description: Принципы и особенности использования экспериментальных модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 77d0ce36ae3ab7c7bddd3febef4600fc9652850f
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/08/2018
ms.locfileid: "51274523"
---
# <a name="use-experimental-azure-powershell-modules"></a><span data-ttu-id="1e7c6-103">Использование экспериментальных модулей Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e7c6-103">Use experimental Azure PowerShell modules</span></span>

<span data-ttu-id="1e7c6-104">Команда Azure PowerShell уделяет особое внимание средствам для разработчиков в Azure (в особенности интерфейсам CLI). Для этого мы проводим множество экспериментов, оценивая усовершенствования и оптимизируя работу с Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="1e7c6-105">Методология экспериментов</span><span class="sxs-lookup"><span data-stu-id="1e7c6-105">Experimentation methodology</span></span>

<span data-ttu-id="1e7c6-106">Мы создаем модули Azure PowerShell, которые упрощают использование существующих функций пакета Azure SDK в рамках экспериментов.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-106">To facilitate experimentation, we're creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="1e7c6-107">В большинстве случаев новые командлеты точно соответствуют существующим.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="1e7c6-108">При этом экспериментальные командлеты обеспечивают сокращенную нотацию и оптимизированные стандартные значения. Это упрощает процесс создания и администрирования ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="1e7c6-109">Эти модули можно установить параллельно с существующими модулями Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-109">These modules can be installed side by side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="1e7c6-110">Имена командлетов сокращены для удобства. Также это сделано, чтобы избежать конфликтов с именами существующих командлетов, которые не предназначены для экспериментов.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="1e7c6-111">Для экспериментальных модулей используется следующее соглашение об именовании: `AzureRM.*.Experiments`.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-111">The experimental modules use the following naming convention: `AzureRM.*.Experiments`.</span></span> <span data-ttu-id="1e7c6-112">Это соглашение об именовании соответствует правилам именования модулей, используемых в режиме предварительной версии: `AzureRM.*.Preview`.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-112">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="1e7c6-113">Модули, используемые в режиме предварительной версии, отличаются от экспериментальных модулей.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-113">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="1e7c6-114">В таких модулях реализованы новые функции служб Azure, доступные только в предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-114">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="1e7c6-115">Модули предварительной версии заменяют существующие модули Azure PowerShell. В них используется те же имена командлетов и параметров.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-115">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="1e7c6-116">Как установить экспериментальный модуль</span><span class="sxs-lookup"><span data-stu-id="1e7c6-116">How to install an experimental module</span></span>

<span data-ttu-id="1e7c6-117">Экспериментальные модули публикуются в коллекции PowerShell так же, как и существующие модули Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-117">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="1e7c6-118">Чтобы просмотреть список экспериментальный модулей, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1e7c6-118">To see a list of experimental modules, run the following command:</span></span>

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

<span data-ttu-id="1e7c6-119">Чтобы установить экспериментальный модуль, используйте следующие команды из сеанса PowerShell с повышенными привилегиями:</span><span class="sxs-lookup"><span data-stu-id="1e7c6-119">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="1e7c6-120">Документация и поддержка</span><span class="sxs-lookup"><span data-stu-id="1e7c6-120">Documentation and support</span></span>

<span data-ttu-id="1e7c6-121">Документация включена в пакет установки. Просмотреть ее можно с помощью командлета `Get-Help`.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-121">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="1e7c6-122">Для экспериментальных модулей официальная документация не опубликована.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-122">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="1e7c6-123">Рекомендуем протестировать эти модули.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-123">We encourage you to test these modules.</span></span> <span data-ttu-id="1e7c6-124">Ваши отзывы помогут повысить удобство использования и привести продукт в соответствие с вашими требованиями.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-124">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="1e7c6-125">Но так как эти модули являются экспериментальными, их поддержка ограничена.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-125">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="1e7c6-126">Вопросы или сообщения о проблемах можно отправлять, создав [вопрос](https://github.com/Azure/azure-powershell/issues) в репозитории GitHub.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-126">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="1e7c6-127">Эксперименты и области усовершенствований</span><span class="sxs-lookup"><span data-stu-id="1e7c6-127">Experiments and areas of improvement</span></span>

<span data-ttu-id="1e7c6-128">Эти усовершенствования выбраны на основе отличий с конкурирующими продуктами.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-128">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="1e7c6-129">Например, в Azure CLI 2.0 команды в большей степени основываются на _сценариях_, а не на _контактной зоне API_.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-129">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="1e7c6-130">В Azure CLI 2.0 используется ряд стандартных интеллектуальных значений, которые помогают пользователям быстрее приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-130">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="1e7c6-131">Основные усовершенствования</span><span class="sxs-lookup"><span data-stu-id="1e7c6-131">Core improvements</span></span>

<span data-ttu-id="1e7c6-132">Основные усовершенствования рассматриваются с точки зрения здравого смысла. Для реализации этих обновлений требуется незначительно число экспериментов.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-132">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="1e7c6-133">Командлеты на основе сценария. <em>\*Все</em> командлеты должны разрабатываться на основе сценариев, а не на основе службы Azure REST.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-133">Scenario-based Cmdlets - <em>\*All</em>- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="1e7c6-134">Сокращение имен. Это касается имен командлетов (например, `New-AzureRmVM` => `New-AzVm`) и параметров (например, `-ResourceGroupName` => `-Rg`).</span><span class="sxs-lookup"><span data-stu-id="1e7c6-134">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="1e7c6-135">Чтобы обеспечить совместимость со старыми версиями командлетов, используйте псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-135">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="1e7c6-136">Обеспечьте _обратную совместимость_ наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-136">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="1e7c6-137">Стандартные интеллектуальные значения. Создайте стандартные интеллектуальные значения для заполнения обязательных полей.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-137">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="1e7c6-138">Например: </span><span class="sxs-lookup"><span data-stu-id="1e7c6-138">For example:</span></span>
  - <span data-ttu-id="1e7c6-139">Группа ресурсов</span><span class="sxs-lookup"><span data-stu-id="1e7c6-139">Resource Group</span></span>
  - <span data-ttu-id="1e7c6-140">Расположение</span><span class="sxs-lookup"><span data-stu-id="1e7c6-140">Location</span></span>
  - <span data-ttu-id="1e7c6-141">Зависимые ресурсы</span><span class="sxs-lookup"><span data-stu-id="1e7c6-141">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="1e7c6-142">Экспериментальные усовершенствования</span><span class="sxs-lookup"><span data-stu-id="1e7c6-142">Experimental improvements</span></span>

<span data-ttu-id="1e7c6-143">Экспериментальные усовершенствования — это существенное изменение, которое группе нужно проверить в ходе экспериментов.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-143">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="1e7c6-144">Простые типы. В сценариях создания не должны использоваться сложные типы и объекты конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-144">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="1e7c6-145">Упростите конфигурацию, ограничившись одним или двумя параметрами.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-145">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="1e7c6-146">Интеллектуальный процесс создания. Для всех сценариев создания, в которых реализован интеллектуальный процесс, _не_ используются обязательные параметры. Вся необходимая информация определяется исключительно Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-146">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="1e7c6-147">Параметры, выделенные серым. Во многих случаях некоторые параметры могут выделяться серым. Это значит, что они частично необязательны.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-147">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="1e7c6-148">Если параметр не указан, пользователь получает запрос на создание параметра.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-148">If the parameter isn't specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="1e7c6-149">Также для параметров, выделенных серым, с согласия пользователя можно вывести значение на основе контекста.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-149">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="1e7c6-150">Например, имеет смысл задать для выделенного серым параметра наиболее часто используемое значение.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-150">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="1e7c6-151">Переключатель `-Auto`. Переключатель `-Auto` позволяет с согласия пользователя _задать все параметры по умолчанию_. При этом целостность обязательных параметров в основном пути сохраняется.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-151">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="1e7c6-152">Переключатели для конкретных функций</span><span class="sxs-lookup"><span data-stu-id="1e7c6-152">Feature-specific switches</span></span>

<span data-ttu-id="1e7c6-153">Например, в сценарии создания веб-приложения может использоваться переключатель `-Git` или `-AddRemote`, который автоматически добавляет удаленный объект azure в существующий репозиторий Git.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-153">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="1e7c6-154">Устанавливаемые значения по умолчанию. Пользователи должны иметь возможность задать значения по умолчанию для распространенных параметров, таких как `-ResourceGroupName` и `-Location`.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-154">Settable Defaults - Users should be able to set defaults for common parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="1e7c6-155">Размер по умолчанию. Размер ресурса может быть затруднительным параметром для пользователя, так как многие поставщики ресурсов используют разные имена (например, Standard\_DS1\_v2 или S1).</span><span class="sxs-lookup"><span data-stu-id="1e7c6-155">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="1e7c6-156">Но большинство пользователей волнуют затраты.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-156">However, most users care more about cost.</span></span> <span data-ttu-id="1e7c6-157">Поэтому есть смысл определить универсальные размеры на основе расценок.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-157">So it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="1e7c6-158">Пользователи могут выбрать определенный размер и разрешить Azure PowerShell выбрать _наилучший вариант_ ресурса, исходя из бюджета.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-158">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="1e7c6-159">Формат вывода. Сейчас Azure PowerShell возвращает объекты `PSObject`. Выходные данные консоли при этом незначительны.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-159">Output Format - Azure PowerShell currently returns `PSObject`s and there's little console output.</span></span> <span data-ttu-id="1e7c6-160">Возможно, Azure PowerShell потребуется вывести для пользователя некоторые сведения об используемых стандартных интеллектуальных значениях.</span><span class="sxs-lookup"><span data-stu-id="1e7c6-160">Azure PowerShell may need to display some information to the user about the "smart defaults" used.</span></span>
