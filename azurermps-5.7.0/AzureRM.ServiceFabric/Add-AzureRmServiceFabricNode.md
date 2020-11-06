---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: af8f5d38777674d761b8b55c649b048c933f2c66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563300"
---
# <span data-ttu-id="4f7af-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="4f7af-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="4f7af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f7af-102">SYNOPSIS</span></span>
<span data-ttu-id="4f7af-103">Добавьте узлы в конкретный тип узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="4f7af-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f7af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f7af-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f7af-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f7af-105">DESCRIPTION</span></span>
<span data-ttu-id="4f7af-106">Используйте **Add-AzureRmServiceFabricNode** , чтобы добавить узлы в конкретный тип узла.</span><span class="sxs-lookup"><span data-stu-id="4f7af-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="4f7af-107">Вам нужно просто указать количество узлов, которые нужно добавить в тип узла.</span><span class="sxs-lookup"><span data-stu-id="4f7af-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="4f7af-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f7af-108">EXAMPLES</span></span>

### <span data-ttu-id="4f7af-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4f7af-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="4f7af-110">Эта команда добавит 2 узла в тип "N1".</span><span class="sxs-lookup"><span data-stu-id="4f7af-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="4f7af-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f7af-111">PARAMETERS</span></span>

### <span data-ttu-id="4f7af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f7af-112">-DefaultProfile</span></span>
<span data-ttu-id="4f7af-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f7af-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f7af-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4f7af-114">-Name</span></span>
<span data-ttu-id="4f7af-115">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="4f7af-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4f7af-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="4f7af-116">-NodeType</span></span>
<span data-ttu-id="4f7af-117">Имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="4f7af-117">Node type name.</span></span>

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

### <span data-ttu-id="4f7af-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="4f7af-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="4f7af-119">Номер экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f7af-119">VM instance number.</span></span>

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

### <span data-ttu-id="4f7af-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f7af-120">-ResourceGroupName</span></span>
<span data-ttu-id="4f7af-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4f7af-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4f7af-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f7af-122">-Confirm</span></span>
<span data-ttu-id="4f7af-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4f7af-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f7af-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f7af-124">-WhatIf</span></span>
<span data-ttu-id="4f7af-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4f7af-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f7af-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4f7af-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f7af-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f7af-127">CommonParameters</span></span>
<span data-ttu-id="4f7af-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f7af-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f7af-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f7af-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f7af-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f7af-130">INPUTS</span></span>

### <span data-ttu-id="4f7af-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4f7af-131">System.String</span></span>

## <span data-ttu-id="4f7af-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f7af-132">OUTPUTS</span></span>

### <span data-ttu-id="4f7af-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="4f7af-133">System.Object</span></span>

## <span data-ttu-id="4f7af-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f7af-134">NOTES</span></span>

## <span data-ttu-id="4f7af-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f7af-135">RELATED LINKS</span></span>

[<span data-ttu-id="4f7af-136">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="4f7af-136">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
