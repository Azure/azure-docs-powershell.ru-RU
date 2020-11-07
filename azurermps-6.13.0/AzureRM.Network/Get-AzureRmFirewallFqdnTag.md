---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734618"
---
# <span data-ttu-id="51ac3-101">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="51ac3-101">Get-AzureRmFirewallFqdnTag</span></span>

## <span data-ttu-id="51ac3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51ac3-102">SYNOPSIS</span></span>
<span data-ttu-id="51ac3-103">Получает доступные теги брандмауэра для полного доменного имени для Azure.</span><span class="sxs-lookup"><span data-stu-id="51ac3-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51ac3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51ac3-104">SYNTAX</span></span>

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51ac3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51ac3-105">DESCRIPTION</span></span>
<span data-ttu-id="51ac3-106">Командлет **Get-AzureRmFirewallFqdnTag** получает список тегов полных доменных имен, которые можно использовать в правилах брандмауэра для приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="51ac3-106">The **Get-AzureRmFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="51ac3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51ac3-107">EXAMPLES</span></span>

### <span data-ttu-id="51ac3-108">1. Извлеките все доступные теги полного доменного имени</span><span class="sxs-lookup"><span data-stu-id="51ac3-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzureRmFirewallFqdnTag
```

<span data-ttu-id="51ac3-109">В этом примере извлекаются все доступные теги полного доменного имени.</span><span class="sxs-lookup"><span data-stu-id="51ac3-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="51ac3-110">2. Использование первого доступного тега полного доменного имени в правиле приложения</span><span class="sxs-lookup"><span data-stu-id="51ac3-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="51ac3-111">В этом примере создается правило приложения брандмауэра с помощью первого доступного тега полного доменного имени</span><span class="sxs-lookup"><span data-stu-id="51ac3-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="51ac3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51ac3-112">PARAMETERS</span></span>

### <span data-ttu-id="51ac3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ac3-113">-DefaultProfile</span></span>
<span data-ttu-id="51ac3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51ac3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ac3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ac3-115">CommonParameters</span></span>
<span data-ttu-id="51ac3-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51ac3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ac3-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51ac3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ac3-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51ac3-118">INPUTS</span></span>

### <span data-ttu-id="51ac3-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="51ac3-119">None</span></span>
<span data-ttu-id="51ac3-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="51ac3-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51ac3-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51ac3-121">OUTPUTS</span></span>

### <span data-ttu-id="51ac3-122">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="51ac3-122">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

## <span data-ttu-id="51ac3-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="51ac3-123">NOTES</span></span>

## <span data-ttu-id="51ac3-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51ac3-124">RELATED LINKS</span></span>

[<span data-ttu-id="51ac3-125">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="51ac3-125">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="51ac3-126">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="51ac3-126">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)
