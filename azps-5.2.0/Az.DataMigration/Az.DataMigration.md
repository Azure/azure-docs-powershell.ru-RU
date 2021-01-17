---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: 6eb1ccb692f9f57e0d686a26a7c534459118cd19
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327715"
---
# <span data-ttu-id="44a31-101">Модуль Az.DataMigration</span><span class="sxs-lookup"><span data-stu-id="44a31-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="44a31-102">Описание</span><span class="sxs-lookup"><span data-stu-id="44a31-102">Description</span></span>
<span data-ttu-id="44a31-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="44a31-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="44a31-104">Az.DataMigration Cmdlets</span><span class="sxs-lookup"><span data-stu-id="44a31-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="44a31-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="44a31-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="44a31-106">Извлекает свойства проекта миграции базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="44a31-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="44a31-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="44a31-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="44a31-108">Извлекает свойства, связанные с экземпляром службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="44a31-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="44a31-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="44a31-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="44a31-110">Извлекает объект PSProjectTask, связанный с задачей миграции службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="44a31-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="44a31-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="44a31-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="44a31-112">Создает новую команду, которая будет выполняться в существующей задаче DMS.</span><span class="sxs-lookup"><span data-stu-id="44a31-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="44a31-113">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="44a31-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="44a31-114">Создание объекта "Сведения о под соединении", определяющий тип сервера и имя подключения.</span><span class="sxs-lookup"><span data-stu-id="44a31-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="44a31-115">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="44a31-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="44a31-116">Создание объекта DatabaseInfo для службы миграции баз данных Azure, которая определяет источник базы данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="44a31-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="44a31-117">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="44a31-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="44a31-118">Создание объекта FileShare для службы миграции баз данных Azure, в которой указывается локализованная сетевая папка, в которую нужно архивации.</span><span class="sxs-lookup"><span data-stu-id="44a31-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="44a31-119">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="44a31-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="44a31-120">Создает новый проект службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="44a31-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="44a31-121">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="44a31-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="44a31-122">Создает объект ввода базы данных, содержащий сведения об исходных и целевых базах данных для миграции.</span><span class="sxs-lookup"><span data-stu-id="44a31-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="44a31-123">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="44a31-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="44a31-124">Создает новый экземпляр службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="44a31-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="44a31-125">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="44a31-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="44a31-126">Создание информационного объекта базы данных, специального для сценария синхронизации, который будет использоваться для задачи миграции.</span><span class="sxs-lookup"><span data-stu-id="44a31-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="44a31-127">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="44a31-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="44a31-128">Создание и начало задачи переноса данных в службе миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="44a31-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="44a31-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="44a31-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="44a31-130">Удаляет проект службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="44a31-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="44a31-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="44a31-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="44a31-132">Удаляет экземпляр службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="44a31-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="44a31-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="44a31-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="44a31-134">Удаляет задачу службы миграции баз данных Azure из Azure.</span><span class="sxs-lookup"><span data-stu-id="44a31-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="44a31-135">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="44a31-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="44a31-136">Запускает экземпляр службы миграции баз данных Azure в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="44a31-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="44a31-137">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="44a31-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="44a31-138">Остановка экземпляра службы миграции баз данных Azure, которая находится в запущенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="44a31-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="44a31-139">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="44a31-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="44a31-140">Остановка задачи службы миграции баз данных Azure, которая находится в запущенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="44a31-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

