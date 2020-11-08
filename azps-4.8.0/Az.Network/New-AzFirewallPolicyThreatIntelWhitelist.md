---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244120"
---
# <span data-ttu-id="defe5-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="defe5-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="defe5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="defe5-102">SYNOPSIS</span></span>
<span data-ttu-id="defe5-103">Создание добавление для политики брандмауэра Azure с помощью новой логики операций с угрозами</span><span class="sxs-lookup"><span data-stu-id="defe5-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="defe5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="defe5-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="defe5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="defe5-105">DESCRIPTION</span></span>
<span data-ttu-id="defe5-106">Командлет **New-AzFirewallPolicyThreatIntelWhitelist** создает объект Threat Intel Добавление, который можно использовать при создании или настройке политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="defe5-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="defe5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="defe5-107">EXAMPLES</span></span>

### <span data-ttu-id="defe5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="defe5-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="defe5-109">В этом примере создается угроза Intel добавление с полным доменным именем Добавление одной записи и IP-адресом Добавление из двух записей.</span><span class="sxs-lookup"><span data-stu-id="defe5-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="defe5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="defe5-110">PARAMETERS</span></span>

### <span data-ttu-id="defe5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="defe5-111">-DefaultProfile</span></span>
<span data-ttu-id="defe5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="defe5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="defe5-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="defe5-113">-FQDN</span></span>
<span data-ttu-id="defe5-114">Полные доменные имена для угрозы Intel Добавление</span><span class="sxs-lookup"><span data-stu-id="defe5-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="defe5-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="defe5-115">-IpAddress</span></span>
<span data-ttu-id="defe5-116">IP-адреса угроз корпорации Intel Добавление</span><span class="sxs-lookup"><span data-stu-id="defe5-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="defe5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="defe5-117">CommonParameters</span></span>
<span data-ttu-id="defe5-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="defe5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="defe5-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="defe5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="defe5-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="defe5-120">INPUTS</span></span>

### <span data-ttu-id="defe5-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="defe5-121">None</span></span>

## <span data-ttu-id="defe5-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="defe5-122">OUTPUTS</span></span>

### <span data-ttu-id="defe5-123">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="defe5-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="defe5-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="defe5-124">NOTES</span></span>

## <span data-ttu-id="defe5-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="defe5-125">RELATED LINKS</span></span>
