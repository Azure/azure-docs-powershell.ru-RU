---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 3da05194d74de1fe547beb66dea420a7f0e90155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562131"
---
# <span data-ttu-id="913cd-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="913cd-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="913cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="913cd-102">SYNOPSIS</span></span>
<span data-ttu-id="913cd-103">Удаление типа полного узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="913cd-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="913cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="913cd-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="913cd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="913cd-105">DESCRIPTION</span></span>
<span data-ttu-id="913cd-106">С помощью **Remove-AzureRmServiceFabricNodeType** можно удалить все узлы из определенного типа узла и типа узла из кластера.</span><span class="sxs-lookup"><span data-stu-id="913cd-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="913cd-107">Эту команду нельзя использовать для удаления типа основного узла.</span><span class="sxs-lookup"><span data-stu-id="913cd-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="913cd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="913cd-108">EXAMPLES</span></span>

### <span data-ttu-id="913cd-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="913cd-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="913cd-110">Эта команда удалит из кластера NodeType "NT1".</span><span class="sxs-lookup"><span data-stu-id="913cd-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="913cd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="913cd-111">PARAMETERS</span></span>

### <span data-ttu-id="913cd-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="913cd-112">-Name</span></span>
<span data-ttu-id="913cd-113">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="913cd-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="913cd-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="913cd-114">-NodeType</span></span>
<span data-ttu-id="913cd-115">Имя типа узла.</span><span class="sxs-lookup"><span data-stu-id="913cd-115">The node type name.</span></span>

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

### <span data-ttu-id="913cd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913cd-116">-ResourceGroupName</span></span>
<span data-ttu-id="913cd-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="913cd-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="913cd-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="913cd-118">-Confirm</span></span>
<span data-ttu-id="913cd-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="913cd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="913cd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="913cd-120">-WhatIf</span></span>
<span data-ttu-id="913cd-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="913cd-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="913cd-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="913cd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="913cd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913cd-123">-DefaultProfile</span></span>
<span data-ttu-id="913cd-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="913cd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="913cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913cd-125">CommonParameters</span></span>
<span data-ttu-id="913cd-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="913cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913cd-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913cd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913cd-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="913cd-128">INPUTS</span></span>

### <span data-ttu-id="913cd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="913cd-129">System.String</span></span>

## <span data-ttu-id="913cd-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="913cd-130">OUTPUTS</span></span>

### <span data-ttu-id="913cd-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="913cd-131">System.Object</span></span>

## <span data-ttu-id="913cd-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="913cd-132">NOTES</span></span>

## <span data-ttu-id="913cd-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="913cd-133">RELATED LINKS</span></span>

