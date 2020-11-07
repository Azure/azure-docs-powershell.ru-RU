---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 22aa963f772a87b97a0a64ccdaef5ad6ef004696
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729110"
---
# <span data-ttu-id="262e5-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="262e5-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="262e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="262e5-102">SYNOPSIS</span></span>
<span data-ttu-id="262e5-103">Удаление узлов из кластера с определенным типом узла.</span><span class="sxs-lookup"><span data-stu-id="262e5-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="262e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="262e5-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="262e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="262e5-105">DESCRIPTION</span></span>
<span data-ttu-id="262e5-106">С помощью **Remove-AzServiceFabricNode** удалите узлы из кластера определенного типа.</span><span class="sxs-lookup"><span data-stu-id="262e5-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="262e5-107">Удаление выполняется только в том случае, если оно соответствует метрикам работоспособности кластера.</span><span class="sxs-lookup"><span data-stu-id="262e5-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="262e5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="262e5-108">EXAMPLES</span></span>

### <span data-ttu-id="262e5-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="262e5-109">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="262e5-110">Эта команда удалит 2 узла из NodeType "NT1".</span><span class="sxs-lookup"><span data-stu-id="262e5-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="262e5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="262e5-111">PARAMETERS</span></span>

### <span data-ttu-id="262e5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262e5-112">-DefaultProfile</span></span>
<span data-ttu-id="262e5-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="262e5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="262e5-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="262e5-114">-Name</span></span>
<span data-ttu-id="262e5-115">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="262e5-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="262e5-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="262e5-116">-NodeType</span></span>
<span data-ttu-id="262e5-117">Имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="262e5-117">Node type name.</span></span>

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

### <span data-ttu-id="262e5-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="262e5-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="262e5-119">Количество узлов, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="262e5-119">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="262e5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="262e5-120">-ResourceGroupName</span></span>
<span data-ttu-id="262e5-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="262e5-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="262e5-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="262e5-122">-Confirm</span></span>
<span data-ttu-id="262e5-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="262e5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="262e5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="262e5-124">-WhatIf</span></span>
<span data-ttu-id="262e5-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="262e5-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="262e5-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="262e5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="262e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262e5-127">CommonParameters</span></span>
<span data-ttu-id="262e5-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="262e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262e5-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="262e5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262e5-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="262e5-130">INPUTS</span></span>

### <span data-ttu-id="262e5-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="262e5-131">System.Int32</span></span>

### <span data-ttu-id="262e5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="262e5-132">System.String</span></span>

## <span data-ttu-id="262e5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="262e5-133">OUTPUTS</span></span>

### <span data-ttu-id="262e5-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="262e5-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="262e5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="262e5-135">NOTES</span></span>

## <span data-ttu-id="262e5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="262e5-136">RELATED LINKS</span></span>

[<span data-ttu-id="262e5-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="262e5-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md) 
