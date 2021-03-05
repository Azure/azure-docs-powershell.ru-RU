---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: 0a7874079b7de782fa7471e9087f04fdc3a9e754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967411"
---
# <span data-ttu-id="609b1-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="609b1-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="609b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="609b1-102">SYNOPSIS</span></span>
<span data-ttu-id="609b1-103">Удаляет пул экземпляров Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="609b1-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="609b1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="609b1-104">SYNTAX</span></span>

### <span data-ttu-id="609b1-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="609b1-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="609b1-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="609b1-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="609b1-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="609b1-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="609b1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="609b1-108">DESCRIPTION</span></span>
<span data-ttu-id="609b1-109">С **использованием cmdlet Remove-AzSqlInstancePool** удаляется пул экземпляров Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="609b1-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="609b1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="609b1-110">EXAMPLES</span></span>

### <span data-ttu-id="609b1-111">Пример 1. Удаление пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="609b1-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="609b1-112">Пример 2. Удаление пула экземпляров по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="609b1-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="609b1-113">Пример 3. Удаление пула экземпляров с помощью объекта пула экземпляров</span><span class="sxs-lookup"><span data-stu-id="609b1-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="609b1-114">Эта команда удаляет пул экземпляров с именем instancePool0.</span><span class="sxs-lookup"><span data-stu-id="609b1-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="609b1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="609b1-115">PARAMETERS</span></span>

### <span data-ttu-id="609b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609b1-116">-DefaultProfile</span></span>
<span data-ttu-id="609b1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="609b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="609b1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="609b1-118">-InputObject</span></span>
<span data-ttu-id="609b1-119">Объект пула экземпляров, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="609b1-119">The instance pool object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="609b1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="609b1-120">-Name</span></span>
<span data-ttu-id="609b1-121">Имя пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="609b1-121">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="609b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="609b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="609b1-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="609b1-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="609b1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="609b1-124">-ResourceId</span></span>
<span data-ttu-id="609b1-125">Удаляемый ид пула экземпляров.</span><span class="sxs-lookup"><span data-stu-id="609b1-125">The instance pool resource id to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="609b1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="609b1-126">-Confirm</span></span>
<span data-ttu-id="609b1-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="609b1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="609b1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="609b1-128">-WhatIf</span></span>
<span data-ttu-id="609b1-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="609b1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="609b1-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="609b1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="609b1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609b1-131">CommonParameters</span></span>
<span data-ttu-id="609b1-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="609b1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="609b1-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="609b1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609b1-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="609b1-134">INPUTS</span></span>

### <span data-ttu-id="609b1-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="609b1-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="609b1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="609b1-136">System.String</span></span>

## <span data-ttu-id="609b1-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="609b1-137">OUTPUTS</span></span>

### <span data-ttu-id="609b1-138">System.Object</span><span class="sxs-lookup"><span data-stu-id="609b1-138">System.Object</span></span>
## <span data-ttu-id="609b1-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="609b1-139">NOTES</span></span>

## <span data-ttu-id="609b1-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="609b1-140">RELATED LINKS</span></span>
