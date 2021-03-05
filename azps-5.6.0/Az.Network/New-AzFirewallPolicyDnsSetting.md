---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 35b56e6aafe73c09343fb17d385dd7ab4c705c5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985771"
---
# <span data-ttu-id="cf754-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="cf754-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="cf754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf754-102">SYNOPSIS</span></span>
<span data-ttu-id="cf754-103">Создание нового параметра DNS для политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="cf754-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="cf754-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cf754-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf754-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf754-105">DESCRIPTION</span></span>
<span data-ttu-id="cf754-106">С **помощью cmdlet New-AzFirewallPolicyDnsSetting** создается объект настройки DNS для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cf754-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="cf754-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cf754-107">EXAMPLES</span></span>

### <span data-ttu-id="cf754-108">1. Создание пустой политики</span><span class="sxs-lookup"><span data-stu-id="cf754-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="cf754-109">В этом примере создается объект настройки DNS с параметром, включающий прокси-сервер DNS.</span><span class="sxs-lookup"><span data-stu-id="cf754-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="cf754-110">2. Создание пустой политики в режиме ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="cf754-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="cf754-111">В этом примере создается объект настройки DNS с параметром, позволяющим настроить прокси-сервер dns и настроить пользовательские DNS-серверы.</span><span class="sxs-lookup"><span data-stu-id="cf754-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="cf754-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf754-112">PARAMETERS</span></span>

### <span data-ttu-id="cf754-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf754-113">-DefaultProfile</span></span>
<span data-ttu-id="cf754-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf754-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf754-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="cf754-115">-EnableProxy</span></span>
<span data-ttu-id="cf754-116">В включить прокси-сервер DNS.</span><span class="sxs-lookup"><span data-stu-id="cf754-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="cf754-117">По умолчанию он отключен.</span><span class="sxs-lookup"><span data-stu-id="cf754-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="cf754-118">-Server</span><span class="sxs-lookup"><span data-stu-id="cf754-118">-Server</span></span>
<span data-ttu-id="cf754-119">Список DNS-серверов</span><span class="sxs-lookup"><span data-stu-id="cf754-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="cf754-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf754-120">-Confirm</span></span>
<span data-ttu-id="cf754-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cf754-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf754-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf754-122">-WhatIf</span></span>
<span data-ttu-id="cf754-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf754-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf754-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cf754-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf754-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf754-125">CommonParameters</span></span>
<span data-ttu-id="cf754-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf754-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf754-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf754-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf754-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf754-128">INPUTS</span></span>

### <span data-ttu-id="cf754-129">Нет</span><span class="sxs-lookup"><span data-stu-id="cf754-129">None</span></span>

## <span data-ttu-id="cf754-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf754-130">OUTPUTS</span></span>

### <span data-ttu-id="cf754-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="cf754-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="cf754-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cf754-132">NOTES</span></span>

## <span data-ttu-id="cf754-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf754-133">RELATED LINKS</span></span>
