---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077541"
---
# <span data-ttu-id="54f03-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="54f03-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="54f03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54f03-102">SYNOPSIS</span></span>
<span data-ttu-id="54f03-103">Прекращает выполнение операций управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="54f03-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="54f03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54f03-104">SYNTAX</span></span>

### <span data-ttu-id="54f03-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54f03-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54f03-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f03-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54f03-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f03-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54f03-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54f03-108">DESCRIPTION</span></span>
<span data-ttu-id="54f03-109">Командлет Stop-AzSqlInstanceOperation прекращает операцию с указанным именем операции в управляемом экземпляре SQL.</span><span class="sxs-lookup"><span data-stu-id="54f03-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="54f03-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54f03-110">EXAMPLES</span></span>

### <span data-ttu-id="54f03-111">Пример 1: получение определенной операции</span><span class="sxs-lookup"><span data-stu-id="54f03-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="54f03-112">Эта команда останавливает операцию с именем "d0f5bef5-e2b1-4ef8-bb42-2e54073874f9" в управляемом экземпляре SQL.</span><span class="sxs-lookup"><span data-stu-id="54f03-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="54f03-113">Пример 2: использование идентификатора ресурса операции</span><span class="sxs-lookup"><span data-stu-id="54f03-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="54f03-114">Эта команда останавливает операцию с идентификатором ресурса $managedInstanceOperation. ID.</span><span class="sxs-lookup"><span data-stu-id="54f03-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="54f03-115">Пример 3: использование объекта Operation</span><span class="sxs-lookup"><span data-stu-id="54f03-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="54f03-116">Эта команда останавливает операцию с объектом $managedInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="54f03-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="54f03-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54f03-117">PARAMETERS</span></span>

### <span data-ttu-id="54f03-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f03-118">-DefaultProfile</span></span>
<span data-ttu-id="54f03-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54f03-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54f03-120">-Force</span><span class="sxs-lookup"><span data-stu-id="54f03-120">-Force</span></span>
<span data-ttu-id="54f03-121">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="54f03-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="54f03-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54f03-122">-InputObject</span></span>
<span data-ttu-id="54f03-123">Операция отмены</span><span class="sxs-lookup"><span data-stu-id="54f03-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54f03-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="54f03-124">-ManagedInstanceName</span></span>
<span data-ttu-id="54f03-125">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="54f03-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f03-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54f03-126">-Name</span></span>
<span data-ttu-id="54f03-127">Имя операции.</span><span class="sxs-lookup"><span data-stu-id="54f03-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f03-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54f03-128">-ResourceGroupName</span></span>
<span data-ttu-id="54f03-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54f03-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f03-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54f03-130">-ResourceId</span></span>
<span data-ttu-id="54f03-131">Идентификатор ресурса для объекта Operations, который нужно остановить</span><span class="sxs-lookup"><span data-stu-id="54f03-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f03-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54f03-132">-Confirm</span></span>
<span data-ttu-id="54f03-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54f03-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54f03-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54f03-134">-WhatIf</span></span>
<span data-ttu-id="54f03-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54f03-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54f03-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54f03-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54f03-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f03-137">CommonParameters</span></span>
<span data-ttu-id="54f03-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54f03-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f03-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54f03-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f03-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54f03-140">INPUTS</span></span>

### <span data-ttu-id="54f03-141">System. String</span><span class="sxs-lookup"><span data-stu-id="54f03-141">System.String</span></span>

### <span data-ttu-id="54f03-142">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="54f03-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="54f03-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54f03-143">OUTPUTS</span></span>

### <span data-ttu-id="54f03-144">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="54f03-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="54f03-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="54f03-145">NOTES</span></span>

## <span data-ttu-id="54f03-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54f03-146">RELATED LINKS</span></span>
