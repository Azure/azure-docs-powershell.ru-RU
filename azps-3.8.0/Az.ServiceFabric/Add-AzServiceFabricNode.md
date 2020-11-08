---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 7f19e7e1891eb7dee4edbe382d2fb3936b401549
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074303"
---
# <span data-ttu-id="c2650-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c2650-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="c2650-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2650-102">SYNOPSIS</span></span>
<span data-ttu-id="c2650-103">Добавьте узлы в конкретный тип узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="c2650-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="c2650-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2650-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2650-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2650-105">DESCRIPTION</span></span>
<span data-ttu-id="c2650-106">Используйте **Add-AzServiceFabricNode** , чтобы добавить узлы в конкретный тип узла.</span><span class="sxs-lookup"><span data-stu-id="c2650-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="c2650-107">Вам нужно просто указать количество узлов, которые нужно добавить в тип узла.</span><span class="sxs-lookup"><span data-stu-id="c2650-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="c2650-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2650-108">EXAMPLES</span></span>

### <span data-ttu-id="c2650-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2650-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="c2650-110">Эта команда добавит 2 узла в тип "N1".</span><span class="sxs-lookup"><span data-stu-id="c2650-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="c2650-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2650-111">PARAMETERS</span></span>

### <span data-ttu-id="c2650-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2650-112">-DefaultProfile</span></span>
<span data-ttu-id="c2650-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2650-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2650-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2650-114">-Name</span></span>
<span data-ttu-id="c2650-115">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="c2650-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="c2650-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="c2650-116">-NodeType</span></span>
<span data-ttu-id="c2650-117">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="c2650-117">Node type name</span></span>

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

### <span data-ttu-id="c2650-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="c2650-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="c2650-119">Количество добавляемых узлов</span><span class="sxs-lookup"><span data-stu-id="c2650-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="c2650-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2650-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2650-121">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2650-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c2650-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2650-122">-Confirm</span></span>
<span data-ttu-id="c2650-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2650-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2650-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2650-124">-WhatIf</span></span>
<span data-ttu-id="c2650-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2650-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2650-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2650-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2650-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2650-127">CommonParameters</span></span>
<span data-ttu-id="c2650-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2650-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2650-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2650-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2650-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2650-130">INPUTS</span></span>

### <span data-ttu-id="c2650-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c2650-131">System.Int32</span></span>

### <span data-ttu-id="c2650-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c2650-132">System.String</span></span>

## <span data-ttu-id="c2650-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2650-133">OUTPUTS</span></span>

### <span data-ttu-id="c2650-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c2650-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c2650-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2650-135">NOTES</span></span>

## <span data-ttu-id="c2650-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2650-136">RELATED LINKS</span></span>

[<span data-ttu-id="c2650-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c2650-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
