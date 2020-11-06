---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationTask.md
ms.openlocfilehash: 5ca6edfa811a1b73cbdaae59e8d3b0e2f76cc15f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563568"
---
# <span data-ttu-id="507e9-101">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="507e9-101">Get-AzureRmDataMigrationTask</span></span>

## <span data-ttu-id="507e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="507e9-102">SYNOPSIS</span></span>
<span data-ttu-id="507e9-103">Извлекает объект PSProjectTask, связанный с задачей миграции службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="507e9-103">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="507e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="507e9-104">SYNTAX</span></span>

### <span data-ttu-id="507e9-105">ListByComponent (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="507e9-105">ListByComponent (Default)</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="507e9-106">ListByInputObject</span><span class="sxs-lookup"><span data-stu-id="507e9-106">ListByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="507e9-107">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="507e9-107">GetByInputObject</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="507e9-108">GetByInputObjectResultType</span><span class="sxs-lookup"><span data-stu-id="507e9-108">GetByInputObjectResultType</span></span>
```
Get-AzureRmDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="507e9-109">ListByResourceId</span><span class="sxs-lookup"><span data-stu-id="507e9-109">ListByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="507e9-110">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="507e9-110">GetByResourceId</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="507e9-111">GetByResourceIdResultType</span><span class="sxs-lookup"><span data-stu-id="507e9-111">GetByResourceIdResultType</span></span>
```
Get-AzureRmDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="507e9-112">GetByComponent</span><span class="sxs-lookup"><span data-stu-id="507e9-112">GetByComponent</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="507e9-113">GetByComponentResultType</span><span class="sxs-lookup"><span data-stu-id="507e9-113">GetByComponentResultType</span></span>
```
Get-AzureRmDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 -Name <String> [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="507e9-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="507e9-114">DESCRIPTION</span></span>
<span data-ttu-id="507e9-115">Командлет Get-AzureRmDataMigrationTask извлекает свойства, связанные с задачей миграции службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="507e9-115">The Get-AzureRmDataMigrationTask cmdlet retrieves the properties associated with an Azure Database Migration Service migration task.</span></span>

## <span data-ttu-id="507e9-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="507e9-116">EXAMPLES</span></span>

### <span data-ttu-id="507e9-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="507e9-117">Example 1</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

<span data-ttu-id="507e9-118">В приведенном выше примере показано, как использовать командлет Get-AzureRmDataMigrationTask для получения свойств, связанных с задачей миграции службы миграции баз данных Azure, на основе имени задачи, переданного в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="507e9-118">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve the properties associated with an Azure Database Migration Service migration task based on task name passed in as input parameter</span></span>

### <span data-ttu-id="507e9-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="507e9-119">Example 2</span></span>
```
PS C:\> Get -AzureRmDataMigrationTask -Project $myProject
```

<span data-ttu-id="507e9-120">В приведенном выше примере показано, как использовать командлет Get-AzureRmDataMigrationTask, чтобы извлечь все задачи миграции, связанные с объектом PSProject, который передается в качестве входного параметра.</span><span class="sxs-lookup"><span data-stu-id="507e9-120">The above example illustrates the use of Get-AzureRmDataMigrationTask cmdlet to retrieve all of the migration tasks associated with PSProject object passed in as input parameter</span></span>

## <span data-ttu-id="507e9-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="507e9-121">PARAMETERS</span></span>

### <span data-ttu-id="507e9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="507e9-122">-DefaultProfile</span></span>
<span data-ttu-id="507e9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="507e9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="507e9-124">-Expand</span><span class="sxs-lookup"><span data-stu-id="507e9-124">-Expand</span></span>
<span data-ttu-id="507e9-125">Развернуть вывод</span><span class="sxs-lookup"><span data-stu-id="507e9-125">Expand output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507e9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="507e9-126">-InputObject</span></span>
<span data-ttu-id="507e9-127">Объект PSProject.</span><span class="sxs-lookup"><span data-stu-id="507e9-127">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="507e9-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="507e9-128">-Name</span></span>
<span data-ttu-id="507e9-129">Имя задачи.</span><span class="sxs-lookup"><span data-stu-id="507e9-129">The name of the task.</span></span>

```yaml
Type: String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507e9-130">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="507e9-130">-ProjectName</span></span>
<span data-ttu-id="507e9-131">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="507e9-131">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507e9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="507e9-132">-ResourceGroupName</span></span>
<span data-ttu-id="507e9-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="507e9-133">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507e9-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="507e9-134">-ResourceId</span></span>
<span data-ttu-id="507e9-135">Идентификатор ресурса проекта.</span><span class="sxs-lookup"><span data-stu-id="507e9-135">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="507e9-136">-ResultType</span><span class="sxs-lookup"><span data-stu-id="507e9-136">-ResultType</span></span>
<span data-ttu-id="507e9-137">Развертывание результатов с данным типом результата.</span><span class="sxs-lookup"><span data-stu-id="507e9-137">Expand output of given result type.</span></span>

```yaml
Type: ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases: 
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507e9-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="507e9-138">-ServiceName</span></span>
<span data-ttu-id="507e9-139">Имя службы миграции данных.</span><span class="sxs-lookup"><span data-stu-id="507e9-139">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="507e9-140">-TaskType</span><span class="sxs-lookup"><span data-stu-id="507e9-140">-TaskType</span></span>
<span data-ttu-id="507e9-141">Фильтрация по TaskType.</span><span class="sxs-lookup"><span data-stu-id="507e9-141">Filter by TaskType.</span></span>

```yaml
Type: TaskTypeEnum
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases: 
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="507e9-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="507e9-142">INPUTS</span></span>

### <span data-ttu-id="507e9-143">Microsoft. Azure. Commands. Migration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="507e9-143">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="507e9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="507e9-144">System.String</span></span>

## <span data-ttu-id="507e9-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="507e9-145">OUTPUTS</span></span>

### <span data-ttu-id="507e9-146">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Migration. Models. PSProjectTask, Microsoft. Azure. Commands. DataCulture, версия = 0.1.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="507e9-146">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="507e9-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="507e9-147">NOTES</span></span>

## <span data-ttu-id="507e9-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="507e9-148">RELATED LINKS</span></span>

