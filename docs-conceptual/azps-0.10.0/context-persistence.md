---
title: Контексты Azure и учетные данные для входа
description: Узнайте, как использовать учетные данные Azure и другие сведения в нескольких сеансах PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b6ac8b821f2d88431be67fd5fe1d50fc640d2b8f
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242007"
---
# <a name="azure-powershell-context-objects"></a><span data-ttu-id="aae40-103">Объекты контекста Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aae40-103">Azure PowerShell context objects</span></span>

<span data-ttu-id="aae40-104">Azure PowerShell использует _объекты контекста Azure PowerShell_ (контексты Azure) для хранения информации о подписке и аутентификации.</span><span class="sxs-lookup"><span data-stu-id="aae40-104">Azure PowerShell uses _Azure PowerShell context objects_ (Azure contexts) to hold subscription and authentication information.</span></span> <span data-ttu-id="aae40-105">При наличие нескольких подписок, контексты Azure позволяют выбрать подписку для запуска командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aae40-105">If you have more than one subscription, Azure contexts let you select the subscription to run Azure PowerShell cmdlets on.</span></span> <span data-ttu-id="aae40-106">Контексты Azure также используются для хранения данных для входа в несколько сеансов PowerShell и выполнения фоновых задач.</span><span class="sxs-lookup"><span data-stu-id="aae40-106">Azure contexts are also used to store sign-in information across multiple PowerShell sessions and run background tasks.</span></span>

<span data-ttu-id="aae40-107">Эта статья посвящена рассмотрению управления контекстами Azure, а не подписками или учетными записями.</span><span class="sxs-lookup"><span data-stu-id="aae40-107">This article covers managing Azure contexts, not the management of subscriptions or accounts.</span></span> <span data-ttu-id="aae40-108">Если вы хотите управлять пользователями, подписками, клиентами или другой информацией об учетной записи, см. документацию по [Azure Active Directory](/azure/active-directory).</span><span class="sxs-lookup"><span data-stu-id="aae40-108">If you're looking to manage users, subscriptions, tenants, or other account information, see the [Azure Active Directory](/azure/active-directory) documentation.</span></span> <span data-ttu-id="aae40-109">Чтобы узнать, как использовать контексты для выполнения фоновых или параллельных задач, см. раздел [Выполнение командлетов в параллельном режиме с помощью заданий PowerShell](using-psjobs.md) после ознакомления с контекстами Azure.</span><span class="sxs-lookup"><span data-stu-id="aae40-109">To learn about using contexts for running background or parallel tasks, see [Use Azure PowerShell cmdlets in PowerShell jobs](using-psjobs.md) after becoming familiar with Azure contexts.</span></span>

## <a name="overview-of-azure-context-objects"></a><span data-ttu-id="aae40-110">Обзор объектов контекста Azure</span><span class="sxs-lookup"><span data-stu-id="aae40-110">Overview of Azure context objects</span></span>

<span data-ttu-id="aae40-111">Контексты Azure — это объекты PowerShell, которые представляют активную подписку для выполнения команд и информацию об аутентификации, необходимую для подключения к облаку Azure.</span><span class="sxs-lookup"><span data-stu-id="aae40-111">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="aae40-112">Благодаря контекстам Azure, Azure PowerShell не требуется повторная аутентификация учетной записи при каждом переключении между подписками.</span><span class="sxs-lookup"><span data-stu-id="aae40-112">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="aae40-113">Контекст Azure состоит из:</span><span class="sxs-lookup"><span data-stu-id="aae40-113">An Azure context consists of:</span></span>

* <span data-ttu-id="aae40-114">_Учетной записи_, использованной для входа в Azure с помощью [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="aae40-114">The _account_ that was used to sign in to Azure with [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span></span> <span data-ttu-id="aae40-115">Контексты Azure обрабатывают пользователей, идентификаторы приложения и субъект-службы одинаково с точки зрения учетной записи.</span><span class="sxs-lookup"><span data-stu-id="aae40-115">Azure contexts treat users, application IDs, and service principals the same from an account perspective.</span></span>
* <span data-ttu-id="aae40-116">Активной _подписки_, соглашения об обслуживании Майкрософт для создания и запуска ресурсов Azure, связанных с _клиентом_.</span><span class="sxs-lookup"><span data-stu-id="aae40-116">The active _subscription_, a service agreement with Microsoft to create and run Azure resources, which are associated with a _tenant_.</span></span> <span data-ttu-id="aae40-117">В документации или при работе с Active Directory клиентов часто называют _организациями_.</span><span class="sxs-lookup"><span data-stu-id="aae40-117">Tenants are often referred to as _organizations_ in documentation or when working with Active Directory.</span></span>
* <span data-ttu-id="aae40-118">Ссылка на _кэш токена_ — сохраненный токен аутентификации для доступа к облаку Azure.</span><span class="sxs-lookup"><span data-stu-id="aae40-118">A reference to a _token cache_, a stored authentication token for accessing an Azure cloud.</span></span> <span data-ttu-id="aae40-119">[Настройки автосохранения контекста](#save-azure-contexts-across-powershell-sessions) определяют место и срок хранения этого токена.</span><span class="sxs-lookup"><span data-stu-id="aae40-119">Where this token is stored and how long it persists for is determined by the [context autosave settings](#save-azure-contexts-across-powershell-sessions).</span></span>

<span data-ttu-id="aae40-120">Дополнительные сведения об этих условиях см. в разделе [Терминология Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span><span class="sxs-lookup"><span data-stu-id="aae40-120">For more information on these terms, see [Azure Active Directory Terminology](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span></span> <span data-ttu-id="aae40-121">Токены аутентификации, используемые контекстами Azure, подобны другим сохраненным токенам, являющимся частью постоянного сеанса.</span><span class="sxs-lookup"><span data-stu-id="aae40-121">Authentication tokens used by Azure contexts are the same as other stored tokens that are part of a persistent session.</span></span> 

<span data-ttu-id="aae40-122">При входе с помощью `Connect-AzAccount`для подписки по умолчанию создается как минимум один контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="aae40-122">When you sign in with `Connect-AzAccount`, at least one Azure context is created for your default subscription.</span></span> <span data-ttu-id="aae40-123">Объект, возвращаемый `Connect-AzAccount` является контекстом Azure по умолчанию, используемым до конца сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aae40-123">The object returned by `Connect-AzAccount` is the default Azure context used for the rest of the PowerShell session.</span></span>

## <a name="get-azure-contexts"></a><span data-ttu-id="aae40-124">Получение контекстов Azure</span><span class="sxs-lookup"><span data-stu-id="aae40-124">Get Azure contexts</span></span>

<span data-ttu-id="aae40-125">Доступные контексты Azure извлекаются с помощью командлета [Get-AzContext](/powershell/module/az.accounts/get-azcontext).</span><span class="sxs-lookup"><span data-stu-id="aae40-125">Available Azure contexts are retrieved with the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet.</span></span> <span data-ttu-id="aae40-126">Перечислите все доступные контексты с помощью `-ListAvailable`:</span><span class="sxs-lookup"><span data-stu-id="aae40-126">List all of the available contexts with `-ListAvailable`:</span></span>

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

<span data-ttu-id="aae40-127">Или получите контекст по имени:</span><span class="sxs-lookup"><span data-stu-id="aae40-127">Or get a context by name:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

<span data-ttu-id="aae40-128">Имена контекстов могут отличаться от имен связанных подписок.</span><span class="sxs-lookup"><span data-stu-id="aae40-128">Context names may be different from the name of the associated subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aae40-129">Доступные контексты Azure __не__ всегда являются доступными подписками.</span><span class="sxs-lookup"><span data-stu-id="aae40-129">The available Azure contexts __aren't__ always your available subscriptions.</span></span> <span data-ttu-id="aae40-130">Контексты Azure представляют только локально хранимую информацию.</span><span class="sxs-lookup"><span data-stu-id="aae40-130">Azure contexts only represent locally-stored information.</span></span> <span data-ttu-id="aae40-131">Вы можете получить подписки с помощью командлета [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0).</span><span class="sxs-lookup"><span data-stu-id="aae40-131">You can get your subscriptions with the [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0) cmdlet.</span></span>

## <a name="create-a-new-azure-context-from-subscription-information"></a><span data-ttu-id="aae40-132">Создание нового контекста Azure из сведений о подписке</span><span class="sxs-lookup"><span data-stu-id="aae40-132">Create a new Azure context from subscription information</span></span>

<span data-ttu-id="aae40-133">Командлет [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) используется как для создания новых контекстов Azure, так и для их установки в качестве активного контекста.</span><span class="sxs-lookup"><span data-stu-id="aae40-133">The [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet is used to both create new Azure contexts and set them as the active context.</span></span>
<span data-ttu-id="aae40-134">Самый простой способ создать новый контекст Azure — использовать существующие сведения о подписке.</span><span class="sxs-lookup"><span data-stu-id="aae40-134">The easiest way to create a new Azure context is to use existing subscription information.</span></span> <span data-ttu-id="aae40-135">Командлет предназначен для получения объекта вывода из `Get-AzSubscription` в качестве переданного значения и настройки нового контекста Azure:</span><span class="sxs-lookup"><span data-stu-id="aae40-135">The cmdlet is designed to take the output object from `Get-AzSubscription` as a piped value and configure a new Azure context:</span></span>

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

<span data-ttu-id="aae40-136">При необходимости укажите либо имя, либо идентификатор подписки и идентификатор клиента:</span><span class="sxs-lookup"><span data-stu-id="aae40-136">Or give the subscription name or ID and the tenant ID if necessary:</span></span>

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

<span data-ttu-id="aae40-137">Если аргумент `-Name` пропущен, имя и идентификатор подписки используются в качестве имени контекста в формате `Subscription Name (subscription-id)`.</span><span class="sxs-lookup"><span data-stu-id="aae40-137">If the `-Name` argument is omitted, then the subscription's name and ID are used as the context name in the format `Subscription Name (subscription-id)`.</span></span>

## <a name="change-the-active-azure-context"></a><span data-ttu-id="aae40-138">Изменение активного контекста Azure</span><span class="sxs-lookup"><span data-stu-id="aae40-138">Change the active Azure context</span></span>

<span data-ttu-id="aae40-139">Для изменения активного контекста Azure можно использовать как `Set-AzContext`, так и [Select-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="aae40-139">Both `Set-AzContext` and [Select-AzContext](/powershell/module/az.accounts/set-azcontext) can be used to change the active Azure context.</span></span> <span data-ttu-id="aae40-140">Как описано в статье [Создание нового контекста Azure](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` создает новый контекст Azure для подписки, если он не существует, а затем переключается на использование этого контекста в качестве активного.</span><span class="sxs-lookup"><span data-stu-id="aae40-140">As described in [Create a new Azure context](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` creates a new Azure context for a subscription if one doesn't exist, and then switches to use that context as the active one.</span></span>

<span data-ttu-id="aae40-141">`Select-AzContext` предназначен для использования только с существующими контекстами Azure и работает аналогично использованию `Set-AzContext -Context`, но предназначен для использования с конвейером:</span><span class="sxs-lookup"><span data-stu-id="aae40-141">`Select-AzContext` is meant to be used with existing Azure contexts only and works similarly to using `Set-AzContext -Context`, but is designed for use with piping:</span></span>

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

<span data-ttu-id="aae40-142">Как и многие другие команды управления учетными записями и контекстами в Azure PowerShell, `Set-AzContext` и `Select-AzContext` поддерживают аргумент `-Scope`, чтобы можно было контролировать продолжительность активного контекста.</span><span class="sxs-lookup"><span data-stu-id="aae40-142">Like many other account and context management commands in Azure PowerShell, `Set-AzContext` and `Select-AzContext` support the `-Scope` argument so that you can control how long the context is active.</span></span> <span data-ttu-id="aae40-143">`-Scope` позволяет изменить активный контекст одного сеанса, не меняя значение по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="aae40-143">`-Scope` lets you change a single session's active context without changing the default:</span></span>

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

<span data-ttu-id="aae40-144">Чтобы избежать переключения контекстов для всего сеанса PowerShell, все команды Azure PowerShell могут выполняться в данном контексте с аргументом `-AzContext`:</span><span class="sxs-lookup"><span data-stu-id="aae40-144">To avoid switching contexts for a whole PowerShell session, all Azure PowerShell commands can be run against a given context with the `-AzContext` argument:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

<span data-ttu-id="aae40-145">Другое основное использование контекстов с командлетами Azure PowerShell — запуск фоновых команд.</span><span class="sxs-lookup"><span data-stu-id="aae40-145">The other main use of contexts with Azure PowerShell cmdlets is to run background commands.</span></span> <span data-ttu-id="aae40-146">Дополнительные сведения о запуске заданий PowerShell с помощью Azure PowerShell см. в разделе [Выполнение командлетов PowerShell Azure в заданиях PowerShell](using-psjobs.md).</span><span class="sxs-lookup"><span data-stu-id="aae40-146">To learn more about running PowerShell Jobs using Azure PowerShell, see [Run Azure PowerShell cmdlets in PowerShell Jobs](using-psjobs.md).</span></span>

## <a name="save-azure-contexts-across-powershell-sessions"></a><span data-ttu-id="aae40-147">Сохранение контекстов Azure в сеансах PowerShell</span><span class="sxs-lookup"><span data-stu-id="aae40-147">Save Azure contexts across PowerShell sessions</span></span>

<span data-ttu-id="aae40-148">По умолчанию контексты Azure сохраняются для использования между сеансами PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aae40-148">By default, Azure contexts are saved for use between PowerShell sessions.</span></span> <span data-ttu-id="aae40-149">Это поведение можно изменить следующими способами:</span><span class="sxs-lookup"><span data-stu-id="aae40-149">You change this behavior in the following ways:</span></span>

* <span data-ttu-id="aae40-150">Войдите, используя `-Scope Process` с помощью `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="aae40-150">Sign in using `-Scope Process` with `Connect-AzAccount`.</span></span>

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  <span data-ttu-id="aae40-151">Контекст Azure, возвращенный как часть этого входа, действителен _только_ для текущего сеанса и не будет автоматически сохраняться независимо от параметра автосохранения контекста Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aae40-151">The Azure context returned as part of this sign in is valid for the current session _only_ and will not be automatically saved, regardless of the Azure PowerShell context autosave setting.</span></span>
* <span data-ttu-id="aae40-152">Отключите автосохранение контекста Azure Powershell с помощью командлета [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="aae40-152">Disable AzurePowershell's context autosave with the [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet.</span></span>
  <span data-ttu-id="aae40-153">Отключение автосохранения контекста __не__ удаляет сохраненные токены.</span><span class="sxs-lookup"><span data-stu-id="aae40-153">Disabling context autosave __doesn't__ clear any stored tokens.</span></span> <span data-ttu-id="aae40-154">Чтобы узнать, как очистить сохраненную информацию о контексте Azure, см. раздел [Удаление контекстов и учетных данных Azure](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="aae40-154">To learn how to clear stored Azure context information, see [Remove Azure contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>
* <span data-ttu-id="aae40-155">Явное включение автосохранения контекста Azure можно включить с помощью командлета [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="aae40-155">Explicitly enable Azure context autosave can be enabled with the [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet.</span></span> <span data-ttu-id="aae40-156">При включенном автосохранении все контексты пользователя хранятся локально для последующих сеансов PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aae40-156">With autosave enabled, all of a user's contexts are stored locally for later PowerShell sessions.</span></span>
* <span data-ttu-id="aae40-157">Сохраните контексты вручную с помощью [Save-AzContext](/powershell/module/az.accounts/save-azcontext) для использования в будущих сеансах PowerShell, где их можно загрузить с помощью командлета [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span><span class="sxs-lookup"><span data-stu-id="aae40-157">Manually save contexts with [Save-AzContext](/powershell/module/az.accounts/save-azcontext) to be used in future PowerShell sessions, where they can be loaded with [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span></span>

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> <span data-ttu-id="aae40-158">Отключение автосохранения контекста __не__ удаляет сохраненную информацию контекста.</span><span class="sxs-lookup"><span data-stu-id="aae40-158">Disabling context autosave __doesn't__ clear any stored context information that was saved.</span></span> <span data-ttu-id="aae40-159">Чтобы удалить сохраненную информацию, используйте командлет [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="aae40-159">To remove stored information, use the [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet.</span></span> <span data-ttu-id="aae40-160">Подробнее об удалении сохраненных контекстов см. раздел [Удаление контекстов и учетных данных](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="aae40-160">For more on removing saved contexts, see [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>

<span data-ttu-id="aae40-161">Каждая из этих команд поддерживает параметр `-Scope`, который может принимать значение `Process` только для текущего запущенного процесса.</span><span class="sxs-lookup"><span data-stu-id="aae40-161">Each of these commands supports the `-Scope` parameter, which can take a value of `Process` to only apply to the current running process.</span></span> <span data-ttu-id="aae40-162">Например, чтобы убедиться, что вновь созданные контексты не сохраняются после выхода из сеанса PowerShell:</span><span class="sxs-lookup"><span data-stu-id="aae40-162">For example, to ensure that newly created contexts aren't saved after exiting a PowerShell session:</span></span>

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

<span data-ttu-id="aae40-163">Информация контекстов и токены хранятся в каталоге `$env:USERPROFILE\.Azure` в Windows и в `$HOME/.Azure` — на других платформах.</span><span class="sxs-lookup"><span data-stu-id="aae40-163">Context information and tokens are stored in the `$env:USERPROFILE\.Azure` directory on Windows, and on `$HOME/.Azure` on other platforms.</span></span> <span data-ttu-id="aae40-164">Конфиденциальная информация, такая как идентификаторы подписки и идентификаторы клиентов, может по-прежнему отображаться в сохраненной информации через журналы или сохраненные контексты.</span><span class="sxs-lookup"><span data-stu-id="aae40-164">Sensitive information such as subscription IDs and tenant IDs may still be exposed in stored information, through logs or saved contexts.</span></span> <span data-ttu-id="aae40-165">Чтобы узнать, как очистить сохраненную информацию, см. раздел [Удаление контекстов и учетных данных](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="aae40-165">To learn how to clear stored information, see the [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials) section.</span></span>

## <a name="remove-azure-contexts-and-stored-credentials"></a><span data-ttu-id="aae40-166">Удаление контекстов Azure и сохраненных учетных данных</span><span class="sxs-lookup"><span data-stu-id="aae40-166">Remove Azure contexts and stored credentials</span></span>

<span data-ttu-id="aae40-167">Для удаления контекстов и учетных данных Azure выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="aae40-167">To clear Azure contexts and credentials:</span></span>

* <span data-ttu-id="aae40-168">Выйдите из учетной записи с помощью командлета [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="aae40-168">Sign out of an account with [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span></span>
  <span data-ttu-id="aae40-169">Используя учетную запись или контекст, можно выйти из любой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="aae40-169">You can sign out of any account either by account or context:</span></span>

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  <span data-ttu-id="aae40-170">При отключении всегда удаляются сохраненные токены аутентификации и очищаются сохраненные контексты, связанные с отключенным пользователем или контекстом.</span><span class="sxs-lookup"><span data-stu-id="aae40-170">Disconnecting always removes stored authentication tokens and clears saved contexts associated with the disconnected user or context.</span></span>
* <span data-ttu-id="aae40-171">Используйте [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="aae40-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span></span> <span data-ttu-id="aae40-172">Этот командлет гарантированно всегда удаляет сохраненные контексты и токены аутентификации, а также выводит вас из системы.</span><span class="sxs-lookup"><span data-stu-id="aae40-172">This cmdlet is guaranteed to always remove stored contexts and authentication tokens, and will also sign you out.</span></span>
* <span data-ttu-id="aae40-173">Удаление контекста с помощью [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span><span class="sxs-lookup"><span data-stu-id="aae40-173">Remove a context with [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span></span>
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  <span data-ttu-id="aae40-174">При удалении активного контекста, вы будете отключены от Azure. Вам также потребуется повторно выполнить проверку подлинности с помощью `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="aae40-174">If you remove the active context, you will be disconnected from Azure and need to reauthenticate with `Connect-AzAccount`.</span></span>

## <a name="see-also"></a><span data-ttu-id="aae40-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aae40-175">See also</span></span>

* [<span data-ttu-id="aae40-176">Запуск командлетов Azure PowerShell в заданиях PowerShell</span><span class="sxs-lookup"><span data-stu-id="aae40-176">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>](using-psjobs.md)
* [<span data-ttu-id="aae40-177">Терминология Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="aae40-177">Azure Active Directory Terminology</span></span>](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [<span data-ttu-id="aae40-178">Справочные материалы по Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="aae40-178">Az.Accounts reference</span></span>](/powershell/module/az.accounts)
