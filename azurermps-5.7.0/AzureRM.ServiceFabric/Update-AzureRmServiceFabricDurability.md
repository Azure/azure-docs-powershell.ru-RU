---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 9c82f0aab38fb5479f5344166a409b9b32f7447c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566899"
---
# <span data-ttu-id="a1d5f-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="a1d5f-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="a1d5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d5f-103">Обновите уровень устойчивости или VmSku типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1d5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1d5f-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1d5f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1d5f-105">DESCRIPTION</span></span>
<span data-ttu-id="a1d5f-106">С помощью **Update-AzureRmServiceFabricDurability** обновите устойчивость или SKU кластера.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="a1d5f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1d5f-107">EXAMPLES</span></span>

### <span data-ttu-id="a1d5f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1d5f-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="a1d5f-109">Эта команда изменяет уровень устойчивости NodeType "NT1" на "серебр.".</span><span class="sxs-lookup"><span data-stu-id="a1d5f-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="a1d5f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1d5f-110">PARAMETERS</span></span>

### <span data-ttu-id="a1d5f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d5f-111">-DefaultProfile</span></span>
<span data-ttu-id="a1d5f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d5f-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="a1d5f-113">-DurabilityLevel</span></span>
<span data-ttu-id="a1d5f-114">Укажите уровень устойчивости.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-114">Specify durability level.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d5f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1d5f-115">-Name</span></span>
<span data-ttu-id="a1d5f-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d5f-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a1d5f-117">-NodeType</span></span>
<span data-ttu-id="a1d5f-118">Укажите имя типа узла фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-118">Specify Service Fabric node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d5f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d5f-119">-ResourceGroupName</span></span>
<span data-ttu-id="a1d5f-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d5f-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="a1d5f-121">-Sku</span></span>
<span data-ttu-id="a1d5f-122">Укажите номер SKU для типа узла.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-122">Specify the SKU of the node type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d5f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1d5f-123">-Confirm</span></span>
<span data-ttu-id="a1d5f-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d5f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d5f-125">-WhatIf</span></span>
<span data-ttu-id="a1d5f-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1d5f-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d5f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d5f-128">CommonParameters</span></span>
<span data-ttu-id="a1d5f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d5f-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1d5f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d5f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1d5f-131">INPUTS</span></span>

### <span data-ttu-id="a1d5f-132">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="a1d5f-132">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="a1d5f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a1d5f-133">System.String</span></span>

## <span data-ttu-id="a1d5f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1d5f-134">OUTPUTS</span></span>

### <span data-ttu-id="a1d5f-135">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="a1d5f-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="a1d5f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1d5f-136">NOTES</span></span>

## <span data-ttu-id="a1d5f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1d5f-137">RELATED LINKS</span></span>

