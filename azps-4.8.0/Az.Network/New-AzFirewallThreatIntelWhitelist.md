---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236049"
---
# <span data-ttu-id="8da6c-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="8da6c-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="8da6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8da6c-102">SYNOPSIS</span></span>
<span data-ttu-id="8da6c-103">Создание нового добавлениеного каталога для угроз для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="8da6c-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="8da6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8da6c-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8da6c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8da6c-105">DESCRIPTION</span></span>
<span data-ttu-id="8da6c-106">Командлет **New-AzFirewallThreatIntelWhitelist** создает объект Threat Intel Добавление, который можно использовать при создании или настройке брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="8da6c-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="8da6c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8da6c-107">EXAMPLES</span></span>

### <span data-ttu-id="8da6c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8da6c-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="8da6c-109">В этом примере создается угроза Intel Добавление, содержащая полное доменное имя Добавление из двух записей и IP-адреса добавление с двумя записями.</span><span class="sxs-lookup"><span data-stu-id="8da6c-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="8da6c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8da6c-110">PARAMETERS</span></span>

### <span data-ttu-id="8da6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da6c-111">-DefaultProfile</span></span>
<span data-ttu-id="8da6c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8da6c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8da6c-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="8da6c-113">-FQDN</span></span>
<span data-ttu-id="8da6c-114">Полные доменные имена для угрозы Intel Добавление</span><span class="sxs-lookup"><span data-stu-id="8da6c-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="8da6c-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="8da6c-115">-IpAddress</span></span>
<span data-ttu-id="8da6c-116">IP-адреса угроз корпорации Intel Добавление</span><span class="sxs-lookup"><span data-stu-id="8da6c-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="8da6c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da6c-117">CommonParameters</span></span>
<span data-ttu-id="8da6c-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8da6c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da6c-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8da6c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da6c-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8da6c-120">INPUTS</span></span>

### <span data-ttu-id="8da6c-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="8da6c-121">None</span></span>

## <span data-ttu-id="8da6c-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8da6c-122">OUTPUTS</span></span>

### <span data-ttu-id="8da6c-123">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="8da6c-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="8da6c-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="8da6c-124">NOTES</span></span>

## <span data-ttu-id="8da6c-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8da6c-125">RELATED LINKS</span></span>

[<span data-ttu-id="8da6c-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8da6c-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="8da6c-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8da6c-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="8da6c-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8da6c-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)