---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 18946b74ea72ac3d5db2dd683657eda60b8eeec5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964152"
---
# <span data-ttu-id="d37af-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="d37af-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="d37af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37af-102">SYNOPSIS</span></span>
<span data-ttu-id="d37af-103">Создание списка аналитики угроз для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="d37af-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="d37af-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d37af-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d37af-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d37af-105">DESCRIPTION</span></span>
<span data-ttu-id="d37af-106">С **помощью cmdletIntelWhitelist New-AzFirewallThreatIntelWhitelist** создается объект списка угроз Intel, который можно использовать при создании или настройке брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="d37af-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="d37af-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d37af-107">EXAMPLES</span></span>

### <span data-ttu-id="d37af-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d37af-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="d37af-109">В этом примере создается белый список intel угроз, содержащий белый список FQDN из двух записей и список IP-адресов из двух записей.</span><span class="sxs-lookup"><span data-stu-id="d37af-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="d37af-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d37af-110">PARAMETERS</span></span>

### <span data-ttu-id="d37af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37af-111">-DefaultProfile</span></span>
<span data-ttu-id="d37af-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d37af-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37af-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="d37af-113">-FQDN</span></span>
<span data-ttu-id="d37af-114">FQDNs списка Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="d37af-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="d37af-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="d37af-115">-IpAddress</span></span>
<span data-ttu-id="d37af-116">IP-адреса списка Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="d37af-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="d37af-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37af-117">CommonParameters</span></span>
<span data-ttu-id="d37af-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37af-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37af-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d37af-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37af-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d37af-120">INPUTS</span></span>

### <span data-ttu-id="d37af-121">Нет</span><span class="sxs-lookup"><span data-stu-id="d37af-121">None</span></span>

## <span data-ttu-id="d37af-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d37af-122">OUTPUTS</span></span>

### <span data-ttu-id="d37af-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="d37af-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="d37af-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d37af-124">NOTES</span></span>

## <span data-ttu-id="d37af-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d37af-125">RELATED LINKS</span></span>

[<span data-ttu-id="d37af-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d37af-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="d37af-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d37af-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d37af-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d37af-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)