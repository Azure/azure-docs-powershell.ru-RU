---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 2e4179019f74a8fd85b5f0ea3471bc586864172a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244837"
---
# <span data-ttu-id="5fe03-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="5fe03-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="5fe03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5fe03-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe03-103">Создание нового параметра DNS для политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="5fe03-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="5fe03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5fe03-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-ProxyNotRequiredForNetworkRule] [-Server <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fe03-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fe03-105">DESCRIPTION</span></span>
<span data-ttu-id="5fe03-106">Командлет **New-AzFirewallPolicyDnsSetting** создает объект параметров DNS для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe03-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="5fe03-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5fe03-107">EXAMPLES</span></span>

### <span data-ttu-id="5fe03-108">1. Создание пустой политики</span><span class="sxs-lookup"><span data-stu-id="5fe03-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="5fe03-109">В этом примере создается объект параметров DNS с параметром включения DNS-прокси.</span><span class="sxs-lookup"><span data-stu-id="5fe03-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="5fe03-110">2. Создание пустой политики с помощью режима ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="5fe03-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```
<span data-ttu-id="5fe03-111">В этом примере создается объект параметров DNS с параметром включения DNS-прокси и настройки настраиваемых DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="5fe03-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="5fe03-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5fe03-112">PARAMETERS</span></span>

### <span data-ttu-id="5fe03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe03-113">-DefaultProfile</span></span>
<span data-ttu-id="5fe03-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fe03-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fe03-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="5fe03-115">-EnableProxy</span></span>
<span data-ttu-id="5fe03-116">Включите DNS-прокси.</span><span class="sxs-lookup"><span data-stu-id="5fe03-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="5fe03-117">По умолчанию это значение отключено.</span><span class="sxs-lookup"><span data-stu-id="5fe03-117">By default it is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe03-118">-ProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5fe03-118">-ProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="5fe03-119">В сетевых правилах для полных доменных имен требуются функции DNS-прокси.</span><span class="sxs-lookup"><span data-stu-id="5fe03-119">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>
<span data-ttu-id="5fe03-120">По умолчанию используется значение true.</span><span class="sxs-lookup"><span data-stu-id="5fe03-120">By default it is true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe03-121">-Сервер</span><span class="sxs-lookup"><span data-stu-id="5fe03-121">-Server</span></span>
<span data-ttu-id="5fe03-122">Список DNS-серверов</span><span class="sxs-lookup"><span data-stu-id="5fe03-122">The list of DNS Servers</span></span>

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

### <span data-ttu-id="5fe03-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fe03-123">-Confirm</span></span>
<span data-ttu-id="5fe03-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5fe03-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe03-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fe03-125">-WhatIf</span></span>
<span data-ttu-id="5fe03-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5fe03-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fe03-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5fe03-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe03-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe03-128">CommonParameters</span></span>
<span data-ttu-id="5fe03-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5fe03-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe03-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fe03-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe03-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5fe03-131">INPUTS</span></span>

### <span data-ttu-id="5fe03-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="5fe03-132">None</span></span>

## <span data-ttu-id="5fe03-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fe03-133">OUTPUTS</span></span>

### <span data-ttu-id="5fe03-134">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="5fe03-134">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="5fe03-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5fe03-135">NOTES</span></span>

## <span data-ttu-id="5fe03-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fe03-136">RELATED LINKS</span></span>
