---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 99884c23ff99287deb721e3cb76871766cdfa7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568590"
---
# <span data-ttu-id="dc1b9-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="dc1b9-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="dc1b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1b9-103">Создание нового проекта службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc1b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc1b9-104">SYNTAX</span></span>

### <span data-ttu-id="dc1b9-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc1b9-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform>
 [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="dc1b9-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc1b9-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="dc1b9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc1b9-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="dc1b9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc1b9-108">DESCRIPTION</span></span>
<span data-ttu-id="dc1b9-109">Командлет New-AzureRmDataMigrationProject создает новый проект службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="dc1b9-110">Этот командлет принимает все необходимые параметры, такие как имя группы ресурсов Azure, имя службы миграции данных Azure, в которой нужно создать новый проект, область, в которой нужно создать проект, уникальное имя нового проекта, объекты исходного и целевого соединения и объект целевого типа в качестве входных данных для переносимого списка.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="dc1b9-111">Используйте командлет New-AzureRmDataMigrationConnectionInfo, чтобы создать новый объект ConnectionInfo как для исходного, так и для целевого соединения.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="dc1b9-112">Список Microsoft. Azure. Management. Migration. Models. DatabaseInfo является ожидаемым для выбранных баз данных; Этот объект можно создать с помощью New-AzureRmDataMigrationDatabaseInfo командлета.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="dc1b9-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc1b9-113">EXAMPLES</span></span>

### <span data-ttu-id="dc1b9-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc1b9-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="dc1b9-115">В приведенном выше примере показано, как создать новый проект с именем MyDMSProject, размещенный в центральной области US в экземпляре службы миграции баз данных Azure с именем TestService.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>



## <span data-ttu-id="dc1b9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc1b9-116">PARAMETERS</span></span>

### <span data-ttu-id="dc1b9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc1b9-117">-Confirm</span></span>
<span data-ttu-id="dc1b9-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1b9-119">-DatabaseInfo[]</span><span class="sxs-lookup"><span data-stu-id="dc1b9-119">-DatabaseInfo[]</span></span>
<span data-ttu-id="dc1b9-120">Сведения о базе данных</span><span class="sxs-lookup"><span data-stu-id="dc1b9-120">Database information</span></span>

```yaml
Type: DatabaseInfo[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc1b9-121">-DefaultProfile</span></span>
<span data-ttu-id="dc1b9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1b9-123">-Location</span><span class="sxs-lookup"><span data-stu-id="dc1b9-123">-Location</span></span>
<span data-ttu-id="dc1b9-124">Расположение экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1b9-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="dc1b9-125">-ProjectName</span></span>
<span data-ttu-id="dc1b9-126">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-126">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1b9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc1b9-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc1b9-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1b9-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dc1b9-129">-ServiceName</span></span>
<span data-ttu-id="dc1b9-130">Имя экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-130">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1b9-131">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="dc1b9-131">-SourceConnection</span></span>
<span data-ttu-id="dc1b9-132">Сведения о подключении к источнику.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-132">Source Connection Info.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1b9-133">-SourceType</span><span class="sxs-lookup"><span data-stu-id="dc1b9-133">-SourceType</span></span>
<span data-ttu-id="dc1b9-134">Тип исходной платформы для проекта.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-134">Source platform type for project.</span></span>

```yaml
Type: ProjectSourcePlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1b9-135">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="dc1b9-135">-TargetConnection</span></span>
<span data-ttu-id="dc1b9-136">Сведения о целевом подключении.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-136">Target connection information.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1b9-137">-TargetType</span><span class="sxs-lookup"><span data-stu-id="dc1b9-137">-TargetType</span></span>
<span data-ttu-id="dc1b9-138">Тип целевой платформы для Project.</span><span class="sxs-lookup"><span data-stu-id="dc1b9-138">Target platform type for project.</span></span>

```yaml
Type: ProjectTargetPlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="dc1b9-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc1b9-139">OUTPUTS</span></span>

### <span data-ttu-id="dc1b9-140">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="dc1b9-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>


## <span data-ttu-id="dc1b9-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc1b9-141">NOTES</span></span>

## <span data-ttu-id="dc1b9-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc1b9-142">RELATED LINKS</span></span>

