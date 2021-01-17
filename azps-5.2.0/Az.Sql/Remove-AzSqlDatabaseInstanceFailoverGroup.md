---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399788"
---
# <span data-ttu-id="e0eef-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e0eef-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="e0eef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0eef-102">SYNOPSIS</span></span>
<span data-ttu-id="e0eef-103">Удаляет группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="e0eef-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="e0eef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0eef-104">SYNTAX</span></span>

### <span data-ttu-id="e0eef-105">RemoveIFGDefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0eef-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0eef-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0eef-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0eef-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="e0eef-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0eef-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0eef-108">DESCRIPTION</span></span>
<span data-ttu-id="e0eef-109">Эта команда удаляет группу отбойных экземпляров с указанным именем, оставляя все базы данных без изменений.</span><span class="sxs-lookup"><span data-stu-id="e0eef-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="e0eef-110">Конечная точка будет отрегистрирована из DNS.</span><span class="sxs-lookup"><span data-stu-id="e0eef-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="e0eef-111">Для выполнения команды следует использовать основную область группы отбойных команд экземпляров.</span><span class="sxs-lookup"><span data-stu-id="e0eef-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="e0eef-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0eef-112">EXAMPLES</span></span>

### <span data-ttu-id="e0eef-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0eef-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="e0eef-114">Удалите группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="e0eef-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="e0eef-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0eef-115">PARAMETERS</span></span>

### <span data-ttu-id="e0eef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0eef-116">-DefaultProfile</span></span>
<span data-ttu-id="e0eef-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0eef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0eef-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e0eef-118">-Force</span></span>
<span data-ttu-id="e0eef-119">Пропустите сообщение с подтверждением выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="e0eef-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="e0eef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0eef-120">-InputObject</span></span>
<span data-ttu-id="e0eef-121">Удаляемая группа отбойных экземпляров</span><span class="sxs-lookup"><span data-stu-id="e0eef-121">The Instance Failover Group object to remove</span></span>

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

### <span data-ttu-id="e0eef-122">-Location</span><span class="sxs-lookup"><span data-stu-id="e0eef-122">-Location</span></span>
<span data-ttu-id="e0eef-123">Имя локального региона, из которого нужно получить группу отбойных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="e0eef-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="e0eef-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e0eef-124">-Name</span></span>
<span data-ttu-id="e0eef-125">Имя группы отбойных экземпляров, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e0eef-125">The name of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="e0eef-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0eef-126">-PassThru</span></span>
<span data-ttu-id="e0eef-127">Указывает, следует ли пройти через вывод выполнения с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0eef-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="e0eef-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0eef-128">-ResourceGroupName</span></span>
<span data-ttu-id="e0eef-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0eef-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="e0eef-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0eef-130">-ResourceId</span></span>
<span data-ttu-id="e0eef-131">ИД ресурса группы отбойных экземпляров, который требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="e0eef-131">The Resource ID of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="e0eef-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0eef-132">-Confirm</span></span>
<span data-ttu-id="e0eef-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e0eef-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0eef-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0eef-134">-WhatIf</span></span>
<span data-ttu-id="e0eef-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0eef-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0eef-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e0eef-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0eef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0eef-137">CommonParameters</span></span>
<span data-ttu-id="e0eef-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0eef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0eef-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0eef-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0eef-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0eef-140">INPUTS</span></span>

### <span data-ttu-id="e0eef-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e0eef-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="e0eef-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e0eef-142">System.String</span></span>

## <span data-ttu-id="e0eef-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0eef-143">OUTPUTS</span></span>

### <span data-ttu-id="e0eef-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="e0eef-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="e0eef-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0eef-145">NOTES</span></span>

## <span data-ttu-id="e0eef-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0eef-146">RELATED LINKS</span></span>
