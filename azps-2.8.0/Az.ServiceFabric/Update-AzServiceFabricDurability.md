---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 283ca228ba44d2ec87cd926d23e0217eb67434eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903726"
---
# <span data-ttu-id="13fb6-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="13fb6-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="13fb6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="13fb6-103">Обновите уровень устойчивости или VmSku типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="13fb6-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="13fb6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13fb6-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13fb6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13fb6-105">DESCRIPTION</span></span>
<span data-ttu-id="13fb6-106">С помощью **Update-AzServiceFabricDurability** обновите устойчивость или SKU кластера.</span><span class="sxs-lookup"><span data-stu-id="13fb6-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="13fb6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13fb6-107">EXAMPLES</span></span>

### <span data-ttu-id="13fb6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="13fb6-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="13fb6-109">Эта команда изменяет уровень устойчивости NodeType "NT1" на "серебр.".</span><span class="sxs-lookup"><span data-stu-id="13fb6-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="13fb6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13fb6-110">PARAMETERS</span></span>

### <span data-ttu-id="13fb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13fb6-111">-DefaultProfile</span></span>
<span data-ttu-id="13fb6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13fb6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13fb6-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="13fb6-113">-DurabilityLevel</span></span>
<span data-ttu-id="13fb6-114">Укажите уровень устойчивости.</span><span class="sxs-lookup"><span data-stu-id="13fb6-114">Specify durability level.</span></span>

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

### <span data-ttu-id="13fb6-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13fb6-115">-Name</span></span>
<span data-ttu-id="13fb6-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="13fb6-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="13fb6-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="13fb6-117">-NodeType</span></span>
<span data-ttu-id="13fb6-118">Укажите имя типа узла фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="13fb6-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="13fb6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13fb6-119">-ResourceGroupName</span></span>
<span data-ttu-id="13fb6-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13fb6-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="13fb6-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="13fb6-121">-Sku</span></span>
<span data-ttu-id="13fb6-122">Укажите номер SKU для типа узла.</span><span class="sxs-lookup"><span data-stu-id="13fb6-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="13fb6-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13fb6-123">-Confirm</span></span>
<span data-ttu-id="13fb6-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13fb6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13fb6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13fb6-125">-WhatIf</span></span>
<span data-ttu-id="13fb6-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13fb6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13fb6-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13fb6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13fb6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13fb6-128">CommonParameters</span></span>
<span data-ttu-id="13fb6-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13fb6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13fb6-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13fb6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13fb6-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13fb6-131">INPUTS</span></span>

### <span data-ttu-id="13fb6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="13fb6-132">System.String</span></span>

### <span data-ttu-id="13fb6-133">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="13fb6-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="13fb6-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13fb6-134">OUTPUTS</span></span>

### <span data-ttu-id="13fb6-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="13fb6-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="13fb6-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="13fb6-136">NOTES</span></span>

## <span data-ttu-id="13fb6-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13fb6-137">RELATED LINKS</span></span>
