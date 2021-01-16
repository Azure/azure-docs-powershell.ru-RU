---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506914"
---
# <span data-ttu-id="74f66-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="74f66-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="74f66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74f66-102">SYNOPSIS</span></span>
<span data-ttu-id="74f66-103">Создание списка аналитики угроз для политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="74f66-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="74f66-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="74f66-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74f66-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74f66-105">DESCRIPTION</span></span>
<span data-ttu-id="74f66-106">С **помощью cmdlet New-AzFirewallPolicyThreatIntelWhitelist** создается объект из списка угроз Intel, который можно использовать при создании или настройке политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="74f66-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="74f66-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="74f66-107">EXAMPLES</span></span>

### <span data-ttu-id="74f66-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74f66-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="74f66-109">В этом примере создается белый список intel угроз, содержащий белый список FQDN из одной записи и список IP-адресов из двух записей.</span><span class="sxs-lookup"><span data-stu-id="74f66-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="74f66-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74f66-110">PARAMETERS</span></span>

### <span data-ttu-id="74f66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f66-111">-DefaultProfile</span></span>
<span data-ttu-id="74f66-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74f66-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74f66-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="74f66-113">-FQDN</span></span>
<span data-ttu-id="74f66-114">FQDNs списка Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="74f66-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="74f66-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="74f66-115">-IpAddress</span></span>
<span data-ttu-id="74f66-116">IP-адреса списка Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="74f66-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="74f66-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f66-117">CommonParameters</span></span>
<span data-ttu-id="74f66-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f66-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f66-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74f66-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f66-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74f66-120">INPUTS</span></span>

### <span data-ttu-id="74f66-121">Нет</span><span class="sxs-lookup"><span data-stu-id="74f66-121">None</span></span>

## <span data-ttu-id="74f66-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="74f66-122">OUTPUTS</span></span>

### <span data-ttu-id="74f66-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="74f66-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="74f66-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="74f66-124">NOTES</span></span>

## <span data-ttu-id="74f66-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74f66-125">RELATED LINKS</span></span>
