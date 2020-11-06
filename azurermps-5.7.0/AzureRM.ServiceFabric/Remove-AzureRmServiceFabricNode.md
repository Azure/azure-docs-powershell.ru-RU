---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: 6df403d432d212e1d0f8d074b9ac57caad438f83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566099"
---
# <span data-ttu-id="ffa1c-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ffa1c-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="ffa1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ffa1c-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa1c-103">Удаление узлов из кластера с определенным типом узла.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffa1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ffa1c-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffa1c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffa1c-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa1c-106">С помощью **Remove-AzureRmServiceFabricNode** удалите узлы из кластера определенного типа.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="ffa1c-107">Удаление выполняется только в том случае, если оно соответствует метрикам работоспособности кластера.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="ffa1c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ffa1c-108">EXAMPLES</span></span>

### <span data-ttu-id="ffa1c-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ffa1c-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="ffa1c-110">Эта команда удалит 2 узла из NodeType "NT1".</span><span class="sxs-lookup"><span data-stu-id="ffa1c-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="ffa1c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ffa1c-111">PARAMETERS</span></span>

### <span data-ttu-id="ffa1c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa1c-112">-DefaultProfile</span></span>
<span data-ttu-id="ffa1c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa1c-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ffa1c-114">-Name</span></span>
<span data-ttu-id="ffa1c-115">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-115">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa1c-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ffa1c-116">-NodeType</span></span>
<span data-ttu-id="ffa1c-117">Имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-117">Node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa1c-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="ffa1c-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="ffa1c-119">Количество узлов, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-119">Number of nodes to remove.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa1c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa1c-120">-ResourceGroupName</span></span>
<span data-ttu-id="ffa1c-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa1c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffa1c-122">-Confirm</span></span>
<span data-ttu-id="ffa1c-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa1c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa1c-124">-WhatIf</span></span>
<span data-ttu-id="ffa1c-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffa1c-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa1c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa1c-127">CommonParameters</span></span>
<span data-ttu-id="ffa1c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ffa1c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa1c-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffa1c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa1c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ffa1c-130">INPUTS</span></span>

### <span data-ttu-id="ffa1c-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ffa1c-131">System.Int32</span></span>
<span data-ttu-id="ffa1c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ffa1c-132">System.String</span></span>

## <span data-ttu-id="ffa1c-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffa1c-133">OUTPUTS</span></span>

### <span data-ttu-id="ffa1c-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="ffa1c-134">System.Object</span></span>

## <span data-ttu-id="ffa1c-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ffa1c-135">NOTES</span></span>

## <span data-ttu-id="ffa1c-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffa1c-136">RELATED LINKS</span></span>

[<span data-ttu-id="ffa1c-137">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ffa1c-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
