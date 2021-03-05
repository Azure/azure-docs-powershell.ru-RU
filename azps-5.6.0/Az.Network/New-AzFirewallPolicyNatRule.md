---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 2ba006beef1c698c12086ef65efca0213920092c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987790"
---
# <span data-ttu-id="dc127-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="dc127-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="dc127-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc127-102">SYNOPSIS</span></span>
<span data-ttu-id="dc127-103">Создание правила nat политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="dc127-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="dc127-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc127-104">SYNTAX</span></span>

### <span data-ttu-id="dc127-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="dc127-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc127-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="dc127-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc127-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="dc127-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc127-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="dc127-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc127-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc127-109">DESCRIPTION</span></span>
<span data-ttu-id="dc127-110">Для политики брандмауэра **Azure** создается правило NAT для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="dc127-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="dc127-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc127-111">EXAMPLES</span></span>

### <span data-ttu-id="dc127-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc127-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="dc127-113">В этом примере создается правило NAT с исходным адресом, протоколом, адресом назначения, портом назначения, переведенным адресом и переведенным портом.</span><span class="sxs-lookup"><span data-stu-id="dc127-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="dc127-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dc127-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="dc127-115">В этом примере создается правило NAT с исходным адресом, протоколом, адресом назначения, портом назначения, переведенным fqdn и переведенным портом.</span><span class="sxs-lookup"><span data-stu-id="dc127-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="dc127-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc127-116">PARAMETERS</span></span>

### <span data-ttu-id="dc127-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc127-117">-DefaultProfile</span></span>
<span data-ttu-id="dc127-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc127-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc127-119">-Description</span><span class="sxs-lookup"><span data-stu-id="dc127-119">-Description</span></span>
<span data-ttu-id="dc127-120">Описание правила</span><span class="sxs-lookup"><span data-stu-id="dc127-120">The description of the rule</span></span>

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

### <span data-ttu-id="dc127-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="dc127-121">-DestinationAddress</span></span>
<span data-ttu-id="dc127-122">Адреса назначения правила.</span><span class="sxs-lookup"><span data-stu-id="dc127-122">The destination addresses of the rule.</span></span> <span data-ttu-id="dc127-123">Это должен быть общедоступный IP-адрес брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="dc127-123">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc127-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="dc127-124">-DestinationPort</span></span>
<span data-ttu-id="dc127-125">Порты назначения правила</span><span class="sxs-lookup"><span data-stu-id="dc127-125">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc127-126">-Name</span><span class="sxs-lookup"><span data-stu-id="dc127-126">-Name</span></span>
<span data-ttu-id="dc127-127">Имя коллекции правил NAT</span><span class="sxs-lookup"><span data-stu-id="dc127-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="dc127-128">-Protocol</span><span class="sxs-lookup"><span data-stu-id="dc127-128">-Protocol</span></span>
<span data-ttu-id="dc127-129">Протоколы правила</span><span class="sxs-lookup"><span data-stu-id="dc127-129">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc127-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="dc127-130">-SourceAddress</span></span>
<span data-ttu-id="dc127-131">Исходные адреса правила</span><span class="sxs-lookup"><span data-stu-id="dc127-131">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTranslatedAddress, SourceAddressAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc127-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="dc127-132">-SourceIpGroup</span></span>
<span data-ttu-id="dc127-133">Исходные IP-группы правила</span><span class="sxs-lookup"><span data-stu-id="dc127-133">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTranslatedAddress, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc127-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="dc127-134">-TranslatedAddress</span></span>
<span data-ttu-id="dc127-135">Переведенный адрес для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="dc127-135">The translated address for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedAddress, SourceIpGroupAndTranslatedAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc127-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="dc127-136">-TranslatedFqdn</span></span>
<span data-ttu-id="dc127-137">Переведенное FQDN для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="dc127-137">The translated FQDN for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedFqdn, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc127-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="dc127-138">-TranslatedPort</span></span>
<span data-ttu-id="dc127-139">Переведенный порт для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="dc127-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="dc127-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc127-140">CommonParameters</span></span>
<span data-ttu-id="dc127-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc127-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc127-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc127-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc127-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc127-143">INPUTS</span></span>

### <span data-ttu-id="dc127-144">Нет</span><span class="sxs-lookup"><span data-stu-id="dc127-144">None</span></span>

## <span data-ttu-id="dc127-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc127-145">OUTPUTS</span></span>

### <span data-ttu-id="dc127-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="dc127-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="dc127-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc127-147">NOTES</span></span>

## <span data-ttu-id="dc127-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc127-148">RELATED LINKS</span></span>
