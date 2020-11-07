---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: b0630a1d7fee588716c4db493f9c5ead2003165c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729099"
---
# <span data-ttu-id="ebf1a-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="ebf1a-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="ebf1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebf1a-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf1a-103">Обновите уровень надежности основного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="ebf1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebf1a-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebf1a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebf1a-105">DESCRIPTION</span></span>
<span data-ttu-id="ebf1a-106">Используйте **Update-AzServiceFabricReliability** , чтобы обновить надежность типа основного узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="ebf1a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebf1a-107">EXAMPLES</span></span>

### <span data-ttu-id="ebf1a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebf1a-108">Example 1</span></span>
```
PS c:> Add-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="ebf1a-109">Эта команда изменяет уровень надежности основного узла на серебро.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="ebf1a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebf1a-110">PARAMETERS</span></span>

### <span data-ttu-id="ebf1a-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="ebf1a-111">-AutoAddNode</span></span>
<span data-ttu-id="ebf1a-112">Автоматическое добавление счетчика узлов при изменении надежности.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-112">Add node count automatically when changing reliability.</span></span>

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

### <span data-ttu-id="ebf1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf1a-113">-DefaultProfile</span></span>
<span data-ttu-id="ebf1a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebf1a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebf1a-115">-Name</span></span>
<span data-ttu-id="ebf1a-116">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ebf1a-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ebf1a-117">-ReliabilityLevel</span></span>
<span data-ttu-id="ebf1a-118">Уровень надежности.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-118">Reliability tier.</span></span>

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

### <span data-ttu-id="ebf1a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf1a-119">-ResourceGroupName</span></span>
<span data-ttu-id="ebf1a-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ebf1a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebf1a-121">-Confirm</span></span>
<span data-ttu-id="ebf1a-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebf1a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebf1a-123">-WhatIf</span></span>
<span data-ttu-id="ebf1a-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebf1a-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebf1a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf1a-126">CommonParameters</span></span>
<span data-ttu-id="ebf1a-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebf1a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf1a-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebf1a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf1a-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebf1a-129">INPUTS</span></span>

### <span data-ttu-id="ebf1a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ebf1a-130">System.String</span></span>

### <span data-ttu-id="ebf1a-131">Microsoft. Azure. Commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ebf1a-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="ebf1a-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ebf1a-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ebf1a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebf1a-133">OUTPUTS</span></span>

### <span data-ttu-id="ebf1a-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="ebf1a-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ebf1a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebf1a-135">NOTES</span></span>

## <span data-ttu-id="ebf1a-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebf1a-136">RELATED LINKS</span></span>
