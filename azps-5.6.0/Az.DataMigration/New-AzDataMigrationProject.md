---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: 158ae87c636f0ecf8b8c78d2a6d380640ff49677
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972035"
---
# <span data-ttu-id="f5fa8-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="f5fa8-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="f5fa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="f5fa8-103">Создает новый проект службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="f5fa8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5fa8-104">SYNTAX</span></span>

### <span data-ttu-id="f5fa8-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5fa8-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5fa8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5fa8-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5fa8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5fa8-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5fa8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5fa8-108">DESCRIPTION</span></span>
<span data-ttu-id="f5fa8-109">С New-AzDataMigrationProject создается проект службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="f5fa8-110">Этот cmdlet принимает все необходимые параметры, такие как имя группы ресурсов Azure, имя службы миграции данных Azure, в которой должен быть создан новый проект, регион, в котором будет создан проект, уникальное имя нового проекта, объекты подключения к источнику и целевому типу в качестве входных данных для списка переносимых баз данных.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="f5fa8-111">Используйте New-AzDataMigrationConnectionInfo, чтобы создать объект ConnectionInfo для исходных и целевых подключений.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="f5fa8-112">Список Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo ожидается для выбранных баз данных; этот объект можно создать с помощью New-AzDataMigrationDatabaseInfo-управления.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="f5fa8-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5fa8-113">EXAMPLES</span></span>

### <span data-ttu-id="f5fa8-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f5fa8-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="f5fa8-115">В примере выше показано, как создать проект с именем MyDMSProject в центральной части США в экземпляре службы миграции баз данных Azure с именем TestService.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="f5fa8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5fa8-116">PARAMETERS</span></span>

### <span data-ttu-id="f5fa8-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="f5fa8-117">-DatabaseInfo</span></span>
<span data-ttu-id="f5fa8-118">"Сведения о базе данных".</span><span class="sxs-lookup"><span data-stu-id="f5fa8-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5fa8-119">-DefaultProfile</span></span>
<span data-ttu-id="f5fa8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5fa8-121">-InputObject</span></span>
<span data-ttu-id="f5fa8-122">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-123">-Location</span><span class="sxs-lookup"><span data-stu-id="f5fa8-123">-Location</span></span>
<span data-ttu-id="f5fa8-124">Расположение экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-124">The location of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f5fa8-125">-Name</span></span>
<span data-ttu-id="f5fa8-126">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5fa8-127">-ResourceGroupName</span></span>
<span data-ttu-id="f5fa8-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5fa8-129">-ResourceId</span></span>
<span data-ttu-id="f5fa8-130">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f5fa8-131">-ServiceName</span></span>
<span data-ttu-id="f5fa8-132">Имя экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-132">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="f5fa8-133">-SourceConnection</span></span>
<span data-ttu-id="f5fa8-134">Сведения об источнике подключения.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="f5fa8-135">-SourceType</span></span>
<span data-ttu-id="f5fa8-136">Исходный тип платформы для project.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-136">Source platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="f5fa8-137">-TargetConnection</span></span>
<span data-ttu-id="f5fa8-138">Сведения о целевом под соединении.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="f5fa8-139">-TargetType</span></span>
<span data-ttu-id="f5fa8-140">Целевой тип платформы для project.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-140">Target platform type for project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5fa8-141">-Confirm</span></span>
<span data-ttu-id="f5fa8-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5fa8-143">-WhatIf</span></span>
<span data-ttu-id="f5fa8-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5fa8-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5fa8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5fa8-146">CommonParameters</span></span>
<span data-ttu-id="f5fa8-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5fa8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5fa8-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5fa8-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5fa8-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5fa8-149">INPUTS</span></span>

### <span data-ttu-id="f5fa8-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f5fa8-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="f5fa8-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f5fa8-151">System.String</span></span>

## <span data-ttu-id="f5fa8-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5fa8-152">OUTPUTS</span></span>

### <span data-ttu-id="f5fa8-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="f5fa8-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="f5fa8-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5fa8-154">NOTES</span></span>

## <span data-ttu-id="f5fa8-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5fa8-155">RELATED LINKS</span></span>
