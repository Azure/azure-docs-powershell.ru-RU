---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: 07aa0f8b9d207a460d370e3e5c51b720895b62e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073716"
---
# <span data-ttu-id="19c33-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="19c33-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="19c33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19c33-102">SYNOPSIS</span></span>
<span data-ttu-id="19c33-103">Обновите уровень надежности основного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="19c33-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="19c33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19c33-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c33-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19c33-105">DESCRIPTION</span></span>
<span data-ttu-id="19c33-106">Используйте **Update-AzServiceFabricReliability** , чтобы обновить надежность типа основного узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="19c33-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="19c33-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19c33-107">EXAMPLES</span></span>

### <span data-ttu-id="19c33-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="19c33-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="19c33-109">Эта команда изменяет уровень надежности основного узла на серебро.</span><span class="sxs-lookup"><span data-stu-id="19c33-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="19c33-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19c33-110">PARAMETERS</span></span>

### <span data-ttu-id="19c33-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="19c33-111">-AutoAddNode</span></span>
<span data-ttu-id="19c33-112">Автоматическое добавление счетчика узлов при изменении надежности</span><span class="sxs-lookup"><span data-stu-id="19c33-112">Add node count automatically when changing reliability</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19c33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c33-113">-DefaultProfile</span></span>
<span data-ttu-id="19c33-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19c33-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19c33-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19c33-115">-Name</span></span>
<span data-ttu-id="19c33-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="19c33-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="19c33-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="19c33-117">-ReliabilityLevel</span></span>
<span data-ttu-id="19c33-118">Уровень надежности</span><span class="sxs-lookup"><span data-stu-id="19c33-118">Reliability tier</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19c33-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c33-119">-ResourceGroupName</span></span>
<span data-ttu-id="19c33-120">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19c33-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="19c33-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19c33-121">-Confirm</span></span>
<span data-ttu-id="19c33-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19c33-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c33-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c33-123">-WhatIf</span></span>
<span data-ttu-id="19c33-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19c33-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c33-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19c33-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c33-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c33-126">CommonParameters</span></span>
<span data-ttu-id="19c33-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19c33-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c33-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c33-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c33-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19c33-129">INPUTS</span></span>

### <span data-ttu-id="19c33-130">System. String</span><span class="sxs-lookup"><span data-stu-id="19c33-130">System.String</span></span>

### <span data-ttu-id="19c33-131">Microsoft. Azure. Commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="19c33-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="19c33-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="19c33-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="19c33-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19c33-133">OUTPUTS</span></span>

### <span data-ttu-id="19c33-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="19c33-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="19c33-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="19c33-135">NOTES</span></span>

## <span data-ttu-id="19c33-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19c33-136">RELATED LINKS</span></span>
