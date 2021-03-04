---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 40ac27339faf2915ccc88c3bbd5f0a39581af743
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955544"
---
# <span data-ttu-id="12574-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="12574-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="12574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12574-102">SYNOPSIS</span></span>
<span data-ttu-id="12574-103">Обновление уровня надежности (VMSKU) типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="12574-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="12574-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="12574-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12574-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12574-105">DESCRIPTION</span></span>
<span data-ttu-id="12574-106">Используйте **update-AzServiceFabricDurability** для обновления надежности или SKU кластера.</span><span class="sxs-lookup"><span data-stu-id="12574-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="12574-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="12574-107">EXAMPLES</span></span>

### <span data-ttu-id="12574-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="12574-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="12574-109">Эта команда изменяет уровень надежности уровня NodeType "nt1" на silver.</span><span class="sxs-lookup"><span data-stu-id="12574-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="12574-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12574-110">PARAMETERS</span></span>

### <span data-ttu-id="12574-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12574-111">-DefaultProfile</span></span>
<span data-ttu-id="12574-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12574-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12574-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="12574-113">-DurabilityLevel</span></span>
<span data-ttu-id="12574-114">Укажите уровень надежности.</span><span class="sxs-lookup"><span data-stu-id="12574-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12574-115">-Name</span><span class="sxs-lookup"><span data-stu-id="12574-115">-Name</span></span>
<span data-ttu-id="12574-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="12574-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12574-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="12574-117">-NodeType</span></span>
<span data-ttu-id="12574-118">Укажите имя типа узла "Сервисная ткань".</span><span class="sxs-lookup"><span data-stu-id="12574-118">Specify Service Fabric node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12574-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12574-119">-ResourceGroupName</span></span>
<span data-ttu-id="12574-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12574-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12574-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="12574-121">-Sku</span></span>
<span data-ttu-id="12574-122">Укажите SKU типа узла.</span><span class="sxs-lookup"><span data-stu-id="12574-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12574-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12574-123">-Confirm</span></span>
<span data-ttu-id="12574-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="12574-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12574-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12574-125">-WhatIf</span></span>
<span data-ttu-id="12574-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12574-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12574-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="12574-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12574-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12574-128">CommonParameters</span></span>
<span data-ttu-id="12574-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12574-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12574-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12574-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12574-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12574-131">INPUTS</span></span>

### <span data-ttu-id="12574-132">System.String</span><span class="sxs-lookup"><span data-stu-id="12574-132">System.String</span></span>

### <span data-ttu-id="12574-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="12574-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="12574-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12574-134">OUTPUTS</span></span>

### <span data-ttu-id="12574-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="12574-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="12574-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="12574-136">NOTES</span></span>

## <span data-ttu-id="12574-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12574-137">RELATED LINKS</span></span>
