---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: eed81fbd222220225a67378c67aa1d32d440577a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960392"
---
# <span data-ttu-id="ef821-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="ef821-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="ef821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef821-102">SYNOPSIS</span></span>
<span data-ttu-id="ef821-103">Создание списка аналитики угроз для политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="ef821-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="ef821-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ef821-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef821-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef821-105">DESCRIPTION</span></span>
<span data-ttu-id="ef821-106">С **помощью cmdletIntelWhitelist new-AzFirewallPolicyThreatIntelWhitelist** создается объект из списка угроз Intel, который можно использовать при создании или настройке политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="ef821-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="ef821-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ef821-107">EXAMPLES</span></span>

### <span data-ttu-id="ef821-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef821-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="ef821-109">В этом примере создается белый список intel угроз, содержащий белый список FQDN из одной записи и список IP-адресов из двух записей.</span><span class="sxs-lookup"><span data-stu-id="ef821-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="ef821-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef821-110">PARAMETERS</span></span>

### <span data-ttu-id="ef821-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef821-111">-DefaultProfile</span></span>
<span data-ttu-id="ef821-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef821-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef821-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="ef821-113">-FQDN</span></span>
<span data-ttu-id="ef821-114">FQDNs списка Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="ef821-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="ef821-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="ef821-115">-IpAddress</span></span>
<span data-ttu-id="ef821-116">IP-адреса списка Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="ef821-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="ef821-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef821-117">CommonParameters</span></span>
<span data-ttu-id="ef821-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef821-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef821-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef821-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef821-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef821-120">INPUTS</span></span>

### <span data-ttu-id="ef821-121">Нет</span><span class="sxs-lookup"><span data-stu-id="ef821-121">None</span></span>

## <span data-ttu-id="ef821-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef821-122">OUTPUTS</span></span>

### <span data-ttu-id="ef821-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="ef821-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="ef821-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ef821-124">NOTES</span></span>

## <span data-ttu-id="ef821-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef821-125">RELATED LINKS</span></span>
