---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217508"
---
# <span data-ttu-id="94437-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="94437-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="94437-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94437-102">SYNOPSIS</span></span>
<span data-ttu-id="94437-103">Удалите из кластера полный тип узла.</span><span class="sxs-lookup"><span data-stu-id="94437-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="94437-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94437-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94437-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94437-105">DESCRIPTION</span></span>
<span data-ttu-id="94437-106">Используйте **remove-AzServiceFabricNodeType,** чтобы удалить все узлы определенного типа и типа узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="94437-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="94437-107">Эту команду нельзя использовать для удаления основного типа узла.</span><span class="sxs-lookup"><span data-stu-id="94437-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="94437-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94437-108">EXAMPLES</span></span>

### <span data-ttu-id="94437-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94437-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="94437-110">Эта команда удаляет NodeType "nt1" из кластера.</span><span class="sxs-lookup"><span data-stu-id="94437-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="94437-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94437-111">PARAMETERS</span></span>

### <span data-ttu-id="94437-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94437-112">-DefaultProfile</span></span>
<span data-ttu-id="94437-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94437-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94437-114">-Name</span><span class="sxs-lookup"><span data-stu-id="94437-114">-Name</span></span>
<span data-ttu-id="94437-115">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="94437-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="94437-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="94437-116">-NodeType</span></span>
<span data-ttu-id="94437-117">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="94437-117">The node type name</span></span>

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

### <span data-ttu-id="94437-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94437-118">-ResourceGroupName</span></span>
<span data-ttu-id="94437-119">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94437-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="94437-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94437-120">-Confirm</span></span>
<span data-ttu-id="94437-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94437-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94437-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94437-122">-WhatIf</span></span>
<span data-ttu-id="94437-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94437-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94437-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94437-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94437-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94437-125">CommonParameters</span></span>
<span data-ttu-id="94437-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94437-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94437-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94437-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94437-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94437-128">INPUTS</span></span>

### <span data-ttu-id="94437-129">System.String</span><span class="sxs-lookup"><span data-stu-id="94437-129">System.String</span></span>

## <span data-ttu-id="94437-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94437-130">OUTPUTS</span></span>

### <span data-ttu-id="94437-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="94437-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="94437-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94437-132">NOTES</span></span>

## <span data-ttu-id="94437-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94437-133">RELATED LINKS</span></span>
