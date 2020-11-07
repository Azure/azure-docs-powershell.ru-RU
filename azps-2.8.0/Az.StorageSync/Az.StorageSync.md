---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 3bfdc9c488f02794e82388741e7103417878c9f6
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/15/2019
ms.locfileid: "93720028"
---
# <span data-ttu-id="60ee6-101">AZ. StorageSync Module</span><span class="sxs-lookup"><span data-stu-id="60ee6-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="60ee6-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="60ee6-102">Description</span></span>
<span data-ttu-id="60ee6-103">Командлеты в модуле синхронизации хранилища позволяют управлять операциями, относящимися к синхронизации файлов Azure в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="60ee6-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="60ee6-104">Командлеты AZ. StorageSync</span><span class="sxs-lookup"><span data-stu-id="60ee6-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="60ee6-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="60ee6-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="60ee6-106">Эта команда перечисляет все конечные точки облака в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="60ee6-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="60ee6-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="60ee6-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="60ee6-108">Эта команда выводит список всех групп синхронизации в заданной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="60ee6-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="60ee6-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="60ee6-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="60ee6-110">Эта команда перечисляет все серверы, зарегистрированные для указанной службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="60ee6-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="60ee6-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="60ee6-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="60ee6-112">Эта команда перечисляет все конечные точки сервера в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="60ee6-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="60ee6-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="60ee6-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="60ee6-114">Эта команда выводит список всех служб синхронизации хранилища в заданной области подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60ee6-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="60ee6-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="60ee6-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="60ee6-116">С помощью этой команды можно вручную инициировать обнаружение изменений в пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="60ee6-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="60ee6-117">Она может быть назначена всему общему доступу, вложенной папке или набору файлов.</span><span class="sxs-lookup"><span data-stu-id="60ee6-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="60ee6-118">Может быть обнаружено не более 10 000 изменений.</span><span class="sxs-lookup"><span data-stu-id="60ee6-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="60ee6-119">Если вы задаете область изменений, ограничьте выполнение этой команды на части пространства имен, поэтому обнаружение изменений может завершиться быстро и в течение 10 000 изменится.</span><span class="sxs-lookup"><span data-stu-id="60ee6-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="60ee6-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="60ee6-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="60ee6-121">Проверка наличия потенциальных проблем с совместимостью системы и синхронизации файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="60ee6-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="60ee6-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="60ee6-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="60ee6-123">Эта команда повторно вызывает все многоуровневые файлы на локальный диск.</span><span class="sxs-lookup"><span data-stu-id="60ee6-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="60ee6-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="60ee6-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="60ee6-125">Эта команда создает облачную конечную точку синхронизации файлов Azure в группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="60ee6-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="60ee6-126">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="60ee6-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="60ee6-127">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="60ee6-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="60ee6-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="60ee6-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="60ee6-129">Эта команда создает новую конечную точку сервера на зарегистрированном сервере.</span><span class="sxs-lookup"><span data-stu-id="60ee6-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="60ee6-130">Это позволяет заданному пути на сервере запустить синхронизацию файлов с другими конечными точками в группе "Синхронизация".</span><span class="sxs-lookup"><span data-stu-id="60ee6-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="60ee6-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="60ee6-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="60ee6-132">Эта команда создает новую службу синхронизации хранилища в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="60ee6-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="60ee6-133">Регистрация — AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="60ee6-133">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="60ee6-134">Эта команда регистрирует сервер для службы синхронизации хранилища, который создает отношение доверия.</span><span class="sxs-lookup"><span data-stu-id="60ee6-134">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="60ee6-135">Вы можете использовать PowerShell или портал Azure для настройки синхронизации на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="60ee6-135">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="60ee6-136">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="60ee6-136">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="60ee6-137">Эта команда удалит указанную облачную конечную точку из группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="60ee6-137">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="60ee6-138">Без хотя бы одной конечной точки облака нельзя синхронизировать другие конечные точки сервера в этой группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="60ee6-138">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="60ee6-139">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="60ee6-139">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="60ee6-140">Эта команда удалит указанную группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="60ee6-140">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="60ee6-141">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="60ee6-141">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="60ee6-142">Эта команда удалит указанную конечную точку сервера.</span><span class="sxs-lookup"><span data-stu-id="60ee6-142">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="60ee6-143">Синхронизация с этим расположением будет немедленно остановлена.</span><span class="sxs-lookup"><span data-stu-id="60ee6-143">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="60ee6-144">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="60ee6-144">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="60ee6-145">Эта команда удалит указанную службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="60ee6-145">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="60ee6-146">Сброс — AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="60ee6-146">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="60ee6-147">Используется только для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="60ee6-147">Use for troubleshooting only.</span></span> <span data-ttu-id="60ee6-148">Эта команда выполняет откат сертификата сервера синхронизации хранилища, используемого для описания удостоверения сервера для службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="60ee6-148">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="60ee6-149">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="60ee6-149">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="60ee6-150">Эта команда позволяет вносить изменения в регулируемых параметрах конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="60ee6-150">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="60ee6-151">Отмена регистрации — AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="60ee6-151">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="60ee6-152">Предупреждение: Отмена регистрации сервера приводит к каскадному удалению всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="60ee6-152">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="60ee6-153">Эта команда отменит регистрацию сервера в службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="60ee6-153">This command will unregister a server from it's storage sync service.</span></span>

