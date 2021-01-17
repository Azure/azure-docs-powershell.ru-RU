---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 41c78b659a39d3df52185eeb2b67e4c921f22b45
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393071"
---
# <span data-ttu-id="5fff8-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5fff8-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="5fff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fff8-102">SYNOPSIS</span></span>
<span data-ttu-id="5fff8-103">Добавьте узлы для определенного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="5fff8-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="5fff8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5fff8-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fff8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fff8-105">DESCRIPTION</span></span>
<span data-ttu-id="5fff8-106">Добавьте узлы к определенному типу с помощью **add-AzServiceFabricNode.**</span><span class="sxs-lookup"><span data-stu-id="5fff8-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="5fff8-107">Достаточно указать количество узлов, которые вы хотите добавить к типу узла.</span><span class="sxs-lookup"><span data-stu-id="5fff8-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="5fff8-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5fff8-108">EXAMPLES</span></span>

### <span data-ttu-id="5fff8-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fff8-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="5fff8-110">Эта команда добавит 2 узла к типу узла "n1".</span><span class="sxs-lookup"><span data-stu-id="5fff8-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="5fff8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fff8-111">PARAMETERS</span></span>

### <span data-ttu-id="5fff8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fff8-112">-DefaultProfile</span></span>
<span data-ttu-id="5fff8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fff8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fff8-114">-Name</span><span class="sxs-lookup"><span data-stu-id="5fff8-114">-Name</span></span>
<span data-ttu-id="5fff8-115">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="5fff8-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="5fff8-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="5fff8-116">-NodeType</span></span>
<span data-ttu-id="5fff8-117">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="5fff8-117">Node type name</span></span>

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

### <span data-ttu-id="5fff8-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="5fff8-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="5fff8-119">Количество узлов, которые нужно добавить</span><span class="sxs-lookup"><span data-stu-id="5fff8-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="5fff8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fff8-120">-ResourceGroupName</span></span>
<span data-ttu-id="5fff8-121">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5fff8-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5fff8-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fff8-122">-Confirm</span></span>
<span data-ttu-id="5fff8-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5fff8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fff8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fff8-124">-WhatIf</span></span>
<span data-ttu-id="5fff8-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fff8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fff8-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5fff8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fff8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fff8-127">CommonParameters</span></span>
<span data-ttu-id="5fff8-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fff8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fff8-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fff8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fff8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fff8-130">INPUTS</span></span>

### <span data-ttu-id="5fff8-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5fff8-131">System.Int32</span></span>

### <span data-ttu-id="5fff8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5fff8-132">System.String</span></span>

## <span data-ttu-id="5fff8-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5fff8-133">OUTPUTS</span></span>

### <span data-ttu-id="5fff8-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="5fff8-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="5fff8-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5fff8-135">NOTES</span></span>

## <span data-ttu-id="5fff8-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fff8-136">RELATED LINKS</span></span>

[<span data-ttu-id="5fff8-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5fff8-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
