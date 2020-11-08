---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066280"
---
# <span data-ttu-id="6ba11-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="6ba11-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="6ba11-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ba11-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba11-103">Создание нового добавлениеного каталога для угроз для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="6ba11-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="6ba11-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ba11-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ba11-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ba11-105">DESCRIPTION</span></span>
<span data-ttu-id="6ba11-106">Командлет **New-AzFirewallThreatIntelWhitelist** создает объект Threat Intel Добавление, который можно использовать при создании или настройке брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="6ba11-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="6ba11-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ba11-107">EXAMPLES</span></span>

### <span data-ttu-id="6ba11-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ba11-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="6ba11-109">В этом примере создается угроза Intel Добавление, содержащая полное доменное имя Добавление из двух записей и IP-адреса добавление с двумя записями.</span><span class="sxs-lookup"><span data-stu-id="6ba11-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="6ba11-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ba11-110">PARAMETERS</span></span>

### <span data-ttu-id="6ba11-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba11-111">-DefaultProfile</span></span>
<span data-ttu-id="6ba11-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ba11-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ba11-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="6ba11-113">-FQDN</span></span>
<span data-ttu-id="6ba11-114">Полные доменные имена для угрозы Intel Добавление</span><span class="sxs-lookup"><span data-stu-id="6ba11-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="6ba11-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="6ba11-115">-IpAddress</span></span>
<span data-ttu-id="6ba11-116">IP-адреса угроз корпорации Intel Добавление</span><span class="sxs-lookup"><span data-stu-id="6ba11-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="6ba11-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba11-117">CommonParameters</span></span>
<span data-ttu-id="6ba11-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ba11-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba11-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ba11-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba11-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ba11-120">INPUTS</span></span>

### <span data-ttu-id="6ba11-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="6ba11-121">None</span></span>

## <span data-ttu-id="6ba11-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ba11-122">OUTPUTS</span></span>

### <span data-ttu-id="6ba11-123">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="6ba11-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="6ba11-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ba11-124">NOTES</span></span>

## <span data-ttu-id="6ba11-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ba11-125">RELATED LINKS</span></span>

[<span data-ttu-id="6ba11-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6ba11-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="6ba11-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6ba11-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="6ba11-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6ba11-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)