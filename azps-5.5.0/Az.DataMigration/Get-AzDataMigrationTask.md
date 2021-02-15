---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: bcc1c39af722d5f12c333152e8458228f583a842
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211145"
---
# <span data-ttu-id="cf114-101">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="cf114-101">Get-AzDataMigrationTask</span></span>

## <span data-ttu-id="cf114-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf114-102">SYNOPSIS</span></span>
<span data-ttu-id="cf114-103">Извлекает объект PSProjectTask, связанный с задачей миграции службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="cf114-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="cf114-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cf114-104">SYNTAX</span></span>

### <span data-ttu-id="cf114-105">ListByComponent (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf114-105">ListByComponent (Default)</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf114-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="cf114-106">ListByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf114-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="cf114-107">GetByInputObject</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf114-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="cf114-108">GetByInputObjectResultType</span></span>
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf114-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf114-109">ListByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf114-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf114-110">GetByResourceId</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf114-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="cf114-111">GetByResourceIdResultType</span></span>
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf114-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="cf114-112">GetByComponent</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf114-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="cf114-113">GetByComponentResultType</span></span>
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf114-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf114-114">DESCRIPTION</span></span>
<span data-ttu-id="cf114-115">Он Get-AzDataMigrationTask извлекает свойства, связанные с задачей миграции службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="cf114-115">The Get-AzDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="cf114-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cf114-116">EXAMPLES</span></span>

### <span data-ttu-id="cf114-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cf114-117">Example 1</span></span>
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="cf114-118">В примере выше показано использование Get-AzDataMigrationTask для извлечения свойств, связанных с задачей миграции службы миграции баз данных Azure, на основе имени задачи, переданной в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="cf114-118">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="cf114-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cf114-119">Example 2</span></span>
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

<span data-ttu-id="cf114-120">В примере выше показано использование Get-AzDataMigrationTask для получения всех задач миграции, связанных с объектом PSProject, который передается в качестве входного параметра</span><span class="sxs-lookup"><span data-stu-id="cf114-120">The above example illustrates the use of Get-AzDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="cf114-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf114-121">PARAMETERS</span></span>

### <span data-ttu-id="cf114-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf114-122">-DefaultProfile</span></span>
<span data-ttu-id="cf114-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf114-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf114-124">-Развернуть</span><span class="sxs-lookup"><span data-stu-id="cf114-124">-Expand</span></span>
<span data-ttu-id="cf114-125">Развернуть выходные данные</span><span class="sxs-lookup"><span data-stu-id="cf114-125">Expand output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf114-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf114-126">-InputObject</span></span>
<span data-ttu-id="cf114-127">Объект PSProject.</span><span class="sxs-lookup"><span data-stu-id="cf114-127">PSProject Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf114-128">-Name</span><span class="sxs-lookup"><span data-stu-id="cf114-128">-Name</span></span>
<span data-ttu-id="cf114-129">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="cf114-129">The name of the task.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf114-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="cf114-130">-ProjectName</span></span>
<span data-ttu-id="cf114-131">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="cf114-131">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf114-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf114-132">-ResourceGroupName</span></span>
<span data-ttu-id="cf114-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf114-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf114-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf114-134">-ResourceId</span></span>
<span data-ttu-id="cf114-135">ИД ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="cf114-135">Project Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf114-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="cf114-136">-ResultType</span></span>
<span data-ttu-id="cf114-137">Развернуть выходные данные заданного типа результатов.</span><span class="sxs-lookup"><span data-stu-id="cf114-137">Expand output of given result type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf114-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cf114-138">-ServiceName</span></span>
<span data-ttu-id="cf114-139">Имя службы миграции базы данных.</span><span class="sxs-lookup"><span data-stu-id="cf114-139">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf114-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="cf114-140">-TaskType</span></span>
<span data-ttu-id="cf114-141">Фильтрация по типу задач.</span><span class="sxs-lookup"><span data-stu-id="cf114-141">Filter by TaskType.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf114-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf114-142">CommonParameters</span></span>
<span data-ttu-id="cf114-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf114-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf114-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf114-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf114-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf114-145">INPUTS</span></span>

### <span data-ttu-id="cf114-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="cf114-146">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

### <span data-ttu-id="cf114-147">System.String</span><span class="sxs-lookup"><span data-stu-id="cf114-147">System.String</span></span>

## <span data-ttu-id="cf114-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf114-148">OUTPUTS</span></span>

### <span data-ttu-id="cf114-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span><span class="sxs-lookup"><span data-stu-id="cf114-149">Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask</span></span>

## <span data-ttu-id="cf114-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cf114-150">NOTES</span></span>

## <span data-ttu-id="cf114-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf114-151">RELATED LINKS</span></span>
