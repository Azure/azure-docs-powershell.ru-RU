---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 5e9e121e3210510ed073cacfe93d6ec196888db6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991399"
---
# <span data-ttu-id="2b07e-101">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2b07e-101">New-AzDataMigrationTask</span></span>

## <span data-ttu-id="2b07e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b07e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b07e-103">Создание и начало задачи переноса данных в службе миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2b07e-103">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

## <span data-ttu-id="2b07e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2b07e-104">SYNTAX</span></span>

### <span data-ttu-id="2b07e-105">ComponentNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b07e-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b07e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b07e-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b07e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b07e-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b07e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b07e-108">DESCRIPTION</span></span>
<span data-ttu-id="2b07e-109">С New-AzDataMigrationTask создается задача переноса данных.</span><span class="sxs-lookup"><span data-stu-id="2b07e-109">The New-AzDataMigrationTask cmdlet creates data migration task.</span></span> <span data-ttu-id="2b07e-110">Этот cmdlet принимает в качестве входных параметров для enumerator "Тип задачи", "Группа ресурсов Azure", имя связанной службы миграции базы данных Azure и Project.</span><span class="sxs-lookup"><span data-stu-id="2b07e-110">This cmdlet takes in parameters for Task Type enumerator, Azure Resource Group, name of associated Azure Database Migration Service and Project as input.</span></span> 

## <span data-ttu-id="2b07e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2b07e-111">EXAMPLES</span></span>

### <span data-ttu-id="2b07e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b07e-112">Example 1</span></span>
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

<span data-ttu-id="2b07e-113">В этом примере показано, как создать задачу переноса данных с именем MyMigrationTask в проекте myDMSProject и службе TestService.</span><span class="sxs-lookup"><span data-stu-id="2b07e-113">This example script shows how to create a new Data Migration Task named MyMigrationTask in the project named myDMSProject and service named TestService.</span></span> 

## <span data-ttu-id="2b07e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b07e-114">PARAMETERS</span></span>

### <span data-ttu-id="2b07e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b07e-115">-DefaultProfile</span></span>
<span data-ttu-id="2b07e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b07e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b07e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b07e-117">-InputObject</span></span>
<span data-ttu-id="2b07e-118">Объект PSProject.</span><span class="sxs-lookup"><span data-stu-id="2b07e-118">PSProject Object.</span></span>

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

### <span data-ttu-id="2b07e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2b07e-119">-Name</span></span>
<span data-ttu-id="2b07e-120">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="2b07e-120">The name of the task.</span></span>

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

### <span data-ttu-id="2b07e-121">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="2b07e-121">-ProjectName</span></span>
<span data-ttu-id="2b07e-122">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="2b07e-122">The name of the project.</span></span>

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

### <span data-ttu-id="2b07e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b07e-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b07e-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b07e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b07e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b07e-125">-ResourceId</span></span>
<span data-ttu-id="2b07e-126">ИД ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="2b07e-126">Project Resource Id.</span></span>

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

### <span data-ttu-id="2b07e-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2b07e-127">-ServiceName</span></span>
<span data-ttu-id="2b07e-128">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="2b07e-128">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="2b07e-129">-TaskType</span><span class="sxs-lookup"><span data-stu-id="2b07e-129">-TaskType</span></span>
<span data-ttu-id="2b07e-130">Тип задачи.</span><span class="sxs-lookup"><span data-stu-id="2b07e-130">Task Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b07e-131">-MigrationValidation</span><span class="sxs-lookup"><span data-stu-id="2b07e-131">-MigrationValidation</span></span> 
<span data-ttu-id="2b07e-132">Объект ответа задачи по звонку проверки (необязательно, но рекомендуется).</span><span class="sxs-lookup"><span data-stu-id="2b07e-132">Task response object by validation call, optional but recommended.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b07e-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="2b07e-133">-Wait</span></span>
<span data-ttu-id="2b07e-134">Следует ли ждать завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="2b07e-134">Whether to wait for task to finish.</span></span> <span data-ttu-id="2b07e-135">Если флажок установлен, проверяется каждые одну секунду, пока задача не завершится, и пользователь вернется к свойствам задачи, для которых можно проверить выходные данные или ошибки.</span><span class="sxs-lookup"><span data-stu-id="2b07e-135">If the flag is set, checks every one seconds till the task finishes and return to user the task properties where output or error can be inspected.</span></span> 
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b07e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b07e-136">-Confirm</span></span>
<span data-ttu-id="2b07e-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2b07e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b07e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b07e-138">-WhatIf</span></span>
<span data-ttu-id="2b07e-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b07e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b07e-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2b07e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b07e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b07e-141">CommonParameters</span></span>
<span data-ttu-id="2b07e-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b07e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b07e-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b07e-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b07e-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b07e-144">INPUTS</span></span>

### <span data-ttu-id="2b07e-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="2b07e-145">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="2b07e-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2b07e-146">System.String</span></span>

## <span data-ttu-id="2b07e-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2b07e-147">OUTPUTS</span></span>

### <span data-ttu-id="2b07e-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="2b07e-148">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="2b07e-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2b07e-149">NOTES</span></span>

## <span data-ttu-id="2b07e-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b07e-150">RELATED LINKS</span></span>
