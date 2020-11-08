---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 96706ef98a0b21bab06e2c6e8fae947dcd205271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066142"
---
# <span data-ttu-id="db673-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="db673-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="db673-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db673-102">SYNOPSIS</span></span>
<span data-ttu-id="db673-103">Удаление узлов из кластера с определенным типом узла.</span><span class="sxs-lookup"><span data-stu-id="db673-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="db673-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db673-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db673-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db673-105">DESCRIPTION</span></span>
<span data-ttu-id="db673-106">С помощью **Remove-AzServiceFabricNode** удалите узлы из кластера определенного типа.</span><span class="sxs-lookup"><span data-stu-id="db673-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="db673-107">Удаление выполняется только в том случае, если оно соответствует метрикам работоспособности кластера.</span><span class="sxs-lookup"><span data-stu-id="db673-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="db673-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db673-108">EXAMPLES</span></span>

### <span data-ttu-id="db673-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db673-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="db673-110">Эта команда удалит 2 узла из NodeType "NT1".</span><span class="sxs-lookup"><span data-stu-id="db673-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="db673-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db673-111">PARAMETERS</span></span>

### <span data-ttu-id="db673-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db673-112">-DefaultProfile</span></span>
<span data-ttu-id="db673-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db673-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db673-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db673-114">-Name</span></span>
<span data-ttu-id="db673-115">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="db673-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="db673-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="db673-116">-NodeType</span></span>
<span data-ttu-id="db673-117">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="db673-117">Node type name</span></span>

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

### <span data-ttu-id="db673-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="db673-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="db673-119">Количество добавляемых узлов</span><span class="sxs-lookup"><span data-stu-id="db673-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="db673-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db673-120">-ResourceGroupName</span></span>
<span data-ttu-id="db673-121">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db673-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="db673-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db673-122">-Confirm</span></span>
<span data-ttu-id="db673-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db673-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db673-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db673-124">-WhatIf</span></span>
<span data-ttu-id="db673-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db673-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db673-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db673-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db673-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db673-127">CommonParameters</span></span>
<span data-ttu-id="db673-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db673-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db673-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db673-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db673-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db673-130">INPUTS</span></span>

### <span data-ttu-id="db673-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="db673-131">System.Int32</span></span>

### <span data-ttu-id="db673-132">System. String</span><span class="sxs-lookup"><span data-stu-id="db673-132">System.String</span></span>

## <span data-ttu-id="db673-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db673-133">OUTPUTS</span></span>

### <span data-ttu-id="db673-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="db673-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="db673-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="db673-135">NOTES</span></span>

## <span data-ttu-id="db673-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db673-136">RELATED LINKS</span></span>

[<span data-ttu-id="db673-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="db673-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
