---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: b056e5328c24270df6a95e33b079e7b907f29fa3
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "101685025"
---
# <span data-ttu-id="6ecc1-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="6ecc1-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="6ecc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ecc1-102">SYNOPSIS</span></span>
<span data-ttu-id="6ecc1-103">Обновление уровня надежности (VMSKU) типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="6ecc1-104">При этом также будет обновляться уровень надежности в расширении Service Fabric VM в связанном наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ecc1-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ecc1-105">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ecc1-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ecc1-106">DESCRIPTION</span></span>
<span data-ttu-id="6ecc1-107">Используйте **update-AzureRmServiceFabricDurability** для обновления надежности или SKU кластера.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-107">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="6ecc1-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ecc1-108">EXAMPLES</span></span>

### <span data-ttu-id="6ecc1-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ecc1-109">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="6ecc1-110">Эта команда изменяет уровень надежности уровня NodeType "nt1" на silver.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="6ecc1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ecc1-111">PARAMETERS</span></span>

### <span data-ttu-id="6ecc1-112">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="6ecc1-112">-DurabilityLevel</span></span>
<span data-ttu-id="6ecc1-113">Укажите уровень надежности.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-113">Specify durability level.</span></span>

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

### <span data-ttu-id="6ecc1-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6ecc1-114">-Name</span></span>
<span data-ttu-id="6ecc1-115">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6ecc1-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="6ecc1-116">-NodeType</span></span>
<span data-ttu-id="6ecc1-117">Укажите имя типа узла "Сервисная ткань".</span><span class="sxs-lookup"><span data-stu-id="6ecc1-117">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="6ecc1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ecc1-118">-ResourceGroupName</span></span>
<span data-ttu-id="6ecc1-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6ecc1-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="6ecc1-120">-Sku</span></span>
<span data-ttu-id="6ecc1-121">Укажите SKU типа узла.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-121">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="6ecc1-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ecc1-122">-Confirm</span></span>
<span data-ttu-id="6ecc1-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ecc1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ecc1-124">-WhatIf</span></span>
<span data-ttu-id="6ecc1-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ecc1-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ecc1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ecc1-127">-DefaultProfile</span></span>
<span data-ttu-id="6ecc1-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ecc1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ecc1-129">CommonParameters</span></span>
<span data-ttu-id="6ecc1-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ecc1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ecc1-131">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ecc1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ecc1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ecc1-132">INPUTS</span></span>

### <span data-ttu-id="6ecc1-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="6ecc1-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="6ecc1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6ecc1-134">System.String</span></span>

## <span data-ttu-id="6ecc1-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ecc1-135">OUTPUTS</span></span>

### <span data-ttu-id="6ecc1-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span><span class="sxs-lookup"><span data-stu-id="6ecc1-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="6ecc1-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ecc1-137">NOTES</span></span>

## <span data-ttu-id="6ecc1-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ecc1-138">RELATED LINKS</span></span>

