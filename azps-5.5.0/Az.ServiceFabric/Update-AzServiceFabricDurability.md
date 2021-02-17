---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223132"
---
# <span data-ttu-id="87811-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="87811-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="87811-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87811-102">SYNOPSIS</span></span>
<span data-ttu-id="87811-103">Обновление уровня надежности (VMSKU) типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="87811-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="87811-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="87811-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87811-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87811-105">DESCRIPTION</span></span>
<span data-ttu-id="87811-106">Используйте **update-AzServiceFabricDurability** для обновления надежности или SKU кластера.</span><span class="sxs-lookup"><span data-stu-id="87811-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="87811-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="87811-107">EXAMPLES</span></span>

### <span data-ttu-id="87811-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87811-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="87811-109">Эта команда изменяет уровень надежности nodeType "nt1" на silver.</span><span class="sxs-lookup"><span data-stu-id="87811-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="87811-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87811-110">PARAMETERS</span></span>

### <span data-ttu-id="87811-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87811-111">-DefaultProfile</span></span>
<span data-ttu-id="87811-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87811-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87811-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="87811-113">-DurabilityLevel</span></span>
<span data-ttu-id="87811-114">Укажите уровень надежности.</span><span class="sxs-lookup"><span data-stu-id="87811-114">Specify durability level.</span></span>

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

### <span data-ttu-id="87811-115">-Name</span><span class="sxs-lookup"><span data-stu-id="87811-115">-Name</span></span>
<span data-ttu-id="87811-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="87811-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="87811-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="87811-117">-NodeType</span></span>
<span data-ttu-id="87811-118">Укажите имя типа узла "Сервисная ткань".</span><span class="sxs-lookup"><span data-stu-id="87811-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="87811-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87811-119">-ResourceGroupName</span></span>
<span data-ttu-id="87811-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87811-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="87811-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="87811-121">-Sku</span></span>
<span data-ttu-id="87811-122">Укажите SKU типа узла.</span><span class="sxs-lookup"><span data-stu-id="87811-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="87811-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87811-123">-Confirm</span></span>
<span data-ttu-id="87811-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87811-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87811-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87811-125">-WhatIf</span></span>
<span data-ttu-id="87811-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87811-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87811-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="87811-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87811-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87811-128">CommonParameters</span></span>
<span data-ttu-id="87811-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87811-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87811-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87811-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87811-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87811-131">INPUTS</span></span>

### <span data-ttu-id="87811-132">System.String</span><span class="sxs-lookup"><span data-stu-id="87811-132">System.String</span></span>

### <span data-ttu-id="87811-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="87811-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="87811-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87811-134">OUTPUTS</span></span>

### <span data-ttu-id="87811-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="87811-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="87811-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="87811-136">NOTES</span></span>

## <span data-ttu-id="87811-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87811-137">RELATED LINKS</span></span>
