---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 1ab1690d3c5fccca2994abc4958f3cf7e6a4e52d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93719836"
---
# <span data-ttu-id="83069-101">AZ. StorageSync Module</span><span class="sxs-lookup"><span data-stu-id="83069-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="83069-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="83069-102">Description</span></span>
<span data-ttu-id="83069-103">Командлеты в модуле синхронизации хранилища позволяют управлять операциями, относящимися к синхронизации файлов Azure в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="83069-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="83069-104">Командлеты AZ. StorageSync</span><span class="sxs-lookup"><span data-stu-id="83069-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="83069-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="83069-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="83069-106">Эта команда перечисляет все конечные точки облака в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="83069-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="83069-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="83069-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="83069-108">Эта команда выводит список всех групп синхронизации в заданной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="83069-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="83069-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="83069-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="83069-110">Эта команда перечисляет все серверы, зарегистрированные для указанной службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="83069-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="83069-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="83069-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="83069-112">Эта команда перечисляет все конечные точки сервера в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="83069-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="83069-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="83069-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="83069-114">Эта команда выводит список всех служб синхронизации хранилища в заданной области подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83069-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="83069-115">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="83069-115">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="83069-116">Проверка наличия потенциальных проблем с совместимостью системы и синхронизации файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="83069-116">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="83069-117">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="83069-117">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="83069-118">Эта команда повторно вызывает все многоуровневые файлы на локальный диск.</span><span class="sxs-lookup"><span data-stu-id="83069-118">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="83069-119">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="83069-119">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="83069-120">Эта команда создает облачную конечную точку синхронизации файлов Azure в группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="83069-120">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="83069-121">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="83069-121">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="83069-122">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="83069-122">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="83069-123">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="83069-123">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="83069-124">Эта команда создает новую конечную точку сервера на зарегистрированном сервере.</span><span class="sxs-lookup"><span data-stu-id="83069-124">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="83069-125">Это позволяет заданному пути на сервере запустить синхронизацию файлов с другими конечными точками в группе "Синхронизация".</span><span class="sxs-lookup"><span data-stu-id="83069-125">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="83069-126">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="83069-126">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="83069-127">Эта команда создает новую службу синхронизации хранилища в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83069-127">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="83069-128">Регистрация — AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="83069-128">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="83069-129">Эта команда регистрирует сервер для службы синхронизации хранилища, который создает отношение доверия.</span><span class="sxs-lookup"><span data-stu-id="83069-129">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="83069-130">Вы можете использовать PowerShell или портал Azure для настройки синхронизации на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="83069-130">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="83069-131">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="83069-131">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="83069-132">Эта команда удалит указанную облачную конечную точку из группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="83069-132">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="83069-133">Без хотя бы одной конечной точки облака нельзя синхронизировать другие конечные точки сервера в этой группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="83069-133">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="83069-134">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="83069-134">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="83069-135">Эта команда удалит указанную группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="83069-135">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="83069-136">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="83069-136">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="83069-137">Эта команда удалит указанную конечную точку сервера.</span><span class="sxs-lookup"><span data-stu-id="83069-137">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="83069-138">Синхронизация с этим расположением будет немедленно остановлена.</span><span class="sxs-lookup"><span data-stu-id="83069-138">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="83069-139">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="83069-139">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="83069-140">Эта команда удалит указанную службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="83069-140">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="83069-141">Сброс — AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="83069-141">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="83069-142">Используется только для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="83069-142">Use for troubleshooting only.</span></span> <span data-ttu-id="83069-143">Эта команда выполняет откат сертификата сервера синхронизации хранилища, используемого для описания удостоверения сервера для службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="83069-143">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="83069-144">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="83069-144">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="83069-145">Эта команда позволяет вносить изменения в регулируемых параметрах конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="83069-145">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="83069-146">Отмена регистрации — AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="83069-146">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="83069-147">Предупреждение: Отмена регистрации сервера приводит к каскадному удалению всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="83069-147">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="83069-148">Эта команда отменит регистрацию сервера в службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="83069-148">This command will unregister a server from it's storage sync service.</span></span>