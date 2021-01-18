---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 41c78b659a39d3df52185eeb2b67e4c921f22b45
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517297"
---
# <span data-ttu-id="6f77b-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6f77b-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="6f77b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f77b-102">SYNOPSIS</span></span>
<span data-ttu-id="6f77b-103">Добавьте узлы для определенного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="6f77b-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="6f77b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f77b-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f77b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f77b-105">DESCRIPTION</span></span>
<span data-ttu-id="6f77b-106">Добавьте узлы к определенному типу с помощью **add-AzServiceFabricNode.**</span><span class="sxs-lookup"><span data-stu-id="6f77b-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="6f77b-107">Достаточно указать количество узлов, которые вы хотите добавить к типу узла.</span><span class="sxs-lookup"><span data-stu-id="6f77b-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="6f77b-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f77b-108">EXAMPLES</span></span>

### <span data-ttu-id="6f77b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f77b-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="6f77b-110">Эта команда добавит 2 узла к типу узла "n1".</span><span class="sxs-lookup"><span data-stu-id="6f77b-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="6f77b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f77b-111">PARAMETERS</span></span>

### <span data-ttu-id="6f77b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f77b-112">-DefaultProfile</span></span>
<span data-ttu-id="6f77b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f77b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f77b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6f77b-114">-Name</span></span>
<span data-ttu-id="6f77b-115">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="6f77b-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="6f77b-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="6f77b-116">-NodeType</span></span>
<span data-ttu-id="6f77b-117">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="6f77b-117">Node type name</span></span>

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

### <span data-ttu-id="6f77b-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="6f77b-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="6f77b-119">Количество узлов, которые нужно добавить</span><span class="sxs-lookup"><span data-stu-id="6f77b-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="6f77b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f77b-120">-ResourceGroupName</span></span>
<span data-ttu-id="6f77b-121">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f77b-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6f77b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f77b-122">-Confirm</span></span>
<span data-ttu-id="6f77b-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f77b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f77b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f77b-124">-WhatIf</span></span>
<span data-ttu-id="6f77b-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f77b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f77b-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6f77b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f77b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f77b-127">CommonParameters</span></span>
<span data-ttu-id="6f77b-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f77b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f77b-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f77b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f77b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f77b-130">INPUTS</span></span>

### <span data-ttu-id="6f77b-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6f77b-131">System.Int32</span></span>

### <span data-ttu-id="6f77b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6f77b-132">System.String</span></span>

## <span data-ttu-id="6f77b-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f77b-133">OUTPUTS</span></span>

### <span data-ttu-id="6f77b-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="6f77b-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6f77b-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f77b-135">NOTES</span></span>

## <span data-ttu-id="6f77b-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f77b-136">RELATED LINKS</span></span>

[<span data-ttu-id="6f77b-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6f77b-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
