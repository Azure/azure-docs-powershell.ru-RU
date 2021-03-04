---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: ff5dee9a4e072cea7f1ee5bd46898857233ed0d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956947"
---
# <span data-ttu-id="28187-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="28187-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="28187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28187-102">SYNOPSIS</span></span>
<span data-ttu-id="28187-103">Возвращает доступные теги брандмауэра Azure FQDN.</span><span class="sxs-lookup"><span data-stu-id="28187-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="28187-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="28187-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28187-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28187-105">DESCRIPTION</span></span>
<span data-ttu-id="28187-106">Командлет **Get-AzFirewallFqdnTag** получает список тегов FQDN, которые можно использовать для правил брандмауэра приложения Azure</span><span class="sxs-lookup"><span data-stu-id="28187-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="28187-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="28187-107">EXAMPLES</span></span>

### <span data-ttu-id="28187-108">1. Извлечение всех доступных тегов FQDN</span><span class="sxs-lookup"><span data-stu-id="28187-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="28187-109">В этом примере извлекаются все доступные теги FQDN.</span><span class="sxs-lookup"><span data-stu-id="28187-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="28187-110">2. Используйте первый доступный тег FQDN в правиле приложения</span><span class="sxs-lookup"><span data-stu-id="28187-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="28187-111">В этом примере создается правило брандмауэра приложения с использованием первого доступного тега FQDN.</span><span class="sxs-lookup"><span data-stu-id="28187-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="28187-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28187-112">PARAMETERS</span></span>

### <span data-ttu-id="28187-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28187-113">-DefaultProfile</span></span>
<span data-ttu-id="28187-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28187-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28187-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28187-115">CommonParameters</span></span>
<span data-ttu-id="28187-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28187-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28187-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28187-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28187-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28187-118">INPUTS</span></span>

### <span data-ttu-id="28187-119">Нет</span><span class="sxs-lookup"><span data-stu-id="28187-119">None</span></span>

## <span data-ttu-id="28187-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="28187-120">OUTPUTS</span></span>

### <span data-ttu-id="28187-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="28187-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="28187-122">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="28187-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="28187-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="28187-123">NOTES</span></span>

## <span data-ttu-id="28187-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28187-124">RELATED LINKS</span></span>

[<span data-ttu-id="28187-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="28187-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="28187-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="28187-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
