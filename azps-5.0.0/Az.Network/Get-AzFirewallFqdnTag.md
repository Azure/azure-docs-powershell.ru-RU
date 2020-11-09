---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248843"
---
# <span data-ttu-id="0af3c-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="0af3c-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="0af3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0af3c-102">SYNOPSIS</span></span>
<span data-ttu-id="0af3c-103">Получает доступные теги брандмауэра для полного доменного имени для Azure.</span><span class="sxs-lookup"><span data-stu-id="0af3c-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="0af3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0af3c-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0af3c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0af3c-105">DESCRIPTION</span></span>
<span data-ttu-id="0af3c-106">Командлет **Get-AzFirewallFqdnTag** получает список тегов полных доменных имен, которые можно использовать в правилах брандмауэра для приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="0af3c-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="0af3c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0af3c-107">EXAMPLES</span></span>

### <span data-ttu-id="0af3c-108">1. Извлеките все доступные теги полного доменного имени</span><span class="sxs-lookup"><span data-stu-id="0af3c-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="0af3c-109">В этом примере извлекаются все доступные теги полного доменного имени.</span><span class="sxs-lookup"><span data-stu-id="0af3c-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="0af3c-110">2. Использование первого доступного тега полного доменного имени в правиле приложения</span><span class="sxs-lookup"><span data-stu-id="0af3c-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="0af3c-111">В этом примере создается правило приложения брандмауэра с помощью первого доступного тега полного доменного имени</span><span class="sxs-lookup"><span data-stu-id="0af3c-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="0af3c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0af3c-112">PARAMETERS</span></span>

### <span data-ttu-id="0af3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af3c-113">-DefaultProfile</span></span>
<span data-ttu-id="0af3c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0af3c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0af3c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af3c-115">CommonParameters</span></span>
<span data-ttu-id="0af3c-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0af3c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af3c-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0af3c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af3c-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0af3c-118">INPUTS</span></span>

### <span data-ttu-id="0af3c-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="0af3c-119">None</span></span>

## <span data-ttu-id="0af3c-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0af3c-120">OUTPUTS</span></span>

### <span data-ttu-id="0af3c-121">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="0af3c-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="0af3c-122">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network.. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. командлеты. Network, Version = 1.0.0.0, культура = независимая, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0af3c-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0af3c-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="0af3c-123">NOTES</span></span>

## <span data-ttu-id="0af3c-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0af3c-124">RELATED LINKS</span></span>

[<span data-ttu-id="0af3c-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="0af3c-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="0af3c-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0af3c-126">New-AzFirewall</span></span>](./New-AzFirewall.md)