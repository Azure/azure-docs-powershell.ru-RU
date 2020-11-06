---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 9abb97e5006f6572c7a0b08d8d25bcc55906a765
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564571"
---
# <span data-ttu-id="057b0-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="057b0-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="057b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="057b0-102">SYNOPSIS</span></span>
<span data-ttu-id="057b0-103">Создание нового проекта службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="057b0-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="057b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="057b0-104">SYNTAX</span></span>

### <span data-ttu-id="057b0-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="057b0-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="057b0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="057b0-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="057b0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="057b0-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="057b0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="057b0-108">DESCRIPTION</span></span>
<span data-ttu-id="057b0-109">Командлет New-AzureRmDataMigrationProject создает новый проект службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="057b0-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="057b0-110">Этот командлет принимает все необходимые параметры, такие как имя группы ресурсов Azure, имя службы миграции данных Azure, в которой нужно создать новый проект, область, в которой нужно создать проект, уникальное имя нового проекта, объекты исходного и целевого соединения и объект целевого типа в качестве входных данных для переносимого списка.</span><span class="sxs-lookup"><span data-stu-id="057b0-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="057b0-111">Используйте командлет New-AzureRmDataMigrationConnectionInfo, чтобы создать новый объект ConnectionInfo как для исходного, так и для целевого соединения.</span><span class="sxs-lookup"><span data-stu-id="057b0-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="057b0-112">Список Microsoft. Azure. Management. Migration. Models. DatabaseInfo является ожидаемым для выбранных баз данных; Этот объект можно создать с помощью New-AzureRmDataMigrationDatabaseInfo командлета.</span><span class="sxs-lookup"><span data-stu-id="057b0-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="057b0-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="057b0-113">EXAMPLES</span></span>

### <span data-ttu-id="057b0-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="057b0-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="057b0-115">В приведенном выше примере показано, как создать новый проект с именем MyDMSProject, размещенный в центральной области US в экземпляре службы миграции баз данных Azure с именем TestService.</span><span class="sxs-lookup"><span data-stu-id="057b0-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="057b0-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="057b0-116">PARAMETERS</span></span>

### <span data-ttu-id="057b0-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="057b0-117">-DatabaseInfo</span></span>
<span data-ttu-id="057b0-118">Сведения о базе данных.</span><span class="sxs-lookup"><span data-stu-id="057b0-118">Database Infos.</span></span>

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

### <span data-ttu-id="057b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="057b0-119">-DefaultProfile</span></span>
<span data-ttu-id="057b0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="057b0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057b0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="057b0-121">-InputObject</span></span>
<span data-ttu-id="057b0-122">Объект PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="057b0-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="057b0-123">-Location</span><span class="sxs-lookup"><span data-stu-id="057b0-123">-Location</span></span>
<span data-ttu-id="057b0-124">Расположение экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="057b0-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="057b0-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="057b0-125">-Name</span></span>
<span data-ttu-id="057b0-126">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="057b0-126">The name of the project.</span></span>

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

### <span data-ttu-id="057b0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="057b0-127">-ResourceGroupName</span></span>
<span data-ttu-id="057b0-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="057b0-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="057b0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="057b0-129">-ResourceId</span></span>
<span data-ttu-id="057b0-130">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="057b0-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="057b0-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="057b0-131">-ServiceName</span></span>
<span data-ttu-id="057b0-132">Имя экземпляра службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="057b0-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="057b0-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="057b0-133">-SourceConnection</span></span>
<span data-ttu-id="057b0-134">Сведения о подключении к источнику.</span><span class="sxs-lookup"><span data-stu-id="057b0-134">Source Connection Info.</span></span>

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

### <span data-ttu-id="057b0-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="057b0-135">-SourceType</span></span>
<span data-ttu-id="057b0-136">Тип исходной платформы для проекта.</span><span class="sxs-lookup"><span data-stu-id="057b0-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="057b0-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="057b0-137">-TargetConnection</span></span>
<span data-ttu-id="057b0-138">Сведения о целевом подключении.</span><span class="sxs-lookup"><span data-stu-id="057b0-138">Target connection information.</span></span>

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

### <span data-ttu-id="057b0-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="057b0-139">-TargetType</span></span>
<span data-ttu-id="057b0-140">Тип целевой платформы для Project.</span><span class="sxs-lookup"><span data-stu-id="057b0-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="057b0-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="057b0-141">-Confirm</span></span>
<span data-ttu-id="057b0-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="057b0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="057b0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="057b0-143">-WhatIf</span></span>
<span data-ttu-id="057b0-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="057b0-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="057b0-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="057b0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="057b0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="057b0-146">CommonParameters</span></span>
<span data-ttu-id="057b0-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="057b0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="057b0-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="057b0-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="057b0-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="057b0-149">INPUTS</span></span>

### <span data-ttu-id="057b0-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="057b0-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="057b0-151">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="057b0-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="057b0-152">System. String</span><span class="sxs-lookup"><span data-stu-id="057b0-152">System.String</span></span>

## <span data-ttu-id="057b0-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="057b0-153">OUTPUTS</span></span>

### <span data-ttu-id="057b0-154">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="057b0-154">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="057b0-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="057b0-155">NOTES</span></span>

## <span data-ttu-id="057b0-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="057b0-156">RELATED LINKS</span></span>
