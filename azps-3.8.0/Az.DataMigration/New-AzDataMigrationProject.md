---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: beed4ef06d567250fefa8cef86da133447a9f20c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911889"
---
# <span data-ttu-id="26000-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="26000-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="26000-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26000-102">SYNOPSIS</span></span>
<span data-ttu-id="26000-103">Создание нового проекта службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="26000-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="26000-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26000-104">SYNTAX</span></span>

### <span data-ttu-id="26000-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26000-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26000-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26000-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26000-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26000-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26000-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26000-108">DESCRIPTION</span></span>
<span data-ttu-id="26000-109">Командлет New-AzDataMigrationProject создает новый проект службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="26000-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="26000-110">Этот командлет принимает все необходимые параметры, такие как имя группы ресурсов Azure, имя службы миграции данных Azure, в которой нужно создать новый проект, область, в которой нужно создать проект, уникальное имя нового проекта, объекты исходного и целевого соединения и объект целевого типа в качестве входных данных для переносимого списка.</span><span class="sxs-lookup"><span data-stu-id="26000-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="26000-111">Используйте командлет New-AzDataMigrationConnectionInfo, чтобы создать новый объект ConnectionInfo как для исходного, так и для целевого соединения.</span><span class="sxs-lookup"><span data-stu-id="26000-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="26000-112">Список Microsoft. Azure. Management. Migration. Models. DatabaseInfo является ожидаемым для выбранных баз данных; Этот объект можно создать с помощью New-AzDataMigrationDatabaseInfo командлета.</span><span class="sxs-lookup"><span data-stu-id="26000-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="26000-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26000-113">EXAMPLES</span></span>

### <span data-ttu-id="26000-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26000-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="26000-115">В приведенном выше примере показано, как создать новый проект с именем MyDMSProject, размещенный в центральной области US в экземпляре службы миграции баз данных Azure с именем TestService.</span><span class="sxs-lookup"><span data-stu-id="26000-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="26000-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26000-116">PARAMETERS</span></span>

### <span data-ttu-id="26000-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="26000-117">-DatabaseInfo</span></span>
<span data-ttu-id="26000-118">Сведения о базе данных.</span><span class="sxs-lookup"><span data-stu-id="26000-118">Database Infos.</span></span>

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

### <span data-ttu-id="26000-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26000-119">-DefaultProfile</span></span>
<span data-ttu-id="26000-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26000-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26000-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26000-121">-InputObject</span></span>
<span data-ttu-id="26000-122">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="26000-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="26000-123">-Location</span><span class="sxs-lookup"><span data-stu-id="26000-123">-Location</span></span>
<span data-ttu-id="26000-124">Расположение экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="26000-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="26000-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26000-125">-Name</span></span>
<span data-ttu-id="26000-126">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="26000-126">The name of the project.</span></span>

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

### <span data-ttu-id="26000-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26000-127">-ResourceGroupName</span></span>
<span data-ttu-id="26000-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26000-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="26000-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26000-129">-ResourceId</span></span>
<span data-ttu-id="26000-130">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="26000-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="26000-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="26000-131">-ServiceName</span></span>
<span data-ttu-id="26000-132">Имя экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="26000-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="26000-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="26000-133">-SourceConnection</span></span>
<span data-ttu-id="26000-134">Сведения о подключении к источнику.</span><span class="sxs-lookup"><span data-stu-id="26000-134">Source Connection Info.</span></span>

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

### <span data-ttu-id="26000-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="26000-135">-SourceType</span></span>
<span data-ttu-id="26000-136">Тип исходной платформы для проекта.</span><span class="sxs-lookup"><span data-stu-id="26000-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="26000-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="26000-137">-TargetConnection</span></span>
<span data-ttu-id="26000-138">Сведения о целевом подключении.</span><span class="sxs-lookup"><span data-stu-id="26000-138">Target connection information.</span></span>

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

### <span data-ttu-id="26000-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="26000-139">-TargetType</span></span>
<span data-ttu-id="26000-140">Тип целевой платформы для Project.</span><span class="sxs-lookup"><span data-stu-id="26000-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="26000-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26000-141">-Confirm</span></span>
<span data-ttu-id="26000-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26000-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26000-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26000-143">-WhatIf</span></span>
<span data-ttu-id="26000-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26000-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26000-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26000-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26000-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26000-146">CommonParameters</span></span>
<span data-ttu-id="26000-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26000-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26000-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26000-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26000-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26000-149">INPUTS</span></span>

### <span data-ttu-id="26000-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="26000-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="26000-151">System. String</span><span class="sxs-lookup"><span data-stu-id="26000-151">System.String</span></span>

## <span data-ttu-id="26000-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26000-152">OUTPUTS</span></span>

### <span data-ttu-id="26000-153">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="26000-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="26000-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="26000-154">NOTES</span></span>

## <span data-ttu-id="26000-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26000-155">RELATED LINKS</span></span>
