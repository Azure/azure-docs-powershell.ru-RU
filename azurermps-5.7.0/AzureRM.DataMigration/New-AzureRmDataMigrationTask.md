---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationTask.md
ms.openlocfilehash: 1bdf66311acd1b8ff1de43b5ea199d5d0a17c394
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732649"
---
# <span data-ttu-id="a8ce3-101">New-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="a8ce3-101">New-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="a8ce3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ce3-103">Создание и запуск задачи миграции данных в службе миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8ce3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8ce3-104">SYNTAX</span></span>

### <span data-ttu-id="a8ce3-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8ce3-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a8ce3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8ce3-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a8ce3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8ce3-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a8ce3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8ce3-108">DESCRIPTION</span></span>
<span data-ttu-id="a8ce3-109">Командлет New-AzureRmDataMigrationTask создает задачу миграции данных.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-109">The New-AzureRmDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="a8ce3-110">Этот командлет принимает параметры для перечислителя типов задач, группы ресурсов Azure, имени связанной службы миграции данных Azure и проекта в качестве данных.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Data Migration Service and Project as input.</span></span> 

## <span data-ttu-id="a8ce3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8ce3-111">EXAMPLES</span></span>

### <span data-ttu-id="a8ce3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a8ce3-112">Example 1</span></span>
```
PS C:\> New-AzureRmDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs
```
<span data-ttu-id="a8ce3-113">В этом примере показано, как создать новую задачу миграции данных с именем MyMigrationTask в проекте с именем myDMSProject и службой с именем TestService.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="a8ce3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8ce3-114">PARAMETERS</span></span>

### <span data-ttu-id="a8ce3-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8ce3-115">-Confirm</span></span>
<span data-ttu-id="a8ce3-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ce3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ce3-117">-DefaultProfile</span></span>
<span data-ttu-id="a8ce3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8ce3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8ce3-119">-InputObject</span></span>
<span data-ttu-id="a8ce3-120">Объект PSProject.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-120">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ce3-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a8ce3-121">-Name</span></span>
<span data-ttu-id="a8ce3-122">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-122">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ce3-123">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="a8ce3-123">-ProjectName</span></span>
<span data-ttu-id="a8ce3-124">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-124">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ce3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ce3-125">-ResourceGroupName</span></span>
<span data-ttu-id="a8ce3-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ce3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8ce3-127">-ResourceId</span></span>
<span data-ttu-id="a8ce3-128">Идентификатор ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-128">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ce3-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a8ce3-129">-ServiceName</span></span>
<span data-ttu-id="a8ce3-130">Имя службы миграции данных.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-130">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ce3-131">-TaskType</span><span class="sxs-lookup"><span data-stu-id="a8ce3-131">-TaskType</span></span>
<span data-ttu-id="a8ce3-132">Тип задачи.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-132">Task Type.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ce3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ce3-133">-WhatIf</span></span>
<span data-ttu-id="a8ce3-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ce3-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a8ce3-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8ce3-136">INPUTS</span></span>

### <span data-ttu-id="a8ce3-137">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="a8ce3-137">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="a8ce3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a8ce3-138">System.String</span></span>


## <span data-ttu-id="a8ce3-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8ce3-139">OUTPUTS</span></span>

### <span data-ttu-id="a8ce3-140">Microsoft. Azure. Commands. Migration. Models. PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="a8ce3-140">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>


## <span data-ttu-id="a8ce3-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8ce3-141">NOTES</span></span>

## <span data-ttu-id="a8ce3-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8ce3-142">RELATED LINKS</span></span>


