---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 1b9fd10e11cb283f880979e7e4a5d703521c9a87
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911721"
---
# <span data-ttu-id="e71cb-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e71cb-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="e71cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e71cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e71cb-103">Создание правила применения политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="e71cb-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="e71cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e71cb-104">SYNTAX</span></span>

### <span data-ttu-id="e71cb-105">TargetFqdn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e71cb-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e71cb-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="e71cb-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e71cb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e71cb-107">DESCRIPTION</span></span>
<span data-ttu-id="e71cb-108">Командлет **New-AzFirewallPolicyApplicationRule** создает правило приложения для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="e71cb-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="e71cb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e71cb-109">EXAMPLES</span></span>

### <span data-ttu-id="e71cb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e71cb-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="e71cb-111">В этом примере создается правило приложения с исходным адресом, протоколом и целевыми доменными именами.</span><span class="sxs-lookup"><span data-stu-id="e71cb-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

## <span data-ttu-id="e71cb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e71cb-112">PARAMETERS</span></span>

### <span data-ttu-id="e71cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71cb-113">-DefaultProfile</span></span>
<span data-ttu-id="e71cb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e71cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71cb-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="e71cb-115">-Description</span></span>
<span data-ttu-id="e71cb-116">Описание правила.</span><span class="sxs-lookup"><span data-stu-id="e71cb-116">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71cb-117">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="e71cb-117">-FqdnTag</span></span>
<span data-ttu-id="e71cb-118">Теги полного доменного имени для правила.</span><span class="sxs-lookup"><span data-stu-id="e71cb-118">The FQDN Tags of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71cb-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e71cb-119">-Name</span></span>
<span data-ttu-id="e71cb-120">Имя правила приложения.</span><span class="sxs-lookup"><span data-stu-id="e71cb-120">The name of the Application Rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71cb-121">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="e71cb-121">-Protocol</span></span>
<span data-ttu-id="e71cb-122">Протоколы правила.</span><span class="sxs-lookup"><span data-stu-id="e71cb-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71cb-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e71cb-123">-SourceAddress</span></span>
<span data-ttu-id="e71cb-124">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="e71cb-124">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71cb-125">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="e71cb-125">-TargetFqdn</span></span>
<span data-ttu-id="e71cb-126">Целевые полные доменные имена для правила.</span><span class="sxs-lookup"><span data-stu-id="e71cb-126">The target FQDNs of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e71cb-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e71cb-127">-Confirm</span></span>
<span data-ttu-id="e71cb-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e71cb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e71cb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e71cb-129">-WhatIf</span></span>
<span data-ttu-id="e71cb-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e71cb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e71cb-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e71cb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e71cb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71cb-132">CommonParameters</span></span>
<span data-ttu-id="e71cb-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e71cb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71cb-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e71cb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71cb-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e71cb-135">INPUTS</span></span>

### <span data-ttu-id="e71cb-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="e71cb-136">None</span></span>

## <span data-ttu-id="e71cb-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e71cb-137">OUTPUTS</span></span>

### <span data-ttu-id="e71cb-138">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e71cb-138">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="e71cb-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e71cb-139">NOTES</span></span>

## <span data-ttu-id="e71cb-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e71cb-140">RELATED LINKS</span></span>
