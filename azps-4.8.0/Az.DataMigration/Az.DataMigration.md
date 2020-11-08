---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: 6eb1ccb692f9f57e0d686a26a7c534459118cd19
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236769"
---
# <span data-ttu-id="2eb2f-101">AZ. модуль миграции</span><span class="sxs-lookup"><span data-stu-id="2eb2f-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="2eb2f-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="2eb2f-102">Description</span></span>
<span data-ttu-id="2eb2f-103">{{Модуль службы миграции Azure}}</span><span class="sxs-lookup"><span data-stu-id="2eb2f-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="2eb2f-104">"Az. командлеты миграции"</span><span class="sxs-lookup"><span data-stu-id="2eb2f-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="2eb2f-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2eb2f-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="2eb2f-106">Извлекает свойства проекта миграции базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="2eb2f-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2eb2f-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="2eb2f-108">Извлекает свойства, связанные с экземпляром службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="2eb2f-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2eb2f-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="2eb2f-110">Извлекает объект PSProjectTask, связанный с задачей миграции службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="2eb2f-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="2eb2f-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="2eb2f-112">Создает новую команду для выполнения в существующей задаче DMS.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="2eb2f-113">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="2eb2f-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="2eb2f-114">Создает новый объект сведений о соединении, указывающий тип сервера и имя для подключения.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="2eb2f-115">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="2eb2f-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="2eb2f-116">Создает объект DatabaseInfo для службы миграции баз данных Azure, указывающий источник базы данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="2eb2f-117">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="2eb2f-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="2eb2f-118">Создает объект общего файлового обмена для службы миграции баз данных Azure, который определяет локальную общую сетевую папке, в которую нужно сделать резервные копии исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="2eb2f-119">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2eb2f-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="2eb2f-120">Создание нового проекта службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="2eb2f-121">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="2eb2f-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="2eb2f-122">Создает объект ввода базы данных, содержащий сведения об исходной и целевой базах данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="2eb2f-123">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2eb2f-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="2eb2f-124">Создание нового экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="2eb2f-125">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="2eb2f-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="2eb2f-126">Создает объект сведений о базе данных, специфичный для сценария синхронизации, который будет использоваться для задачи миграции.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="2eb2f-127">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2eb2f-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="2eb2f-128">Создание и запуск задачи миграции данных в службе миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="2eb2f-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2eb2f-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="2eb2f-130">Удаление проекта службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="2eb2f-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2eb2f-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="2eb2f-132">Удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="2eb2f-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2eb2f-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="2eb2f-134">Удаление задачи службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="2eb2f-135">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2eb2f-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="2eb2f-136">Запускает экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="2eb2f-137">Остановить-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2eb2f-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="2eb2f-138">Останавливает экземпляр службы миграции баз данных Azure, которая находится в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="2eb2f-139">Остановить-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2eb2f-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="2eb2f-140">Останавливает задачу службы миграции баз данных Azure, которая находится в состоянии выполнения.</span><span class="sxs-lookup"><span data-stu-id="2eb2f-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

