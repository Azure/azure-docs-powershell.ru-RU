---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: f825d1ba1621a00be6196219d99dc188496ea5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558807"
---
# <span data-ttu-id="f9965-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f9965-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="f9965-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9965-102">SYNOPSIS</span></span>
<span data-ttu-id="f9965-103">Удаление типа полного узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="f9965-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9965-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9965-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9965-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9965-105">DESCRIPTION</span></span>
<span data-ttu-id="f9965-106">С помощью **Remove-AzureRmServiceFabricNodeType** можно удалить все узлы из определенного типа узла и типа узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="f9965-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="f9965-107">Эту команду нельзя использовать для удаления типа основного узла.</span><span class="sxs-lookup"><span data-stu-id="f9965-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="f9965-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9965-108">EXAMPLES</span></span>

### <span data-ttu-id="f9965-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f9965-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="f9965-110">Эта команда удалит из кластера NodeType "NT1".</span><span class="sxs-lookup"><span data-stu-id="f9965-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="f9965-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9965-111">PARAMETERS</span></span>

### <span data-ttu-id="f9965-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9965-112">-DefaultProfile</span></span>
<span data-ttu-id="f9965-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9965-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9965-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9965-114">-Name</span></span>
<span data-ttu-id="f9965-115">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="f9965-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f9965-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="f9965-116">-NodeType</span></span>
<span data-ttu-id="f9965-117">Имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="f9965-117">The node type name.</span></span>

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

### <span data-ttu-id="f9965-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9965-118">-ResourceGroupName</span></span>
<span data-ttu-id="f9965-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f9965-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f9965-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9965-120">-Confirm</span></span>
<span data-ttu-id="f9965-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f9965-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9965-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9965-122">-WhatIf</span></span>
<span data-ttu-id="f9965-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f9965-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9965-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f9965-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9965-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9965-125">CommonParameters</span></span>
<span data-ttu-id="f9965-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9965-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9965-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9965-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9965-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9965-128">INPUTS</span></span>

### <span data-ttu-id="f9965-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f9965-129">System.String</span></span>

## <span data-ttu-id="f9965-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9965-130">OUTPUTS</span></span>

### <span data-ttu-id="f9965-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="f9965-131">System.Object</span></span>

## <span data-ttu-id="f9965-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9965-132">NOTES</span></span>

## <span data-ttu-id="f9965-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9965-133">RELATED LINKS</span></span>

