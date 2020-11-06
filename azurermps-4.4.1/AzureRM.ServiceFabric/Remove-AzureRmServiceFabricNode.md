---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: cbf23af4c98e8174091b467e6e05ed5de6ae20c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562132"
---
# <span data-ttu-id="9ace4-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="9ace4-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="9ace4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ace4-102">SYNOPSIS</span></span>
<span data-ttu-id="9ace4-103">Удаление узлов из кластера с определенным типом узла.</span><span class="sxs-lookup"><span data-stu-id="9ace4-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ace4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ace4-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToRemove <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ace4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ace4-105">DESCRIPTION</span></span>
<span data-ttu-id="9ace4-106">С помощью **Remove-AzureRmServiceFabricNode** удалите узлы из кластера определенного типа.</span><span class="sxs-lookup"><span data-stu-id="9ace4-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="9ace4-107">Удаление выполняется только в том случае, если оно соответствует метрикам работоспособности кластера.</span><span class="sxs-lookup"><span data-stu-id="9ace4-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="9ace4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ace4-108">EXAMPLES</span></span>

### <span data-ttu-id="9ace4-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ace4-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="9ace4-110">Эта команда удалит 2 узла из NodeType "NT1".</span><span class="sxs-lookup"><span data-stu-id="9ace4-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="9ace4-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ace4-111">PARAMETERS</span></span>

### <span data-ttu-id="9ace4-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ace4-112">-Name</span></span>
<span data-ttu-id="9ace4-113">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="9ace4-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9ace4-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="9ace4-114">-NodeType</span></span>
<span data-ttu-id="9ace4-115">Имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="9ace4-115">Node type name.</span></span>

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

### <span data-ttu-id="9ace4-116">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="9ace4-116">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="9ace4-117">Количество узлов, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9ace4-117">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="9ace4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ace4-118">-ResourceGroupName</span></span>
<span data-ttu-id="9ace4-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ace4-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9ace4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ace4-120">-Confirm</span></span>
<span data-ttu-id="9ace4-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ace4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ace4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ace4-122">-WhatIf</span></span>
<span data-ttu-id="9ace4-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ace4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ace4-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ace4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ace4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ace4-125">-DefaultProfile</span></span>
<span data-ttu-id="9ace4-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ace4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ace4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ace4-127">CommonParameters</span></span>
<span data-ttu-id="9ace4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ace4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ace4-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ace4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ace4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ace4-130">INPUTS</span></span>

### <span data-ttu-id="9ace4-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9ace4-131">System.Int32</span></span>
<span data-ttu-id="9ace4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9ace4-132">System.String</span></span>

## <span data-ttu-id="9ace4-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ace4-133">OUTPUTS</span></span>

### <span data-ttu-id="9ace4-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="9ace4-134">System.Object</span></span>

## <span data-ttu-id="9ace4-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ace4-135">NOTES</span></span>

## <span data-ttu-id="9ace4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ace4-136">RELATED LINKS</span></span>

[<span data-ttu-id="9ace4-137">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="9ace4-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
