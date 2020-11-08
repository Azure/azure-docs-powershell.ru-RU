---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249605"
---
# <span data-ttu-id="ebf4b-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="ebf4b-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="ebf4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebf4b-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf4b-103">Обновите уровень устойчивости или VmSku типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="ebf4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebf4b-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebf4b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebf4b-105">DESCRIPTION</span></span>
<span data-ttu-id="ebf4b-106">С помощью **Update-AzServiceFabricDurability** обновите устойчивость или SKU кластера.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="ebf4b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebf4b-107">EXAMPLES</span></span>

### <span data-ttu-id="ebf4b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebf4b-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="ebf4b-109">Эта команда изменяет уровень устойчивости NodeType "NT1" на "серебр.".</span><span class="sxs-lookup"><span data-stu-id="ebf4b-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="ebf4b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebf4b-110">PARAMETERS</span></span>

### <span data-ttu-id="ebf4b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf4b-111">-DefaultProfile</span></span>
<span data-ttu-id="ebf4b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebf4b-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ebf4b-113">-DurabilityLevel</span></span>
<span data-ttu-id="ebf4b-114">Укажите уровень устойчивости.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-114">Specify durability level.</span></span>

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

### <span data-ttu-id="ebf4b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebf4b-115">-Name</span></span>
<span data-ttu-id="ebf4b-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ebf4b-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ebf4b-117">-NodeType</span></span>
<span data-ttu-id="ebf4b-118">Укажите имя типа узла фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="ebf4b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf4b-119">-ResourceGroupName</span></span>
<span data-ttu-id="ebf4b-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ebf4b-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="ebf4b-121">-Sku</span></span>
<span data-ttu-id="ebf4b-122">Укажите номер SKU для типа узла.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="ebf4b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebf4b-123">-Confirm</span></span>
<span data-ttu-id="ebf4b-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebf4b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebf4b-125">-WhatIf</span></span>
<span data-ttu-id="ebf4b-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebf4b-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebf4b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf4b-128">CommonParameters</span></span>
<span data-ttu-id="ebf4b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebf4b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf4b-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebf4b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf4b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebf4b-131">INPUTS</span></span>

### <span data-ttu-id="ebf4b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ebf4b-132">System.String</span></span>

### <span data-ttu-id="ebf4b-133">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ebf4b-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="ebf4b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebf4b-134">OUTPUTS</span></span>

### <span data-ttu-id="ebf4b-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="ebf4b-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ebf4b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebf4b-136">NOTES</span></span>

## <span data-ttu-id="ebf4b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebf4b-137">RELATED LINKS</span></span>
