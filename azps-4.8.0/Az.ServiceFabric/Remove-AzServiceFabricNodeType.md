---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235848"
---
# <span data-ttu-id="82047-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="82047-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="82047-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82047-102">SYNOPSIS</span></span>
<span data-ttu-id="82047-103">Удаление типа полного узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="82047-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="82047-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82047-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82047-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82047-105">DESCRIPTION</span></span>
<span data-ttu-id="82047-106">С помощью **Remove-AzServiceFabricNodeType** можно удалить все узлы из определенного типа узла и типа узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="82047-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="82047-107">Эту команду нельзя использовать для удаления типа основного узла.</span><span class="sxs-lookup"><span data-stu-id="82047-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="82047-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82047-108">EXAMPLES</span></span>

### <span data-ttu-id="82047-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="82047-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="82047-110">Эта команда удалит из кластера NodeType "NT1".</span><span class="sxs-lookup"><span data-stu-id="82047-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="82047-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82047-111">PARAMETERS</span></span>

### <span data-ttu-id="82047-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82047-112">-DefaultProfile</span></span>
<span data-ttu-id="82047-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82047-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82047-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82047-114">-Name</span></span>
<span data-ttu-id="82047-115">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="82047-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="82047-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="82047-116">-NodeType</span></span>
<span data-ttu-id="82047-117">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="82047-117">The node type name</span></span>

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

### <span data-ttu-id="82047-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82047-118">-ResourceGroupName</span></span>
<span data-ttu-id="82047-119">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82047-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="82047-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82047-120">-Confirm</span></span>
<span data-ttu-id="82047-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="82047-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82047-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82047-122">-WhatIf</span></span>
<span data-ttu-id="82047-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="82047-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82047-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="82047-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82047-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82047-125">CommonParameters</span></span>
<span data-ttu-id="82047-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82047-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82047-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82047-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82047-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82047-128">INPUTS</span></span>

### <span data-ttu-id="82047-129">System. String</span><span class="sxs-lookup"><span data-stu-id="82047-129">System.String</span></span>

## <span data-ttu-id="82047-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82047-130">OUTPUTS</span></span>

### <span data-ttu-id="82047-131">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="82047-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="82047-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="82047-132">NOTES</span></span>

## <span data-ttu-id="82047-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82047-133">RELATED LINKS</span></span>
