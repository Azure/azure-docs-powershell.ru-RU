---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: c8ee3324f7f6e7653d86bef747bdb9831982474e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562119"
---
# <span data-ttu-id="0afe4-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="0afe4-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="0afe4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0afe4-102">SYNOPSIS</span></span>
<span data-ttu-id="0afe4-103">Обновите уровень надежности основного типа узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="0afe4-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0afe4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0afe4-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0afe4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0afe4-105">DESCRIPTION</span></span>
<span data-ttu-id="0afe4-106">Используйте **Update-AzureRmServiceFabricReliability** , чтобы обновить надежность типа основного узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="0afe4-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="0afe4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0afe4-107">EXAMPLES</span></span>

### <span data-ttu-id="0afe4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0afe4-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="0afe4-109">Эта команда изменяет уровень надежности основного узла на серебро.</span><span class="sxs-lookup"><span data-stu-id="0afe4-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="0afe4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0afe4-110">PARAMETERS</span></span>

### <span data-ttu-id="0afe4-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="0afe4-111">-AutoAddNode</span></span>
<span data-ttu-id="0afe4-112">Автоматическое добавление счетчика узлов при изменении надежности.</span><span class="sxs-lookup"><span data-stu-id="0afe4-112">Add node count automatically when changing reliability.</span></span>

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

### <span data-ttu-id="0afe4-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0afe4-113">-Name</span></span>
<span data-ttu-id="0afe4-114">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="0afe4-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0afe4-115">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="0afe4-115">-ReliabilityLevel</span></span>
<span data-ttu-id="0afe4-116">Уровень надежности.</span><span class="sxs-lookup"><span data-stu-id="0afe4-116">Reliability tier.</span></span>

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

### <span data-ttu-id="0afe4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afe4-117">-ResourceGroupName</span></span>
<span data-ttu-id="0afe4-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0afe4-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0afe4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0afe4-119">-Confirm</span></span>
<span data-ttu-id="0afe4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0afe4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0afe4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0afe4-121">-WhatIf</span></span>
<span data-ttu-id="0afe4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0afe4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0afe4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0afe4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0afe4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afe4-124">-DefaultProfile</span></span>
<span data-ttu-id="0afe4-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0afe4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0afe4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afe4-126">CommonParameters</span></span>
<span data-ttu-id="0afe4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0afe4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afe4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0afe4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afe4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0afe4-129">INPUTS</span></span>

### <span data-ttu-id="0afe4-130">Microsoft. Azure. Commands. ServiceFabric. Models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="0afe4-130">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="0afe4-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0afe4-131">System.Management.Automation.SwitchParameter</span></span>

<span data-ttu-id="0afe4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0afe4-132">System.String</span></span>

## <span data-ttu-id="0afe4-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0afe4-133">OUTPUTS</span></span>

### <span data-ttu-id="0afe4-134">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="0afe4-134">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="0afe4-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="0afe4-135">NOTES</span></span>

## <span data-ttu-id="0afe4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0afe4-136">RELATED LINKS</span></span>

