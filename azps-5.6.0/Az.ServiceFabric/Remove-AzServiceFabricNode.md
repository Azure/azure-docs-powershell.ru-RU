---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: ba5400a35939a221b19ba144b35b0f2a53f6dbe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005432"
---
# <span data-ttu-id="2b929-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2b929-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="2b929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b929-102">SYNOPSIS</span></span>
<span data-ttu-id="2b929-103">Удалите узлы с определенного типа узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="2b929-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="2b929-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2b929-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b929-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b929-105">DESCRIPTION</span></span>
<span data-ttu-id="2b929-106">Используйте **remove-AzServiceFabricNode,** чтобы удалить узлы определенного типа из кластера.</span><span class="sxs-lookup"><span data-stu-id="2b929-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="2b929-107">Удаление выполняется только в том случае, если оно соответствует показатели эффективности кластера.</span><span class="sxs-lookup"><span data-stu-id="2b929-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="2b929-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2b929-108">EXAMPLES</span></span>

### <span data-ttu-id="2b929-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b929-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="2b929-110">Эта команда удалит 2 узла из NodeType "nt1".</span><span class="sxs-lookup"><span data-stu-id="2b929-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="2b929-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b929-111">PARAMETERS</span></span>

### <span data-ttu-id="2b929-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b929-112">-DefaultProfile</span></span>
<span data-ttu-id="2b929-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b929-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b929-114">-Name</span><span class="sxs-lookup"><span data-stu-id="2b929-114">-Name</span></span>
<span data-ttu-id="2b929-115">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="2b929-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="2b929-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="2b929-116">-NodeType</span></span>
<span data-ttu-id="2b929-117">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="2b929-117">Node type name</span></span>

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

### <span data-ttu-id="2b929-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="2b929-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="2b929-119">Количество узлов, которые нужно добавить</span><span class="sxs-lookup"><span data-stu-id="2b929-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="2b929-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b929-120">-ResourceGroupName</span></span>
<span data-ttu-id="2b929-121">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b929-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2b929-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b929-122">-Confirm</span></span>
<span data-ttu-id="2b929-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2b929-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b929-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b929-124">-WhatIf</span></span>
<span data-ttu-id="2b929-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b929-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b929-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2b929-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b929-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b929-127">CommonParameters</span></span>
<span data-ttu-id="2b929-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b929-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b929-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b929-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b929-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b929-130">INPUTS</span></span>

### <span data-ttu-id="2b929-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2b929-131">System.Int32</span></span>

### <span data-ttu-id="2b929-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2b929-132">System.String</span></span>

## <span data-ttu-id="2b929-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2b929-133">OUTPUTS</span></span>

### <span data-ttu-id="2b929-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="2b929-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2b929-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2b929-135">NOTES</span></span>

## <span data-ttu-id="2b929-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b929-136">RELATED LINKS</span></span>

[<span data-ttu-id="2b929-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2b929-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
