---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734616"
---
# <span data-ttu-id="9c92c-101">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="9c92c-101">New-AzureRmFirewallApplicationRule</span></span>

## <span data-ttu-id="9c92c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c92c-102">SYNOPSIS</span></span>
<span data-ttu-id="9c92c-103">Создание правила брандмауэра для приложения.</span><span class="sxs-lookup"><span data-stu-id="9c92c-103">Creates a Firewall Application Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c92c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c92c-104">SYNTAX</span></span>

### <span data-ttu-id="9c92c-105">TargetFqdn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c92c-105">TargetFqdn (Default)</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c92c-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="9c92c-106">FqdnTag</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c92c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c92c-107">DESCRIPTION</span></span>
<span data-ttu-id="9c92c-108">Командлет **New-AzureRmFirewallApplicationRule** создает правило приложения для брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="9c92c-108">The **New-AzureRmFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="9c92c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c92c-109">EXAMPLES</span></span>

### <span data-ttu-id="9c92c-110">1: Создайте правило, разрешающее весь трафик HTTPS из 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="9c92c-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="9c92c-111">В этом примере создается правило, которое позволит включить весь трафик HTTPS для порта 443 из 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="9c92c-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="9c92c-112">2. Создание правила для разрешения WindowsUpdate для подсети 10.0.0.0/24</span><span class="sxs-lookup"><span data-stu-id="9c92c-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="9c92c-113">В этом примере создается правило, которое позволит получить трафик для обновлений Windows для домена 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="9c92c-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="9c92c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c92c-114">PARAMETERS</span></span>

### <span data-ttu-id="9c92c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c92c-115">-DefaultProfile</span></span>
<span data-ttu-id="9c92c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c92c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c92c-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="9c92c-117">-Description</span></span>
<span data-ttu-id="9c92c-118">Задает необязательное описание этого правила.</span><span class="sxs-lookup"><span data-stu-id="9c92c-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="9c92c-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="9c92c-119">-FqdnTag</span></span>
<span data-ttu-id="9c92c-120">Задает список тегов полного доменного имени для этого правила.</span><span class="sxs-lookup"><span data-stu-id="9c92c-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="9c92c-121">Доступные теги можно получить с помощью командлета [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) .</span><span class="sxs-lookup"><span data-stu-id="9c92c-121">The available tags can be retrieved using [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c92c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c92c-122">-Name</span></span>
<span data-ttu-id="9c92c-123">Задает имя этого правила приложения.</span><span class="sxs-lookup"><span data-stu-id="9c92c-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="9c92c-124">Имя должно быть уникальным в пределах коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="9c92c-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="9c92c-125">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="9c92c-125">-Protocol</span></span>
<span data-ttu-id="9c92c-126">Указывает тип трафика для фильтрации с помощью этого правила.</span><span class="sxs-lookup"><span data-stu-id="9c92c-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="9c92c-127">Формат <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="9c92c-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="9c92c-128">Например, "http: 80" или "https: 443".</span><span class="sxs-lookup"><span data-stu-id="9c92c-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="9c92c-129">Протокол является обязательным при использовании TargetFqdn, но его нельзя использовать с FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="9c92c-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="9c92c-130">Поддерживаются протоколы HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9c92c-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c92c-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="9c92c-131">-SourceAddress</span></span>
<span data-ttu-id="9c92c-132">Исходные адреса правила.</span><span class="sxs-lookup"><span data-stu-id="9c92c-132">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c92c-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="9c92c-133">-TargetFqdn</span></span>
<span data-ttu-id="9c92c-134">Указывает список доменных имен, отфильтрованных с помощью этого правила.</span><span class="sxs-lookup"><span data-stu-id="9c92c-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="9c92c-135">Символ звездочек, " *", принимается только в качестве первого символа полного доменного имени в списке. При использовании звездочек соответствует любому количеству символов. (например, "* MSN.com" будет соответствовать MSN.com и всем его дочерним доменам)</span><span class="sxs-lookup"><span data-stu-id="9c92c-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c92c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c92c-136">-Confirm</span></span>
<span data-ttu-id="9c92c-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c92c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c92c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c92c-138">-WhatIf</span></span>
<span data-ttu-id="9c92c-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c92c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c92c-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c92c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c92c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c92c-141">CommonParameters</span></span>
<span data-ttu-id="9c92c-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c92c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c92c-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c92c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c92c-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c92c-144">INPUTS</span></span>

### <span data-ttu-id="9c92c-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="9c92c-145">None</span></span>
<span data-ttu-id="9c92c-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9c92c-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c92c-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c92c-147">OUTPUTS</span></span>

### <span data-ttu-id="9c92c-148">Microsoft. Azure. Commands. Network. Models. PSFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="9c92c-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRule</span></span>

## <span data-ttu-id="9c92c-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c92c-149">NOTES</span></span>

## <span data-ttu-id="9c92c-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c92c-150">RELATED LINKS</span></span>

[<span data-ttu-id="9c92c-151">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9c92c-151">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="9c92c-152">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9c92c-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="9c92c-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9c92c-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="9c92c-154">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="9c92c-154">Get-AzureRmFirewallFqdnTag</span></span>](./Get-AzureRmFirewallFqdnTag.md)
