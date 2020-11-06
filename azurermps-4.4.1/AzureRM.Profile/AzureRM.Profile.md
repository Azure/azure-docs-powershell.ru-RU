---
Module Name: AzureRM.Profile
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/AzureRM.Profile.md
ms.openlocfilehash: bc3ccc2c2b0574eee40357fb0079fe22124ea3e6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93555064"
---
# <span data-ttu-id="53ee7-101">Модуль AzureRM. Profile</span><span class="sxs-lookup"><span data-stu-id="53ee7-101">AzureRM.Profile Module</span></span>
## <span data-ttu-id="53ee7-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="53ee7-102">Description</span></span>
<span data-ttu-id="53ee7-103">Управление учетными данными и общей конфигурацией для всех модулей Azure.</span><span class="sxs-lookup"><span data-stu-id="53ee7-103">Manages credentials and common configuration for all Azure modules.</span></span>

## <span data-ttu-id="53ee7-104">Командлеты AzureRM. Profile</span><span class="sxs-lookup"><span data-stu-id="53ee7-104">AzureRM.Profile Cmdlets</span></span>
### [<span data-ttu-id="53ee7-105">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="53ee7-105">Add-AzureRmAccount</span></span>](Add-AzureRmAccount.md)
<span data-ttu-id="53ee7-106">Добавляет учетную запись с проверкой подлинности, которая используется для запросов командлетов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="53ee7-106">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

### [<span data-ttu-id="53ee7-107">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="53ee7-107">Add-AzureRmEnvironment</span></span>](Add-AzureRmEnvironment.md)
<span data-ttu-id="53ee7-108">Добавляет конечные точки и метаданные для экземпляра диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="53ee7-108">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

### [<span data-ttu-id="53ee7-109">Clear-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="53ee7-109">Clear-AzureRmContext</span></span>](Clear-AzureRmContext.md)
<span data-ttu-id="53ee7-110">Удалите все учетные данные Azure, учетную запись и сведения о подписке.</span><span class="sxs-lookup"><span data-stu-id="53ee7-110">Remove all Azure credentials, account, and subscription information.</span></span>

### [<span data-ttu-id="53ee7-111">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="53ee7-111">Disable-AzureRmContextAutosave</span></span>](Disable-AzureRmContextAutosave.md)
<span data-ttu-id="53ee7-112">Отключите Автосохранение учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="53ee7-112">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="53ee7-113">Ваши регистрационные данные будут утрачены при следующем открытии окна PowerShell.</span><span class="sxs-lookup"><span data-stu-id="53ee7-113">Your login information will be forgotten the next time you open a PowerShell window</span></span>

### [<span data-ttu-id="53ee7-114">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="53ee7-114">Disable-AzureRmDataCollection</span></span>](Disable-AzureRmDataCollection.md)
<span data-ttu-id="53ee7-115">Изменяют сбор данных, чтобы улучшить командлеты AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="53ee7-115">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="53ee7-116">Данные не собираются, пока не будет явно задействовано.</span><span class="sxs-lookup"><span data-stu-id="53ee7-116">Data is not collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="53ee7-117">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="53ee7-117">Enable-AzureRmContextAutosave</span></span>](Enable-AzureRmContextAutosave.md)
<span data-ttu-id="53ee7-118">Предоставление учетных данных Azure, учетной записи и сведений о подписке для сохранения и автоматической загрузки при открытии окна PowerShell.</span><span class="sxs-lookup"><span data-stu-id="53ee7-118">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

### [<span data-ttu-id="53ee7-119">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="53ee7-119">Enable-AzureRmDataCollection</span></span>](Enable-AzureRmDataCollection.md)
<span data-ttu-id="53ee7-120">Позволяет Azure PowerShell собирать данные, чтобы улучшить взаимодействие с пользователем с помощью командлетов AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="53ee7-120">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="53ee7-121">Выполнение этого командлета наследуется в сборе данных для текущего пользователя на текущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="53ee7-121">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="53ee7-122">Никакие данные не собираются, пока не будет явно задействовано.</span><span class="sxs-lookup"><span data-stu-id="53ee7-122">No data is collected unless you explicitly opt in.</span></span>

### [<span data-ttu-id="53ee7-123">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="53ee7-123">Get-AzureRmContext</span></span>](Get-AzureRmContext.md)
<span data-ttu-id="53ee7-124">Получает метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="53ee7-124">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

### [<span data-ttu-id="53ee7-125">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="53ee7-125">Get-AzureRmContextAutosaveSetting</span></span>](Get-AzureRmContextAutosaveSetting.md)
<span data-ttu-id="53ee7-126">Отображение метаданных о функции автосохранения контекста, в том числе whterh контекст автоматически сохраняется, где можно найти сохраненные сведения о контексте и учетных данных.</span><span class="sxs-lookup"><span data-stu-id="53ee7-126">Display metadata about the context autosave feature, including whterh the context is automatically saved, and where saved context and credential information can be found.</span></span>

### [<span data-ttu-id="53ee7-127">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="53ee7-127">Get-AzureRmEnvironment</span></span>](Get-AzureRmEnvironment.md)
<span data-ttu-id="53ee7-128">Получение конечных точек и метаданных для экземпляра служб Azure.</span><span class="sxs-lookup"><span data-stu-id="53ee7-128">Get endpoints and metadata for an instance of Azure services.</span></span>

### [<span data-ttu-id="53ee7-129">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="53ee7-129">Get-AzureRmSubscription</span></span>](Get-AzureRmSubscription.md)
<span data-ttu-id="53ee7-130">Получение подписок, доступ к которым разрешен текущей учетной записью.</span><span class="sxs-lookup"><span data-stu-id="53ee7-130">Get subscriptions that the current account can access.</span></span>

### [<span data-ttu-id="53ee7-131">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="53ee7-131">Get-AzureRmTenant</span></span>](Get-AzureRmTenant.md)
<span data-ttu-id="53ee7-132">Возвращает клиентов, которые авторизованы для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="53ee7-132">Gets tenants that are authorized for the current user.</span></span>

### [<span data-ttu-id="53ee7-133">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="53ee7-133">Import-AzureRmContext</span></span>](Import-AzureRmContext.md)
<span data-ttu-id="53ee7-134">Загрузка данных проверки подлинности Azure из файла.</span><span class="sxs-lookup"><span data-stu-id="53ee7-134">Loads Azure authentication information from a file.</span></span>

### [<span data-ttu-id="53ee7-135">Remove-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="53ee7-135">Remove-AzureRmAccount</span></span>](Remove-AzureRmAccount.md)
<span data-ttu-id="53ee7-136">Удалите все учетные данные и контексты, связанные с этой учетной записью.</span><span class="sxs-lookup"><span data-stu-id="53ee7-136">Remove all credentials and contexts associated with this account.</span></span>

### [<span data-ttu-id="53ee7-137">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="53ee7-137">Remove-AzureRmContext</span></span>](Remove-AzureRmContext.md)
<span data-ttu-id="53ee7-138">Удаление контекста из набора доступных контекстов</span><span class="sxs-lookup"><span data-stu-id="53ee7-138">Remove a context from the set of available contexts</span></span>

### [<span data-ttu-id="53ee7-139">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="53ee7-139">Remove-AzureRmEnvironment</span></span>](Remove-AzureRmEnvironment.md)
<span data-ttu-id="53ee7-140">Удаляет конечные точки и метаданные для подключения к определенному экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="53ee7-140">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

### [<span data-ttu-id="53ee7-141">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="53ee7-141">Rename-AzureRmContext</span></span>](Rename-AzureRmContext.md)
<span data-ttu-id="53ee7-142">Переименуйте контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="53ee7-142">Rename an Azure context.</span></span>  <span data-ttu-id="53ee7-143">По умолчанию контексты названы учетной записью пользователя и подпиской.</span><span class="sxs-lookup"><span data-stu-id="53ee7-143">By default contexts are named by user account and subscription.</span></span>

### [<span data-ttu-id="53ee7-144">Resolve-AzureRmError</span><span class="sxs-lookup"><span data-stu-id="53ee7-144">Resolve-AzureRmError</span></span>](Resolve-AzureRmError.md)
<span data-ttu-id="53ee7-145">Отображение подробных сведений об ошибках PowerShell с дополнительными сведениями об ошибках Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="53ee7-145">Display detailed information about PowerShell errors, with extended details for Azure PowerShell errors.</span></span>

### [<span data-ttu-id="53ee7-146">Сохранить — AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="53ee7-146">Save-AzureRmContext</span></span>](Save-AzureRmContext.md)
<span data-ttu-id="53ee7-147">Сохранение текущих сведений для проверки подлинности для использования в других сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="53ee7-147">Saves the current authentication information for use in other PowerShell sessions.</span></span>

### [<span data-ttu-id="53ee7-148">SELECT-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="53ee7-148">Select-AzureRmContext</span></span>](Select-AzureRmContext.md)
<span data-ttu-id="53ee7-149">Выберите подписку для назначения (или учетной записи, клиента) в командлетах PowerShell для Azure</span><span class="sxs-lookup"><span data-stu-id="53ee7-149">Select a subscription to target (or account, tenant) in Azure PowerShell cmdlets</span></span>

### [<span data-ttu-id="53ee7-150">Отправка и отзыв</span><span class="sxs-lookup"><span data-stu-id="53ee7-150">Send-Feedback</span></span>](Send-Feedback.md)
<span data-ttu-id="53ee7-151">Отправляет отзыв команде Azure PowerShell с помощью набора интерактивных запросов.</span><span class="sxs-lookup"><span data-stu-id="53ee7-151">Sends feedback to the Azure PowerShell team via a set of guided prompts.</span></span>

### [<span data-ttu-id="53ee7-152">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="53ee7-152">Set-AzureRmContext</span></span>](Set-AzureRmContext.md)
<span data-ttu-id="53ee7-153">Задает клиента, подписку и среду для командлетов, используемых в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="53ee7-153">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

### [<span data-ttu-id="53ee7-154">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="53ee7-154">Set-AzureRmEnvironment</span></span>](Set-AzureRmEnvironment.md)
<span data-ttu-id="53ee7-155">Задает свойства среды Azure.</span><span class="sxs-lookup"><span data-stu-id="53ee7-155">Sets properties for an Azure environment.</span></span>

