---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 8352f7a63e40986e27c4b521dca58aaf003679bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568178"
---
# <span data-ttu-id="348d8-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="348d8-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="348d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="348d8-102">SYNOPSIS</span></span>
<span data-ttu-id="348d8-103">Создание и запуск задачи миграции данных в службе миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="348d8-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="348d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="348d8-104">SYNTAX</span></span>

### <span data-ttu-id="348d8-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="348d8-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="348d8-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="348d8-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="348d8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="348d8-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="348d8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="348d8-108">DESCRIPTION</span></span>
<span data-ttu-id="348d8-109">Командлет New-AzureRmDataMigrationTask создает задачу миграции данных.</span><span class="sxs-lookup"><span data-stu-id="348d8-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="348d8-110">Этот командлет принимает параметры для перечислителя типов задач, группы ресурсов Azure, имени связанной службы миграции баз данных Azure и Project.</span><span class="sxs-lookup"><span data-stu-id="348d8-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="348d8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="348d8-111">EXAMPLES</span></span>

### <span data-ttu-id="348d8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="348d8-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```

<span data-ttu-id="348d8-113">В этом примере показано, как создать новую задачу миграции данных с именем MyMigrationTask в проекте с именем myDMSProject и службой с именем TestService.</span><span class="sxs-lookup"><span data-stu-id="348d8-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="348d8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="348d8-114">PARAMETERS</span></span>

### <span data-ttu-id="348d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="348d8-115">-DefaultProfile</span></span>
<span data-ttu-id="348d8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="348d8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="348d8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="348d8-117">-InputObject</span></span>
<span data-ttu-id="348d8-118">Объект PSProject.</span><span class="sxs-lookup"><span data-stu-id="348d8-118">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="348d8-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="348d8-119">-Name</span></span>
<span data-ttu-id="348d8-120">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="348d8-120">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="348d8-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="348d8-121">-ProjectName</span></span>
<span data-ttu-id="348d8-122">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="348d8-122">The name of the project.</span></span>

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

### <span data-ttu-id="348d8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="348d8-123">-ResourceGroupName</span></span>
<span data-ttu-id="348d8-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="348d8-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="348d8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="348d8-125">-ResourceId</span></span>
<span data-ttu-id="348d8-126">Идентификатор ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="348d8-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="348d8-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="348d8-127">-ServiceName</span></span>
<span data-ttu-id="348d8-128">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="348d8-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="348d8-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="348d8-129">-TaskType</span></span>
<span data-ttu-id="348d8-130">Тип задачи.</span><span class="sxs-lookup"><span data-stu-id="348d8-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="348d8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="348d8-131">-Confirm</span></span>
<span data-ttu-id="348d8-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="348d8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="348d8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="348d8-133">-WhatIf</span></span>
<span data-ttu-id="348d8-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="348d8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="348d8-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="348d8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="348d8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348d8-136">CommonParameters</span></span>
<span data-ttu-id="348d8-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="348d8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="348d8-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="348d8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348d8-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="348d8-139">INPUTS</span></span>

### <span data-ttu-id="348d8-140">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="348d8-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="348d8-141">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="348d8-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="348d8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="348d8-142">System.String</span></span>

## <span data-ttu-id="348d8-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="348d8-143">OUTPUTS</span></span>

### <span data-ttu-id="348d8-144">Microsoft. Azure. Commands. Migration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="348d8-144">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="348d8-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="348d8-145">NOTES</span></span>

## <span data-ttu-id="348d8-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="348d8-146">RELATED LINKS</span></span>
