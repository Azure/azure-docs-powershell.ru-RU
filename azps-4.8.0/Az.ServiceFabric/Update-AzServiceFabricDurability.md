---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a0da9869ccfdc6b8344240a8367a4c8dfcd2350
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684817"
---
# <span data-ttu-id="b06b2-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="b06b2-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="b06b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b06b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b06b2-103">Обновление уровня надежности (VMSKU) типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="b06b2-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="b06b2-104">При этом также будет обновляться уровень надежности в расширении Service Fabric VM в связанном наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b06b2-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

## <span data-ttu-id="b06b2-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b06b2-105">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b06b2-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b06b2-106">DESCRIPTION</span></span>
<span data-ttu-id="b06b2-107">Используйте **update-AzServiceFabricDurability** для обновления надежности или SKU кластера.</span><span class="sxs-lookup"><span data-stu-id="b06b2-107">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="b06b2-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b06b2-108">EXAMPLES</span></span>

### <span data-ttu-id="b06b2-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b06b2-109">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="b06b2-110">Эта команда изменяет уровень надежности уровня NodeType "nt1" на silver.</span><span class="sxs-lookup"><span data-stu-id="b06b2-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="b06b2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b06b2-111">PARAMETERS</span></span>

### <span data-ttu-id="b06b2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06b2-112">-DefaultProfile</span></span>
<span data-ttu-id="b06b2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b06b2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b06b2-114">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b06b2-114">-DurabilityLevel</span></span>
<span data-ttu-id="b06b2-115">Укажите уровень надежности.</span><span class="sxs-lookup"><span data-stu-id="b06b2-115">Specify durability level.</span></span>

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

### <span data-ttu-id="b06b2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b06b2-116">-Name</span></span>
<span data-ttu-id="b06b2-117">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b06b2-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b06b2-118">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b06b2-118">-NodeType</span></span>
<span data-ttu-id="b06b2-119">Укажите имя типа узла "Сервисная ткань".</span><span class="sxs-lookup"><span data-stu-id="b06b2-119">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="b06b2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b06b2-120">-ResourceGroupName</span></span>
<span data-ttu-id="b06b2-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b06b2-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b06b2-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="b06b2-122">-Sku</span></span>
<span data-ttu-id="b06b2-123">Укажите SKU типа узла.</span><span class="sxs-lookup"><span data-stu-id="b06b2-123">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="b06b2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b06b2-124">-Confirm</span></span>
<span data-ttu-id="b06b2-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b06b2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b06b2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b06b2-126">-WhatIf</span></span>
<span data-ttu-id="b06b2-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b06b2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b06b2-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b06b2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b06b2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06b2-129">CommonParameters</span></span>
<span data-ttu-id="b06b2-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b06b2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06b2-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b06b2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06b2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b06b2-132">INPUTS</span></span>

### <span data-ttu-id="b06b2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b06b2-133">System.String</span></span>

### <span data-ttu-id="b06b2-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b06b2-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="b06b2-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b06b2-135">OUTPUTS</span></span>

### <span data-ttu-id="b06b2-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="b06b2-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b06b2-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b06b2-137">NOTES</span></span>

## <span data-ttu-id="b06b2-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b06b2-138">RELATED LINKS</span></span>
