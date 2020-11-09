---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: aaf6e2006797a99d37bf5ece341863c34038a3dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248118"
---
# <span data-ttu-id="07b75-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="07b75-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="07b75-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07b75-102">SYNOPSIS</span></span>
<span data-ttu-id="07b75-103">Создание правила применения политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="07b75-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="07b75-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07b75-104">SYNTAX</span></span>

### <span data-ttu-id="07b75-105">TargetFqdn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07b75-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07b75-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="07b75-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07b75-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07b75-107">DESCRIPTION</span></span>
<span data-ttu-id="07b75-108">Командлет **New-AzFirewallPolicyApplicationRule** создает правило приложения для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="07b75-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="07b75-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07b75-109">EXAMPLES</span></span>

### <span data-ttu-id="07b75-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="07b75-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="07b75-111">В этом примере создается правило приложения с исходным адресом, протоколом и целевыми доменными именами.</span><span class="sxs-lookup"><span data-stu-id="07b75-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="07b75-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="07b75-112">Example 2</span></span>

<span data-ttu-id="07b75-113">Создайте новое правило применения политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="07b75-113">Create a new Azure Firewall Policy Application Rule.</span></span> <span data-ttu-id="07b75-114">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="07b75-114">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzFirewallPolicyApplicationRule -Description 'Allow web service' -Name AR1 -Protocol 'http:80' -SourceAddress '192.168.0.0/16' -TargetFqdn '*.ro'
```

## <span data-ttu-id="07b75-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07b75-115">PARAMETERS</span></span>

### <span data-ttu-id="07b75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b75-116">-DefaultProfile</span></span>
<span data-ttu-id="07b75-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07b75-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07b75-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="07b75-118">-Description</span></span>
<span data-ttu-id="07b75-119">Описание правила.</span><span class="sxs-lookup"><span data-stu-id="07b75-119">The description of the rule</span></span>

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

### <span data-ttu-id="07b75-120">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="07b75-120">-FqdnTag</span></span>
<span data-ttu-id="07b75-121">Теги полного доменного имени для правила.</span><span class="sxs-lookup"><span data-stu-id="07b75-121">The FQDN Tags of the rule</span></span>

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

### <span data-ttu-id="07b75-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07b75-122">-Name</span></span>
<span data-ttu-id="07b75-123">Имя правила приложения.</span><span class="sxs-lookup"><span data-stu-id="07b75-123">The name of the Application Rule</span></span>

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

### <span data-ttu-id="07b75-124">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="07b75-124">-Protocol</span></span>
<span data-ttu-id="07b75-125">Протоколы правила.</span><span class="sxs-lookup"><span data-stu-id="07b75-125">The protocols of the rule</span></span>

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

### <span data-ttu-id="07b75-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="07b75-126">-SourceAddress</span></span>
<span data-ttu-id="07b75-127">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="07b75-127">The source addresses of the rule</span></span>

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

### <span data-ttu-id="07b75-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="07b75-128">-SourceIpGroup</span></span>
<span data-ttu-id="07b75-129">Исходная ipgroups правила</span><span class="sxs-lookup"><span data-stu-id="07b75-129">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="07b75-130">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="07b75-130">-TargetFqdn</span></span>
<span data-ttu-id="07b75-131">Целевые полные доменные имена для правила.</span><span class="sxs-lookup"><span data-stu-id="07b75-131">The target FQDNs of the rule</span></span>

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

### <span data-ttu-id="07b75-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07b75-132">-Confirm</span></span>
<span data-ttu-id="07b75-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="07b75-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07b75-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07b75-134">-WhatIf</span></span>
<span data-ttu-id="07b75-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="07b75-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07b75-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="07b75-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07b75-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b75-137">CommonParameters</span></span>
<span data-ttu-id="07b75-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07b75-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b75-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07b75-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b75-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07b75-140">INPUTS</span></span>

### <span data-ttu-id="07b75-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="07b75-141">None</span></span>

## <span data-ttu-id="07b75-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07b75-142">OUTPUTS</span></span>

### <span data-ttu-id="07b75-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="07b75-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="07b75-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="07b75-144">NOTES</span></span>

## <span data-ttu-id="07b75-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07b75-145">RELATED LINKS</span></span>