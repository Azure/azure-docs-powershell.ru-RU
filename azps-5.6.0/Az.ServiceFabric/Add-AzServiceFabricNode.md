---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 34b55a5da226a3985cb6fe3bede244ee1e054726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984067"
---
# <span data-ttu-id="b4b9c-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="b4b9c-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="b4b9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b9c-103">Добавьте узлы для определенного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="b4b9c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4b9c-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4b9c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="b4b9c-106">Добавьте узлы к определенному типу с помощью **add-AzServiceFabricNode.**</span><span class="sxs-lookup"><span data-stu-id="b4b9c-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="b4b9c-107">Достаточно указать количество узлов, которые вы хотите добавить к типу узла.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="b4b9c-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4b9c-108">EXAMPLES</span></span>

### <span data-ttu-id="b4b9c-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4b9c-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="b4b9c-110">Эта команда добавит 2 узла к типу узла "n1".</span><span class="sxs-lookup"><span data-stu-id="b4b9c-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="b4b9c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4b9c-111">PARAMETERS</span></span>

### <span data-ttu-id="b4b9c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b9c-112">-DefaultProfile</span></span>
<span data-ttu-id="b4b9c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4b9c-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b4b9c-114">-Name</span></span>
<span data-ttu-id="b4b9c-115">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="b4b9c-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="b4b9c-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b4b9c-116">-NodeType</span></span>
<span data-ttu-id="b4b9c-117">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="b4b9c-117">Node type name</span></span>

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

### <span data-ttu-id="b4b9c-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="b4b9c-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="b4b9c-119">Количество узлов, которые нужно добавить</span><span class="sxs-lookup"><span data-stu-id="b4b9c-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="b4b9c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4b9c-120">-ResourceGroupName</span></span>
<span data-ttu-id="b4b9c-121">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b4b9c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4b9c-122">-Confirm</span></span>
<span data-ttu-id="b4b9c-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b9c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b9c-124">-WhatIf</span></span>
<span data-ttu-id="b4b9c-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b9c-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b9c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b9c-127">CommonParameters</span></span>
<span data-ttu-id="b4b9c-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b9c-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4b9c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b9c-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4b9c-130">INPUTS</span></span>

### <span data-ttu-id="b4b9c-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b4b9c-131">System.Int32</span></span>

### <span data-ttu-id="b4b9c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b4b9c-132">System.String</span></span>

## <span data-ttu-id="b4b9c-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4b9c-133">OUTPUTS</span></span>

### <span data-ttu-id="b4b9c-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="b4b9c-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b4b9c-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4b9c-135">NOTES</span></span>

## <span data-ttu-id="b4b9c-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4b9c-136">RELATED LINKS</span></span>

[<span data-ttu-id="b4b9c-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="b4b9c-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
