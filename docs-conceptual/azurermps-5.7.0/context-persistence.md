---
title: Использование учетных данных пользователя в разных сеансах PowerShell
description: Узнайте, как использовать учетные данные Azure и другие сведения в нескольких сеансах PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 164444b7bacbef202513bfafe2f75bdcd6d027c4
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56145325"
---
# <a name="persisting-user-credentials-across-powershell-sessions"></a><span data-ttu-id="056a2-103">Использование учетных данных пользователя в разных сеансах PowerShell</span><span class="sxs-lookup"><span data-stu-id="056a2-103">Persisting user credentials across PowerShell sessions</span></span>

<span data-ttu-id="056a2-104">В Azure PowerShell существует функция **автосохранения контекста Azure**, которая предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="056a2-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="056a2-105">хранение учетных данных для входа для повторного использования в новых сеансах PowerShell;</span><span class="sxs-lookup"><span data-stu-id="056a2-105">Retention of sign in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="056a2-106">упрощенное использование фоновых задач для запуска долго выполняющихся командлетов;</span><span class="sxs-lookup"><span data-stu-id="056a2-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="056a2-107">переключение между учетными записями, подписками и средами без необходимости выполнять отдельный вход;</span><span class="sxs-lookup"><span data-stu-id="056a2-107">Switch between accounts, subscriptions, and environments without a separate sign in.</span></span>
- <span data-ttu-id="056a2-108">одновременное выполнение задач с использованием разных учетных данных и подписок в рамках одного сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="056a2-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="056a2-109">Определенные контексты Azure</span><span class="sxs-lookup"><span data-stu-id="056a2-109">Azure contexts defined</span></span>

<span data-ttu-id="056a2-110">*Контекст Azure* — это набор сведений, которые определяют целевой объект для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="056a2-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="056a2-111">Контекст состоит из пяти частей:</span><span class="sxs-lookup"><span data-stu-id="056a2-111">The context consists of five parts:</span></span>

- <span data-ttu-id="056a2-112">*Учетная запись* — имя пользователя или субъекта-службы, которое используется для аутентификации при обмене данными со средой Azure.</span><span class="sxs-lookup"><span data-stu-id="056a2-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="056a2-113">*Подписка* — подписка Azure, которая содержит используемые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="056a2-113">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="056a2-114">*Клиент* — клиент Azure Active Directory, который содержит вашу подписку.</span><span class="sxs-lookup"><span data-stu-id="056a2-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="056a2-115">Клиенты являются более важными при аутентификации субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="056a2-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="056a2-116">*Среда* — определяемое облако Azure (обычно это глобальное облако Azure).</span><span class="sxs-lookup"><span data-stu-id="056a2-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="056a2-117">Кроме того, параметр среды позволяет определять национальные и локальные (Azure Stack) облака, а также облака для государственных организаций.</span><span class="sxs-lookup"><span data-stu-id="056a2-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="056a2-118">*Учетные данные* — сведения, которые используются в Azure для идентификации и авторизации для доступа к ресурсам в Azure.</span><span class="sxs-lookup"><span data-stu-id="056a2-118">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="056a2-119">В предыдущих версиях контекст Azure нужно было создавать при каждом открытии нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="056a2-119">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="056a2-120">Начиная с версии Azure PowerShell 4.4.0 вы можете включить автоматическое сохранение и повторное использование контекстов Azure при каждом открытии нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="056a2-120">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-sign-in"></a><span data-ttu-id="056a2-121">Автоматическое сохранение контекста для следующего входа</span><span class="sxs-lookup"><span data-stu-id="056a2-121">Automatically saving the context for the next sign in</span></span>

<span data-ttu-id="056a2-122">По умолчанию Azure PowerShell не хранит данные контекста после закрытия сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="056a2-122">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="056a2-123">Чтобы разрешить Azure PowerShell запоминать контекст после закрытия сеанса PowerShell, используйте `Enable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="056a2-123">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="056a2-124">Учетные данные и данные контекста автоматически сохраняются в специальной скрытой папке в каталоге пользователя (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="056a2-124">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="056a2-125">Таким образом, каждый новый сеанс PowerShell обращается к контексту, который использовался в ходе последнего сеанса.</span><span class="sxs-lookup"><span data-stu-id="056a2-125">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="056a2-126">Чтобы PowerShell не сохранял учетные данные и данные контекста, используйте `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="056a2-126">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="056a2-127">Для работы с новым сеансом PowerShell вам нужно будет входить в Azure.</span><span class="sxs-lookup"><span data-stu-id="056a2-127">You will need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="056a2-128">Командлеты, которые помогают управлять контекстами Azure, также предоставляют удобные средства.</span><span class="sxs-lookup"><span data-stu-id="056a2-128">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="056a2-129">С их помощью вы можете применить изменения как для текущего сеанса PowerShell (область `Process`), так и для всех сеансов PowerShell (область `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="056a2-129">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="056a2-130">Эти параметры будут подробно описаны в разделе [Использование областей контекстов](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="056a2-130">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="056a2-131">Выполнение командлетов Azure PowerShell как фоновых заданий</span><span class="sxs-lookup"><span data-stu-id="056a2-131">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="056a2-132">Функция **автосохранения контекста Azure** также позволяет использовать контекст с фоновыми заданиями PowerShell.</span><span class="sxs-lookup"><span data-stu-id="056a2-132">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="056a2-133">PowerShell позволяет запускать и отслеживать долго выполняющиеся задачи как фоновые задания. Для этого вам не нужно дожидаться завершения их выполнения.</span><span class="sxs-lookup"><span data-stu-id="056a2-133">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="056a2-134">Чтобы использовать в фоновых заданиях учетные данные, можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="056a2-134">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="056a2-135">Передать контекст как аргумент.</span><span class="sxs-lookup"><span data-stu-id="056a2-135">Passing the context as an argument</span></span>

  <span data-ttu-id="056a2-136">Большинство командлетов AzureRM позволяют передавать контекст как параметр.</span><span class="sxs-lookup"><span data-stu-id="056a2-136">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="056a2-137">Передать контекст в фоновое задание можно так:</span><span class="sxs-lookup"><span data-stu-id="056a2-137">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="056a2-138">Использовать контекст по умолчанию со включенной функцией автосохранения</span><span class="sxs-lookup"><span data-stu-id="056a2-138">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="056a2-139">Если включить функцию **автосохранения контекста**, фоновые задания будут автоматически использовать сохраненный контекст по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="056a2-139">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="056a2-140">Если вам нужно узнать выходные данные фоновой задачи, используйте `Get-Job`, чтобы проверить состояние задания, и `Wait-Job`, чтобы дождаться завершения задания.</span><span class="sxs-lookup"><span data-stu-id="056a2-140">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="056a2-141">Используйте `Receive-Job`, чтобы записать или отобразить выходные данные фонового задания.</span><span class="sxs-lookup"><span data-stu-id="056a2-141">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="056a2-142">См. дополнительные сведения о [заданиях](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="056a2-142">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="056a2-143">Создание, выбор, переименование и удаление контекстов</span><span class="sxs-lookup"><span data-stu-id="056a2-143">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="056a2-144">Чтобы создать контекст, нужно войти в Azure.</span><span class="sxs-lookup"><span data-stu-id="056a2-144">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="056a2-145">Командлет `Connect-AzureRmAccount` (или его псевдоним `Login-AzureRmAccount`) определяет контекст по умолчанию, который будет использоваться последующими командлетами Azure PowerShell. Он также обеспечивает доступ к любому клиенту или подписке в рамках разрешений, предоставляемых вашими учетными данными.</span><span class="sxs-lookup"><span data-stu-id="056a2-145">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="056a2-146">Чтобы добавить новый контекст после входа, используйте командлет `Set-AzureRmContext` (или его псевдоним `Select-AzureRmSubscription`).</span><span class="sxs-lookup"><span data-stu-id="056a2-146">To add a new context after sign in, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="056a2-147">В примере выше мы добавили новый контекст для подписки "Contoso Subscription 1", используя текущие учетные данные.</span><span class="sxs-lookup"><span data-stu-id="056a2-147">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="056a2-148">Новый контекст называется "Contoso1".</span><span class="sxs-lookup"><span data-stu-id="056a2-148">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="056a2-149">Если вы не укажете имя для контекста, будет использоваться имя по умолчанию на основе идентификатора учетной записи и подписки.</span><span class="sxs-lookup"><span data-stu-id="056a2-149">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="056a2-150">Чтобы переименовать существующий контекста, используйте командлет `Rename-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="056a2-150">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="056a2-151">Например: </span><span class="sxs-lookup"><span data-stu-id="056a2-151">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="056a2-152">В этом примере мы изменяем стандартное имя контекста `[user1@contoso.org; 123456-7890-1234-564321]` на простое имя "Contoso2".</span><span class="sxs-lookup"><span data-stu-id="056a2-152">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="056a2-153">Командлеты, которые управляют контекстами, также поддерживают заполнение нажатием клавиши TAB. Это позволяет быстро выбрать контекст.</span><span class="sxs-lookup"><span data-stu-id="056a2-153">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="056a2-154">Наконец, чтобы удалить контекст, используйте командлет `Remove-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="056a2-154">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="056a2-155">Например: </span><span class="sxs-lookup"><span data-stu-id="056a2-155">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="056a2-156">Удаление контекста с именем "Contoso2".</span><span class="sxs-lookup"><span data-stu-id="056a2-156">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="056a2-157">Впоследствии этот контекст можно создать повторно с помощью командлета `Set-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="056a2-157">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="056a2-158">Удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="056a2-158">Removing credentials</span></span>

<span data-ttu-id="056a2-159">Вы можете удалить все учетные данные и связанные контексты пользователя или субъекта-службы с помощью командлета `Disconnect-AzureRmAccount` (или его псевдонима `Logout-AzureRmAccount`).</span><span class="sxs-lookup"><span data-stu-id="056a2-159">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="056a2-160">Выполняемый без параметров командлет `Disconnect-AzureRmAccount` удаляет все учетные данные и контексты, связанные с пользователем или субъектом-службой в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="056a2-160">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="056a2-161">Чтобы связать с контекстом определенный субъект, вы можете передать имя пользователя, имя субъекта-службы или сам контекст.</span><span class="sxs-lookup"><span data-stu-id="056a2-161">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="056a2-162">Использование областей контекстов</span><span class="sxs-lookup"><span data-stu-id="056a2-162">Using context scopes</span></span>

<span data-ttu-id="056a2-163">Иногда нужно выбрать, изменить или удалить контекст в сеансе PowerShell, не влияя на другие сеансы.</span><span class="sxs-lookup"><span data-stu-id="056a2-163">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="056a2-164">Чтобы изменить стандартное поведение командлетов, управляющих контекстом, используйте параметр `Scope`.</span><span class="sxs-lookup"><span data-stu-id="056a2-164">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="056a2-165">Область `Process` переопределяет стандартное поведение, ограничивая его действие текущим сеансом.</span><span class="sxs-lookup"><span data-stu-id="056a2-165">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="056a2-166">И наоборот, область `CurrentUser` изменяет контекст во всех сеансах, а не только в текущем.</span><span class="sxs-lookup"><span data-stu-id="056a2-166">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="056a2-167">Например, вот как можно изменить контекст по умолчанию в текущем сеансе PowerShell, не влияя на другие окна, или изменить контекст, который будет использоваться при следующем открытии сеанса:</span><span class="sxs-lookup"><span data-stu-id="056a2-167">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="056a2-168">Запоминание параметра автосохранения контекста</span><span class="sxs-lookup"><span data-stu-id="056a2-168">How the context autosave setting is remembered</span></span>

<span data-ttu-id="056a2-169">Параметр автосохранения контекста сохраняется в каталоге пользователя Azure PowerShell (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="056a2-169">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="056a2-170">На некоторых компьютерах учетные записи могут не иметь доступ к этому каталогу.</span><span class="sxs-lookup"><span data-stu-id="056a2-170">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="056a2-171">В таких случаях можно использовать переменную среды</span><span class="sxs-lookup"><span data-stu-id="056a2-171">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="056a2-172">Если задано значение true, контекст сохраняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="056a2-172">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="056a2-173">Если задано значение false, контекст не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="056a2-173">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="056a2-174">Изменения в модуле AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="056a2-174">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="056a2-175">Новые командлеты для управления контекстом</span><span class="sxs-lookup"><span data-stu-id="056a2-175">New cmdlets for managing context</span></span>

- <span data-ttu-id="056a2-176">[Enable-AzureRmContextAutosave][enable] — включение сохранения контекста для использования в разных сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="056a2-176">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="056a2-177">Любые изменения влияют на глобальный контекст.</span><span class="sxs-lookup"><span data-stu-id="056a2-177">Any changes alter the global context.</span></span>
- <span data-ttu-id="056a2-178">[Disable-AzureRmContextAutosave][disable] — отключение автосохранения контекста.</span><span class="sxs-lookup"><span data-stu-id="056a2-178">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="056a2-179">Для работы с новым сеансом PowerShell нужно будет выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="056a2-179">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="056a2-180">[Select-AzureRmContext][select] — выбор контекста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="056a2-180">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="056a2-181">Все последующие командлеты будут использовать для аутентификации учетные данные из этого контекста.</span><span class="sxs-lookup"><span data-stu-id="056a2-181">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="056a2-182">[Disconnect-AzureRmAccount][remove-cred] — удаление всех учетных данных и контекстов, связанных с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="056a2-182">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="056a2-183">[Remove-AzureRmContext][remove-context] — удаление именованного контекста.</span><span class="sxs-lookup"><span data-stu-id="056a2-183">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="056a2-184">[Rename-AzureRmContext][rename] — переименование существующего контекста.</span><span class="sxs-lookup"><span data-stu-id="056a2-184">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="056a2-185">Изменения в существующих командлетах профиля</span><span class="sxs-lookup"><span data-stu-id="056a2-185">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="056a2-186">[Add-AzureRmAccount][login] — возможность входа на уровне процесса или текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="056a2-186">[Add-AzureRmAccount][login] - Allow scoping of the sign in to the process or the current user.</span></span>
  <span data-ttu-id="056a2-187">После аутентификации разрешено присваивать имя контексту по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="056a2-187">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="056a2-188">[Import-AzureRmContext][import] — возможность входа на уровне процесса или текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="056a2-188">[Import-AzureRmContext][import] - Allow scoping of the sign in to the process or the current user.</span></span>
- <span data-ttu-id="056a2-189">[Set-AzureRmContext][set-context] — возможность выбора существующих именованных контекстов и применения изменений на уровне процесса или текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="056a2-189">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
