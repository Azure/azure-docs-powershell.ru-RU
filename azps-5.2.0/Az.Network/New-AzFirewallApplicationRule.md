---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415095"
---
# <span data-ttu-id="ab689-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="ab689-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="ab689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab689-102">SYNOPSIS</span></span>
<span data-ttu-id="ab689-103">Создает правило брандмауэра приложения.</span><span class="sxs-lookup"><span data-stu-id="ab689-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="ab689-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ab689-104">SYNTAX</span></span>

### <span data-ttu-id="ab689-105">TargetFqdn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab689-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab689-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="ab689-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab689-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab689-107">DESCRIPTION</span></span>
<span data-ttu-id="ab689-108">Для брандмауэра Azure создается правило приложения **для new-AzFirewallApplicationRule.**</span><span class="sxs-lookup"><span data-stu-id="ab689-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="ab689-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ab689-109">EXAMPLES</span></span>

### <span data-ttu-id="ab689-110">Пример 1. Создание правила для разрешить весь трафик HTTPS с 10.0.0.0</span><span class="sxs-lookup"><span data-stu-id="ab689-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="ab689-111">В этом примере создается правило, которое разрешит весь трафик HTTPS в порте 443 с 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="ab689-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="ab689-112">Пример 2. Создание правила для подсети WindowsUpdate 10.0.0.0/24</span><span class="sxs-lookup"><span data-stu-id="ab689-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="ab689-113">В этом примере создается правило, которое будет разрешать трафик для обновления Windows для домена 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="ab689-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="ab689-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab689-114">PARAMETERS</span></span>

### <span data-ttu-id="ab689-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab689-115">-DefaultProfile</span></span>
<span data-ttu-id="ab689-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab689-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab689-117">-Description</span><span class="sxs-lookup"><span data-stu-id="ab689-117">-Description</span></span>
<span data-ttu-id="ab689-118">Указывает необязательное описание этого правила.</span><span class="sxs-lookup"><span data-stu-id="ab689-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="ab689-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="ab689-119">-FqdnTag</span></span>
<span data-ttu-id="ab689-120">Список тегов FQDN для этого правила.</span><span class="sxs-lookup"><span data-stu-id="ab689-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="ab689-121">Доступные теги можно извлечь с помощью [командлета Get-AzFirewallFqdnTag.](./Get-AzFirewallFqdnTag.md)</span><span class="sxs-lookup"><span data-stu-id="ab689-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

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

### <span data-ttu-id="ab689-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ab689-122">-Name</span></span>
<span data-ttu-id="ab689-123">Указывает имя этого правила приложения.</span><span class="sxs-lookup"><span data-stu-id="ab689-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="ab689-124">Имя должно быть уникальным в наборе правил.</span><span class="sxs-lookup"><span data-stu-id="ab689-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="ab689-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ab689-125">-Protocol</span></span>
<span data-ttu-id="ab689-126">Определяет тип трафика, отфильтрованного этим правилом.</span><span class="sxs-lookup"><span data-stu-id="ab689-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="ab689-127">Формат: <protocol type> <port> .</span><span class="sxs-lookup"><span data-stu-id="ab689-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="ab689-128">Например, http:80 или https:443.</span><span class="sxs-lookup"><span data-stu-id="ab689-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="ab689-129">Протокол является обязательным, если используется TargetFqdn, но его нельзя использовать с FqdnTag.</span><span class="sxs-lookup"><span data-stu-id="ab689-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="ab689-130">Поддерживаются протоколы HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ab689-130">The supported protocols are HTTP and HTTPS.</span></span>

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

### <span data-ttu-id="ab689-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="ab689-131">-SourceAddress</span></span>
<span data-ttu-id="ab689-132">Исходные адреса правила</span><span class="sxs-lookup"><span data-stu-id="ab689-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="ab689-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="ab689-133">-SourceIpGroup</span></span>
<span data-ttu-id="ab689-134">Ipgroup-источник правила</span><span class="sxs-lookup"><span data-stu-id="ab689-134">The source ipgroup of the rule</span></span>

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

### <span data-ttu-id="ab689-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="ab689-135">-TargetFqdn</span></span>
<span data-ttu-id="ab689-136">Список доменных имен, отфильтрованный этим правилом.</span><span class="sxs-lookup"><span data-stu-id="ab689-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="ab689-137">Звездочка (') принимается в списке только как первый символ *FQDN. При этом звездочка соответствует любому количеству символов. (Например, 'msn.com'* будет соответствовать msn.com и всем его поддоменам)</span><span class="sxs-lookup"><span data-stu-id="ab689-137">The asterisk character, '*', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

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

### <span data-ttu-id="ab689-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab689-138">-Confirm</span></span>
<span data-ttu-id="ab689-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ab689-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab689-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab689-140">-WhatIf</span></span>
<span data-ttu-id="ab689-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab689-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab689-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ab689-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab689-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab689-143">CommonParameters</span></span>
<span data-ttu-id="ab689-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab689-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab689-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab689-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab689-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab689-146">INPUTS</span></span>

### <span data-ttu-id="ab689-147">Нет</span><span class="sxs-lookup"><span data-stu-id="ab689-147">None</span></span>

## <span data-ttu-id="ab689-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab689-148">OUTPUTS</span></span>

### <span data-ttu-id="ab689-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="ab689-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="ab689-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ab689-150">NOTES</span></span>

## <span data-ttu-id="ab689-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab689-151">RELATED LINKS</span></span>

[<span data-ttu-id="ab689-152">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ab689-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="ab689-153">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ab689-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="ab689-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ab689-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="ab689-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="ab689-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)
