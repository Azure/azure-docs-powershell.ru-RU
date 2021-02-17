---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: beed4ef06d567250fefa8cef86da133447a9f20c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234636"
---
# <span data-ttu-id="29049-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="29049-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="29049-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29049-102">SYNOPSIS</span></span>
<span data-ttu-id="29049-103">Создает новый проект службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="29049-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="29049-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="29049-104">SYNTAX</span></span>

### <span data-ttu-id="29049-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29049-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29049-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29049-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29049-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29049-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29049-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29049-108">DESCRIPTION</span></span>
<span data-ttu-id="29049-109">С New-AzDataMigrationProject создается проект службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="29049-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="29049-110">Этот cmdlet принимает все необходимые параметры, такие как имя группы ресурсов Azure, имя службы миграции данных Azure, в которой должен быть создан новый проект, регион, в котором будет создан проект, уникальное имя нового проекта, объекты подключения к источнику и целевому типу в качестве входных данных для списка переносимых баз данных.</span><span class="sxs-lookup"><span data-stu-id="29049-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="29049-111">Используйте New-AzDataMigrationConnectionInfo, чтобы создать объект ConnectionInfo для исходных и целевых подключений.</span><span class="sxs-lookup"><span data-stu-id="29049-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="29049-112">Список Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo ожидается для выбранных баз данных; этот объект можно создать с помощью New-AzDataMigrationDatabaseInfo-управления.</span><span class="sxs-lookup"><span data-stu-id="29049-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="29049-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="29049-113">EXAMPLES</span></span>

### <span data-ttu-id="29049-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="29049-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="29049-115">В примере выше показано, как создать проект с именем MyDMSProject в центральной части США в экземпляре службы миграции баз данных Azure с именем TestService.</span><span class="sxs-lookup"><span data-stu-id="29049-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="29049-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29049-116">PARAMETERS</span></span>

### <span data-ttu-id="29049-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="29049-117">-DatabaseInfo</span></span>
<span data-ttu-id="29049-118">"Сведения о базе данных".</span><span class="sxs-lookup"><span data-stu-id="29049-118">Database Infos.</span></span>

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

### <span data-ttu-id="29049-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29049-119">-DefaultProfile</span></span>
<span data-ttu-id="29049-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29049-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29049-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29049-121">-InputObject</span></span>
<span data-ttu-id="29049-122">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="29049-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="29049-123">-Location</span><span class="sxs-lookup"><span data-stu-id="29049-123">-Location</span></span>
<span data-ttu-id="29049-124">Расположение экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="29049-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="29049-125">-Name</span><span class="sxs-lookup"><span data-stu-id="29049-125">-Name</span></span>
<span data-ttu-id="29049-126">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="29049-126">The name of the project.</span></span>

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

### <span data-ttu-id="29049-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29049-127">-ResourceGroupName</span></span>
<span data-ttu-id="29049-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29049-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="29049-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29049-129">-ResourceId</span></span>
<span data-ttu-id="29049-130">DataMigrationService Resource Id.</span><span class="sxs-lookup"><span data-stu-id="29049-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="29049-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="29049-131">-ServiceName</span></span>
<span data-ttu-id="29049-132">Имя экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="29049-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="29049-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="29049-133">-SourceConnection</span></span>
<span data-ttu-id="29049-134">Сведения об источнике подключения.</span><span class="sxs-lookup"><span data-stu-id="29049-134">Source Connection Info.</span></span>

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

### <span data-ttu-id="29049-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="29049-135">-SourceType</span></span>
<span data-ttu-id="29049-136">Исходный тип платформы для project.</span><span class="sxs-lookup"><span data-stu-id="29049-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="29049-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="29049-137">-TargetConnection</span></span>
<span data-ttu-id="29049-138">Сведения о целевом под соединении.</span><span class="sxs-lookup"><span data-stu-id="29049-138">Target connection information.</span></span>

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

### <span data-ttu-id="29049-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="29049-139">-TargetType</span></span>
<span data-ttu-id="29049-140">Целевой тип платформы для project.</span><span class="sxs-lookup"><span data-stu-id="29049-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="29049-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29049-141">-Confirm</span></span>
<span data-ttu-id="29049-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="29049-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29049-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29049-143">-WhatIf</span></span>
<span data-ttu-id="29049-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29049-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29049-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="29049-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29049-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29049-146">CommonParameters</span></span>
<span data-ttu-id="29049-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29049-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29049-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29049-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29049-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29049-149">INPUTS</span></span>

### <span data-ttu-id="29049-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="29049-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="29049-151">System.String</span><span class="sxs-lookup"><span data-stu-id="29049-151">System.String</span></span>

## <span data-ttu-id="29049-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="29049-152">OUTPUTS</span></span>

### <span data-ttu-id="29049-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="29049-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="29049-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="29049-154">NOTES</span></span>

## <span data-ttu-id="29049-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29049-155">RELATED LINKS</span></span>
