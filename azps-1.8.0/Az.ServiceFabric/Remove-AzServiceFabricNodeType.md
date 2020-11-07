---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: d0de428417d59fc6103b9198265f4a38ad04dd52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729106"
---
# <span data-ttu-id="b7f0d-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="b7f0d-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="b7f0d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f0d-103">Удаление типа полного узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="b7f0d-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="b7f0d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7f0d-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7f0d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7f0d-105">DESCRIPTION</span></span>
<span data-ttu-id="b7f0d-106">С помощью **Remove-AzServiceFabricNodeType** можно удалить все узлы из определенного типа узла и типа узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="b7f0d-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="b7f0d-107">Эту команду нельзя использовать для удаления типа основного узла.</span><span class="sxs-lookup"><span data-stu-id="b7f0d-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="b7f0d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7f0d-108">EXAMPLES</span></span>

### <span data-ttu-id="b7f0d-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7f0d-109">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="b7f0d-110">Эта команда удалит из кластера NodeType "NT1".</span><span class="sxs-lookup"><span data-stu-id="b7f0d-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="b7f0d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7f0d-111">PARAMETERS</span></span>

### <span data-ttu-id="b7f0d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f0d-112">-DefaultProfile</span></span>
<span data-ttu-id="b7f0d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f0d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7f0d-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7f0d-114">-Name</span></span>
<span data-ttu-id="b7f0d-115">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="b7f0d-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b7f0d-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b7f0d-116">-NodeType</span></span>
<span data-ttu-id="b7f0d-117">Имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="b7f0d-117">The node type name.</span></span>

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

### <span data-ttu-id="b7f0d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f0d-118">-ResourceGroupName</span></span>
<span data-ttu-id="b7f0d-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7f0d-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b7f0d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7f0d-120">-Confirm</span></span>
<span data-ttu-id="b7f0d-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7f0d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f0d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f0d-122">-WhatIf</span></span>
<span data-ttu-id="b7f0d-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b7f0d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7f0d-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b7f0d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f0d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f0d-125">CommonParameters</span></span>
<span data-ttu-id="b7f0d-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7f0d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f0d-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f0d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f0d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7f0d-128">INPUTS</span></span>

### <span data-ttu-id="b7f0d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b7f0d-129">System.String</span></span>

## <span data-ttu-id="b7f0d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7f0d-130">OUTPUTS</span></span>

### <span data-ttu-id="b7f0d-131">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b7f0d-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b7f0d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7f0d-132">NOTES</span></span>

## <span data-ttu-id="b7f0d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7f0d-133">RELATED LINKS</span></span>
