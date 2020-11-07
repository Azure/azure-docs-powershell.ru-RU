---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: fdcc8946070994cd172514f8da1578328ae61db2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903778"
---
# <span data-ttu-id="a26b1-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a26b1-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="a26b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a26b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a26b1-103">Добавьте узлы в конкретный тип узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="a26b1-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="a26b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a26b1-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a26b1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a26b1-105">DESCRIPTION</span></span>
<span data-ttu-id="a26b1-106">Используйте **Add-AzServiceFabricNode** , чтобы добавить узлы в конкретный тип узла.</span><span class="sxs-lookup"><span data-stu-id="a26b1-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="a26b1-107">Вам нужно просто указать количество узлов, которые нужно добавить в тип узла.</span><span class="sxs-lookup"><span data-stu-id="a26b1-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="a26b1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a26b1-108">EXAMPLES</span></span>

### <span data-ttu-id="a26b1-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a26b1-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="a26b1-110">Эта команда добавит 2 узла в тип "N1".</span><span class="sxs-lookup"><span data-stu-id="a26b1-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="a26b1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a26b1-111">PARAMETERS</span></span>

### <span data-ttu-id="a26b1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a26b1-112">-DefaultProfile</span></span>
<span data-ttu-id="a26b1-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a26b1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a26b1-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a26b1-114">-Name</span></span>
<span data-ttu-id="a26b1-115">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="a26b1-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a26b1-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a26b1-116">-NodeType</span></span>
<span data-ttu-id="a26b1-117">Имя типа узла</span><span class="sxs-lookup"><span data-stu-id="a26b1-117">Node type name</span></span>

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

### <span data-ttu-id="a26b1-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="a26b1-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="a26b1-119">Количество добавляемых узлов</span><span class="sxs-lookup"><span data-stu-id="a26b1-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="a26b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a26b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="a26b1-121">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a26b1-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a26b1-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a26b1-122">-Confirm</span></span>
<span data-ttu-id="a26b1-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a26b1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a26b1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a26b1-124">-WhatIf</span></span>
<span data-ttu-id="a26b1-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a26b1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a26b1-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a26b1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a26b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a26b1-127">CommonParameters</span></span>
<span data-ttu-id="a26b1-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a26b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a26b1-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a26b1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a26b1-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a26b1-130">INPUTS</span></span>

### <span data-ttu-id="a26b1-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a26b1-131">System.Int32</span></span>

### <span data-ttu-id="a26b1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a26b1-132">System.String</span></span>

## <span data-ttu-id="a26b1-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a26b1-133">OUTPUTS</span></span>

### <span data-ttu-id="a26b1-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a26b1-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a26b1-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a26b1-135">NOTES</span></span>

## <span data-ttu-id="a26b1-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a26b1-136">RELATED LINKS</span></span>

[<span data-ttu-id="a26b1-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a26b1-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
