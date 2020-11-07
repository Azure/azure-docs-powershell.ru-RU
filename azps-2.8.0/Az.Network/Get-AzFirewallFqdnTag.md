---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 28a7fa45c8c6dc291f5e0c2a54c9fcf5fb5242dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902930"
---
# <span data-ttu-id="eb847-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="eb847-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="eb847-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb847-102">SYNOPSIS</span></span>
<span data-ttu-id="eb847-103">Получает доступные теги брандмауэра для полного доменного имени для Azure.</span><span class="sxs-lookup"><span data-stu-id="eb847-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="eb847-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb847-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb847-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb847-105">DESCRIPTION</span></span>
<span data-ttu-id="eb847-106">Командлет **Get-AzFirewallFqdnTag** получает список тегов полных доменных имен, которые можно использовать в правилах брандмауэра для приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="eb847-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="eb847-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb847-107">EXAMPLES</span></span>

### <span data-ttu-id="eb847-108">1. Извлеките все доступные теги полного доменного имени</span><span class="sxs-lookup"><span data-stu-id="eb847-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="eb847-109">В этом примере извлекаются все доступные теги полного доменного имени.</span><span class="sxs-lookup"><span data-stu-id="eb847-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="eb847-110">2. Использование первого доступного тега полного доменного имени в правиле приложения</span><span class="sxs-lookup"><span data-stu-id="eb847-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="eb847-111">В этом примере создается правило приложения брандмауэра с помощью первого доступного тега полного доменного имени</span><span class="sxs-lookup"><span data-stu-id="eb847-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="eb847-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb847-112">PARAMETERS</span></span>

### <span data-ttu-id="eb847-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb847-113">-DefaultProfile</span></span>
<span data-ttu-id="eb847-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb847-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb847-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb847-115">CommonParameters</span></span>
<span data-ttu-id="eb847-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb847-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb847-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb847-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb847-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb847-118">INPUTS</span></span>

### <span data-ttu-id="eb847-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="eb847-119">None</span></span>

## <span data-ttu-id="eb847-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb847-120">OUTPUTS</span></span>

### <span data-ttu-id="eb847-121">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="eb847-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="eb847-122">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network.. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. командлеты. Network, Version = 1.0.0.0, культура = независимая, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="eb847-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="eb847-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb847-123">NOTES</span></span>

## <span data-ttu-id="eb847-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb847-124">RELATED LINKS</span></span>

[<span data-ttu-id="eb847-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="eb847-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="eb847-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="eb847-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
