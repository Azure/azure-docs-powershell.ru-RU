---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 1c62c637324f19088dfffcfb4c8defae0a056b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562120"
---
# <span data-ttu-id="eeec6-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="eeec6-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="eeec6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eeec6-102">SYNOPSIS</span></span>
<span data-ttu-id="eeec6-103">Обновите уровень устойчивости или VmSku типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="eeec6-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeec6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eeec6-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeec6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eeec6-105">DESCRIPTION</span></span>
<span data-ttu-id="eeec6-106">С помощью **Update-AzureRmServiceFabricDurability** обновите устойчивость или SKU кластера.</span><span class="sxs-lookup"><span data-stu-id="eeec6-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="eeec6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eeec6-107">EXAMPLES</span></span>

### <span data-ttu-id="eeec6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eeec6-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="eeec6-109">Эта команда изменяет уровень устойчивости NodeType "NT1" на "серебр.".</span><span class="sxs-lookup"><span data-stu-id="eeec6-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="eeec6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eeec6-110">PARAMETERS</span></span>

### <span data-ttu-id="eeec6-111">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="eeec6-111">-DurabilityLevel</span></span>
<span data-ttu-id="eeec6-112">Укажите уровень устойчивости.</span><span class="sxs-lookup"><span data-stu-id="eeec6-112">Specify durability level.</span></span>

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

### <span data-ttu-id="eeec6-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eeec6-113">-Name</span></span>
<span data-ttu-id="eeec6-114">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="eeec6-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="eeec6-115">-NodeType</span><span class="sxs-lookup"><span data-stu-id="eeec6-115">-NodeType</span></span>
<span data-ttu-id="eeec6-116">Укажите имя типа узла фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="eeec6-116">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="eeec6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeec6-117">-ResourceGroupName</span></span>
<span data-ttu-id="eeec6-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eeec6-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="eeec6-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="eeec6-119">-Sku</span></span>
<span data-ttu-id="eeec6-120">Укажите номер SKU для типа узла.</span><span class="sxs-lookup"><span data-stu-id="eeec6-120">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="eeec6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eeec6-121">-Confirm</span></span>
<span data-ttu-id="eeec6-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eeec6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeec6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeec6-123">-WhatIf</span></span>
<span data-ttu-id="eeec6-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eeec6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eeec6-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eeec6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeec6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeec6-126">-DefaultProfile</span></span>
<span data-ttu-id="eeec6-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eeec6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeec6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeec6-128">CommonParameters</span></span>
<span data-ttu-id="eeec6-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eeec6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeec6-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeec6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeec6-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eeec6-131">INPUTS</span></span>

### <span data-ttu-id="eeec6-132">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="eeec6-132">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="eeec6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="eeec6-133">System.String</span></span>

## <span data-ttu-id="eeec6-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eeec6-134">OUTPUTS</span></span>

### <span data-ttu-id="eeec6-135">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="eeec6-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="eeec6-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="eeec6-136">NOTES</span></span>

## <span data-ttu-id="eeec6-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eeec6-137">RELATED LINKS</span></span>

