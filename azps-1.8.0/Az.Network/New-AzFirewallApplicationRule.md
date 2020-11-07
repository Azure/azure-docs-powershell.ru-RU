---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: 6aad78a873b1eb24f1534c9b8c0b38d1567ee2ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730344"
---
# <span data-ttu-id="1e4cc-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="1e4cc-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="1e4cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e4cc-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4cc-103">Создание правила брандмауэра для приложения.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="1e4cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e4cc-104">SYNTAX</span></span>

### <span data-ttu-id="1e4cc-105">TargetFqdn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e4cc-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e4cc-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="1e4cc-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e4cc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e4cc-107">DESCRIPTION</span></span>
<span data-ttu-id="1e4cc-108">Командлет **New-AzFirewallApplicationRule** создает правило приложения для брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="1e4cc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e4cc-109">EXAMPLES</span></span>

### <span data-ttu-id="1e4cc-110">1: Создайте правило, разрешающее весь трафик HTTPS из 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="1e4cc-111">В этом примере создается правило, которое позволит включить весь трафик HTTPS для порта 443 из 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="1e4cc-112">2. Создание правила для разрешения WindowsUpdate для подсети 10.0.0.0/24</span><span class="sxs-lookup"><span data-stu-id="1e4cc-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="1e4cc-113">В этом примере создается правило, которое позволит получить трафик для обновлений Windows для домена 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="1e4cc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e4cc-114">PARAMETERS</span></span>

### <span data-ttu-id="1e4cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4cc-115">-DefaultProfile</span></span>
<span data-ttu-id="1e4cc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e4cc-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="1e4cc-117">-Description</span></span>
<span data-ttu-id="1e4cc-118">Задает необязательное описание этого правила.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-118">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cc-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="1e4cc-119">-FqdnTag</span></span>
<span data-ttu-id="1e4cc-120">Задает список тегов полного доменного имени для этого правила.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="1e4cc-121">Доступные теги можно получить с помощью командлета [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) .</span><span class="sxs-lookup"><span data-stu-id="1e4cc-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cc-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e4cc-122">-Name</span></span>
<span data-ttu-id="1e4cc-123">Задает имя этого правила приложения.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="1e4cc-124">Имя должно быть уникальным в пределах коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-124">The name must be unique inside a rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cc-125">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="1e4cc-125">-Protocol</span></span>
<span data-ttu-id="1e4cc-126">Указывает тип трафика для фильтрации с помощью этого правила.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="1e4cc-127">Формат <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="1e4cc-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="1e4cc-128">Например, "http: 80" или "https: 443".</span><span class="sxs-lookup"><span data-stu-id="1e4cc-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="1e4cc-129">Протокол является обязательным при использовании TargetFqdn, но его нельзя использовать с FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="1e4cc-130">Поддерживаются протоколы HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cc-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="1e4cc-131">-SourceAddress</span></span>
<span data-ttu-id="1e4cc-132">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cc-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="1e4cc-133">-TargetFqdn</span></span>
<span data-ttu-id="1e4cc-134">Указывает список доменных имен, отфильтрованных с помощью этого правила.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="1e4cc-135">Символ звездочек, " *", принимается только в качестве первого символа полного доменного имени в списке. При использовании звездочек соответствует любому количеству символов. (например, "* MSN.com" будет соответствовать MSN.com и всем его дочерним доменам)</span><span class="sxs-lookup"><span data-stu-id="1e4cc-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cc-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e4cc-136">-Confirm</span></span>
<span data-ttu-id="1e4cc-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e4cc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e4cc-138">-WhatIf</span></span>
<span data-ttu-id="1e4cc-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e4cc-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e4cc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4cc-141">CommonParameters</span></span>
<span data-ttu-id="1e4cc-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e4cc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4cc-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e4cc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4cc-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e4cc-144">INPUTS</span></span>

### <span data-ttu-id="1e4cc-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="1e4cc-145">None</span></span>

## <span data-ttu-id="1e4cc-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e4cc-146">OUTPUTS</span></span>

### <span data-ttu-id="1e4cc-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="1e4cc-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="1e4cc-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e4cc-148">NOTES</span></span>

## <span data-ttu-id="1e4cc-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e4cc-149">RELATED LINKS</span></span>

[<span data-ttu-id="1e4cc-150">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1e4cc-150">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="1e4cc-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1e4cc-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="1e4cc-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1e4cc-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="1e4cc-153">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="1e4cc-153">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
