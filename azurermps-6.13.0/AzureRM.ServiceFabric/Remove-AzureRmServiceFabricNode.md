---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: 578210490d92e272e3e4867fb7f96f40a1a39782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568154"
---
# <span data-ttu-id="d10a2-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d10a2-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="d10a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d10a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d10a2-103">Удаление узлов из кластера с определенным типом узла.</span><span class="sxs-lookup"><span data-stu-id="d10a2-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d10a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d10a2-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d10a2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d10a2-105">DESCRIPTION</span></span>
<span data-ttu-id="d10a2-106">С помощью **Remove-AzureRmServiceFabricNode** удалите узлы из кластера определенного типа.</span><span class="sxs-lookup"><span data-stu-id="d10a2-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="d10a2-107">Удаление выполняется только в том случае, если оно соответствует метрикам работоспособности кластера.</span><span class="sxs-lookup"><span data-stu-id="d10a2-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="d10a2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d10a2-108">EXAMPLES</span></span>

### <span data-ttu-id="d10a2-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d10a2-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="d10a2-110">Эта команда удалит 2 узла из NodeType "NT1".</span><span class="sxs-lookup"><span data-stu-id="d10a2-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="d10a2-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d10a2-111">PARAMETERS</span></span>

### <span data-ttu-id="d10a2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d10a2-112">-DefaultProfile</span></span>
<span data-ttu-id="d10a2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d10a2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d10a2-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d10a2-114">-Name</span></span>
<span data-ttu-id="d10a2-115">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="d10a2-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d10a2-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="d10a2-116">-NodeType</span></span>
<span data-ttu-id="d10a2-117">Имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="d10a2-117">Node type name.</span></span>

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

### <span data-ttu-id="d10a2-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="d10a2-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="d10a2-119">Количество узлов, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d10a2-119">Number of nodes to remove.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d10a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d10a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="d10a2-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d10a2-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d10a2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d10a2-122">-Confirm</span></span>
<span data-ttu-id="d10a2-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d10a2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d10a2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d10a2-124">-WhatIf</span></span>
<span data-ttu-id="d10a2-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d10a2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d10a2-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d10a2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d10a2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10a2-127">CommonParameters</span></span>
<span data-ttu-id="d10a2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d10a2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10a2-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d10a2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10a2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d10a2-130">INPUTS</span></span>

### <span data-ttu-id="d10a2-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d10a2-131">System.Int32</span></span>
<span data-ttu-id="d10a2-132">Параметры: NumberOfNodesToRemove (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d10a2-132">Parameters: NumberOfNodesToRemove (ByValue)</span></span>

### <span data-ttu-id="d10a2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d10a2-133">System.String</span></span>
<span data-ttu-id="d10a2-134">Параметры: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d10a2-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="d10a2-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d10a2-135">OUTPUTS</span></span>

### <span data-ttu-id="d10a2-136">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="d10a2-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d10a2-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d10a2-137">NOTES</span></span>

## <span data-ttu-id="d10a2-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d10a2-138">RELATED LINKS</span></span>

[<span data-ttu-id="d10a2-139">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d10a2-139">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
