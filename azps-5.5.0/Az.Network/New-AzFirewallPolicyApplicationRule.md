---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 25a81344d9d8d5b8af8eed907bce7977408515ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218569"
---
# <span data-ttu-id="04387-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="04387-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="04387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04387-102">SYNOPSIS</span></span>
<span data-ttu-id="04387-103">Создание правила политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="04387-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="04387-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="04387-104">SYNTAX</span></span>

### <span data-ttu-id="04387-105">SourceAddressAndTargetFqdn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04387-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04387-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="04387-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04387-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="04387-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04387-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="04387-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04387-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="04387-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04387-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="04387-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04387-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="04387-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04387-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="04387-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04387-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04387-113">DESCRIPTION</span></span>
<span data-ttu-id="04387-114">С **помощью cmdlet New-AzFirewallPolicyApplicationRule** создается правило приложения для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="04387-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="04387-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="04387-115">EXAMPLES</span></span>

### <span data-ttu-id="04387-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="04387-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="04387-117">В этом примере создается правило приложения с исходным адресом, протоколом и целевыми fqdns.</span><span class="sxs-lookup"><span data-stu-id="04387-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="04387-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="04387-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="04387-119">В этом примере создается правило приложения с исходным адресом, протоколом и веб-категориями.</span><span class="sxs-lookup"><span data-stu-id="04387-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="04387-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04387-120">PARAMETERS</span></span>

### <span data-ttu-id="04387-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04387-121">-DefaultProfile</span></span>
<span data-ttu-id="04387-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04387-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04387-123">-Description</span><span class="sxs-lookup"><span data-stu-id="04387-123">-Description</span></span>
<span data-ttu-id="04387-124">Описание правила</span><span class="sxs-lookup"><span data-stu-id="04387-124">The description of the rule</span></span>

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

### <span data-ttu-id="04387-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="04387-125">-FqdnTag</span></span>
<span data-ttu-id="04387-126">Теги FQDN правила</span><span class="sxs-lookup"><span data-stu-id="04387-126">The FQDN Tags of the rule</span></span>

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

### <span data-ttu-id="04387-127">-Name</span><span class="sxs-lookup"><span data-stu-id="04387-127">-Name</span></span>
<span data-ttu-id="04387-128">Имя правила приложения</span><span class="sxs-lookup"><span data-stu-id="04387-128">The name of the Application Rule</span></span>

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

### <span data-ttu-id="04387-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="04387-129">-Protocol</span></span>
<span data-ttu-id="04387-130">Протоколы правила</span><span class="sxs-lookup"><span data-stu-id="04387-130">The protocols of the rule</span></span>

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

### <span data-ttu-id="04387-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="04387-131">-SourceAddress</span></span>
<span data-ttu-id="04387-132">Исходные адреса правила</span><span class="sxs-lookup"><span data-stu-id="04387-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="04387-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="04387-133">-SourceIpGroup</span></span>
<span data-ttu-id="04387-134">Исходные IP-группы правила</span><span class="sxs-lookup"><span data-stu-id="04387-134">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="04387-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="04387-135">-TargetFqdn</span></span>
<span data-ttu-id="04387-136">Целевые FQDNs правила</span><span class="sxs-lookup"><span data-stu-id="04387-136">The target FQDNs of the rule</span></span>

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

### <span data-ttu-id="04387-137">-WebCategory</span><span class="sxs-lookup"><span data-stu-id="04387-137">-WebCategory</span></span>
<span data-ttu-id="04387-138">Веб-категории правила</span><span class="sxs-lookup"><span data-stu-id="04387-138">The Web Categories of the rule</span></span>

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

### <span data-ttu-id="04387-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="04387-139">-TargetUrl</span></span>
<span data-ttu-id="04387-140">Url-адрес конечного правила</span><span class="sxs-lookup"><span data-stu-id="04387-140">The Target Url of the rule</span></span>

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

### <span data-ttu-id="04387-141">-TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="04387-141">-TerminateTLS</span></span>
<span data-ttu-id="04387-142">Указывает на прекращение TLS</span><span class="sxs-lookup"><span data-stu-id="04387-142">Indicates terminating TLS</span></span>

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

### <span data-ttu-id="04387-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04387-143">CommonParameters</span></span>
<span data-ttu-id="04387-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04387-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04387-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04387-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04387-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04387-146">INPUTS</span></span>

### <span data-ttu-id="04387-147">Нет</span><span class="sxs-lookup"><span data-stu-id="04387-147">None</span></span>

## <span data-ttu-id="04387-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="04387-148">OUTPUTS</span></span>

### <span data-ttu-id="04387-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="04387-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="04387-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="04387-150">NOTES</span></span>

## <span data-ttu-id="04387-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04387-151">RELATED LINKS</span></span>
