---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 0c7e29b0c9b59842e885cf8763da63c2d65cfff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001112"
---
# <span data-ttu-id="e272f-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e272f-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="e272f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e272f-102">SYNOPSIS</span></span>
<span data-ttu-id="e272f-103">Создание правила политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="e272f-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="e272f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e272f-104">SYNTAX</span></span>

### <span data-ttu-id="e272f-105">SourceAddressAndTargetFqdn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e272f-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e272f-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="e272f-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e272f-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="e272f-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e272f-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="e272f-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e272f-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="e272f-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e272f-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="e272f-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e272f-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="e272f-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e272f-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="e272f-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e272f-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e272f-113">DESCRIPTION</span></span>
<span data-ttu-id="e272f-114">Для политики брандмауэра Azure создается правило приложения **для** политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="e272f-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="e272f-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e272f-115">EXAMPLES</span></span>

### <span data-ttu-id="e272f-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e272f-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="e272f-117">В этом примере создается правило приложения с исходным адресом, протоколом и целевыми fqdns.</span><span class="sxs-lookup"><span data-stu-id="e272f-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="e272f-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e272f-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="e272f-119">В этом примере создается правило приложения с исходным адресом, протоколом и веб-категориями.</span><span class="sxs-lookup"><span data-stu-id="e272f-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="e272f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e272f-120">PARAMETERS</span></span>

### <span data-ttu-id="e272f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e272f-121">-DefaultProfile</span></span>
<span data-ttu-id="e272f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e272f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e272f-123">-Description</span><span class="sxs-lookup"><span data-stu-id="e272f-123">-Description</span></span>
<span data-ttu-id="e272f-124">Описание правила</span><span class="sxs-lookup"><span data-stu-id="e272f-124">The description of the rule</span></span>

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

### <span data-ttu-id="e272f-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="e272f-125">-FqdnTag</span></span>
<span data-ttu-id="e272f-126">Теги FQDN правила</span><span class="sxs-lookup"><span data-stu-id="e272f-126">The FQDN Tags of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndFqdnTag, SourceIpGroupAndFqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e272f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e272f-127">-Name</span></span>
<span data-ttu-id="e272f-128">Имя правила приложения</span><span class="sxs-lookup"><span data-stu-id="e272f-128">The name of the Application Rule</span></span>

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

### <span data-ttu-id="e272f-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e272f-129">-Protocol</span></span>
<span data-ttu-id="e272f-130">Протоколы правила</span><span class="sxs-lookup"><span data-stu-id="e272f-130">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndWebCategory, SourceIpGroupAndTargetFqdn, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e272f-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e272f-131">-SourceAddress</span></span>
<span data-ttu-id="e272f-132">Исходные адреса правила</span><span class="sxs-lookup"><span data-stu-id="e272f-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndFqdnTag, SourceAddressAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e272f-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="e272f-133">-SourceIpGroup</span></span>
<span data-ttu-id="e272f-134">Исходные IP-группы правила</span><span class="sxs-lookup"><span data-stu-id="e272f-134">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTargetFqdn, SourceIpGroupAndFqdnTag, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e272f-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="e272f-135">-TargetFqdn</span></span>
<span data-ttu-id="e272f-136">Целевые FQDNs правила</span><span class="sxs-lookup"><span data-stu-id="e272f-136">The target FQDNs of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceIpGroupAndTargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e272f-137">-WebCategory</span><span class="sxs-lookup"><span data-stu-id="e272f-137">-WebCategory</span></span>
<span data-ttu-id="e272f-138">Веб-категории правила</span><span class="sxs-lookup"><span data-stu-id="e272f-138">The Web Categories of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndWebCategory, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e272f-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="e272f-139">-TargetUrl</span></span>
<span data-ttu-id="e272f-140">Url-адрес конечного правила</span><span class="sxs-lookup"><span data-stu-id="e272f-140">The Target Url of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetUrl, SourceIpGroupAndTargetUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e272f-141">-TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="e272f-141">-TerminateTLS</span></span>
<span data-ttu-id="e272f-142">Указывает на прекращение TLS</span><span class="sxs-lookup"><span data-stu-id="e272f-142">Indicates terminating TLS</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e272f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e272f-143">CommonParameters</span></span>
<span data-ttu-id="e272f-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e272f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e272f-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e272f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e272f-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e272f-146">INPUTS</span></span>

### <span data-ttu-id="e272f-147">Нет</span><span class="sxs-lookup"><span data-stu-id="e272f-147">None</span></span>

## <span data-ttu-id="e272f-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e272f-148">OUTPUTS</span></span>

### <span data-ttu-id="e272f-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e272f-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="e272f-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e272f-150">NOTES</span></span>

## <span data-ttu-id="e272f-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e272f-151">RELATED LINKS</span></span>
