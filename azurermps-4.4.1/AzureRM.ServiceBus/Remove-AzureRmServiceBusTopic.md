---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 356140c964280634f469dd9b9955adaf62130090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559507"
---
# <span data-ttu-id="0aa02-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="0aa02-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="0aa02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0aa02-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa02-103">Удаляет раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="0aa02-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aa02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0aa02-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0aa02-105">DESCRIPTION</span></span>
<span data-ttu-id="0aa02-106">Командлет **Remove-AzureRmServiceBusTopic** удаляет раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="0aa02-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0aa02-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0aa02-107">EXAMPLES</span></span>

### <span data-ttu-id="0aa02-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0aa02-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="0aa02-109">Удаляет раздел `SB-Topic_exampl1` из пространства имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="0aa02-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="0aa02-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0aa02-110">PARAMETERS</span></span>

### <span data-ttu-id="0aa02-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0aa02-111">-Confirm</span></span>
<span data-ttu-id="0aa02-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0aa02-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa02-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa02-113">-WhatIf</span></span>
<span data-ttu-id="0aa02-114">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0aa02-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aa02-115">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0aa02-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa02-116">-DefaultProfile</span></span>
<span data-ttu-id="0aa02-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa02-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aa02-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0aa02-118">-Name</span></span>
<span data-ttu-id="0aa02-119">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="0aa02-119">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aa02-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0aa02-120">-Namespace</span></span>
<span data-ttu-id="0aa02-121">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="0aa02-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aa02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aa02-122">-ResourceGroupName</span></span>
<span data-ttu-id="0aa02-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0aa02-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aa02-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa02-124">CommonParameters</span></span>
<span data-ttu-id="0aa02-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0aa02-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa02-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aa02-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa02-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0aa02-127">INPUTS</span></span>

### <span data-ttu-id="0aa02-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0aa02-128">-ResourceGroup</span></span>
 <span data-ttu-id="0aa02-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0aa02-129">System.String</span></span>

### <span data-ttu-id="0aa02-130">-+ +</span><span class="sxs-lookup"><span data-stu-id="0aa02-130">-NamespaceName</span></span>
 <span data-ttu-id="0aa02-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0aa02-131">System.String</span></span>

### <span data-ttu-id="0aa02-132">-TopicName</span><span class="sxs-lookup"><span data-stu-id="0aa02-132">-TopicName</span></span>
 <span data-ttu-id="0aa02-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0aa02-133">System.String</span></span>

## <span data-ttu-id="0aa02-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0aa02-134">OUTPUTS</span></span>

### <span data-ttu-id="0aa02-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="0aa02-135">System.Object</span></span>

## <span data-ttu-id="0aa02-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0aa02-136">NOTES</span></span>

## <span data-ttu-id="0aa02-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0aa02-137">RELATED LINKS</span></span>

