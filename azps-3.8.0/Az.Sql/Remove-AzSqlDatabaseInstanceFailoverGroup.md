---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073197"
---
# <span data-ttu-id="a28d9-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a28d9-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="a28d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a28d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a28d9-103">Удаляет группу отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a28d9-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="a28d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a28d9-104">SYNTAX</span></span>

### <span data-ttu-id="a28d9-105">RemoveIFGDefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a28d9-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a28d9-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="a28d9-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a28d9-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="a28d9-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a28d9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a28d9-108">DESCRIPTION</span></span>
<span data-ttu-id="a28d9-109">Эта команда удаляет группу отработки отказа для экземпляра с указанным именем, оставляя все базы данных неизменными.</span><span class="sxs-lookup"><span data-stu-id="a28d9-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="a28d9-110">Конечная точка прослушивателя будет отменена из DNS.</span><span class="sxs-lookup"><span data-stu-id="a28d9-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="a28d9-111">Для выполнения команды следует использовать первичный регион для группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a28d9-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="a28d9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a28d9-112">EXAMPLES</span></span>

### <span data-ttu-id="a28d9-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a28d9-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="a28d9-114">Удаление группы отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a28d9-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="a28d9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a28d9-115">PARAMETERS</span></span>

### <span data-ttu-id="a28d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28d9-116">-DefaultProfile</span></span>
<span data-ttu-id="a28d9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a28d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a28d9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a28d9-118">-Force</span></span>
<span data-ttu-id="a28d9-119">Пропустить предупреждающее сообщение для выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="a28d9-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="a28d9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a28d9-120">-InputObject</span></span>
<span data-ttu-id="a28d9-121">Объект группы для отработки отказа экземпляра, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a28d9-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a28d9-122">-Location</span><span class="sxs-lookup"><span data-stu-id="a28d9-122">-Location</span></span>
<span data-ttu-id="a28d9-123">Имя локальной области, из которой извлекается группа отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a28d9-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet, RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28d9-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a28d9-124">-Name</span></span>
<span data-ttu-id="a28d9-125">Имя удаляемой группы отработки отказа для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a28d9-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28d9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a28d9-126">-PassThru</span></span>
<span data-ttu-id="a28d9-127">Указывает, следует ли передавать результаты выполнения командлетов.</span><span class="sxs-lookup"><span data-stu-id="a28d9-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="a28d9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a28d9-128">-ResourceGroupName</span></span>
<span data-ttu-id="a28d9-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a28d9-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28d9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a28d9-130">-ResourceId</span></span>
<span data-ttu-id="a28d9-131">Идентификатор ресурса группы отработки отказа для удаления экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a28d9-131">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a28d9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a28d9-132">-Confirm</span></span>
<span data-ttu-id="a28d9-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a28d9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a28d9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a28d9-134">-WhatIf</span></span>
<span data-ttu-id="a28d9-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a28d9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a28d9-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a28d9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a28d9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28d9-137">CommonParameters</span></span>
<span data-ttu-id="a28d9-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a28d9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28d9-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a28d9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28d9-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a28d9-140">INPUTS</span></span>

### <span data-ttu-id="a28d9-141">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="a28d9-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="a28d9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a28d9-142">System.String</span></span>

## <span data-ttu-id="a28d9-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a28d9-143">OUTPUTS</span></span>

### <span data-ttu-id="a28d9-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="a28d9-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="a28d9-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="a28d9-145">NOTES</span></span>

## <span data-ttu-id="a28d9-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a28d9-146">RELATED LINKS</span></span>
