---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: 27e5715f32b631fff3f185f0925d0b2a85967ac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559700"
---
# <span data-ttu-id="65c2b-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="65c2b-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="65c2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="65c2b-103">Получает все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="65c2b-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65c2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65c2b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65c2b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65c2b-105">DESCRIPTION</span></span>
<span data-ttu-id="65c2b-106">Командлет **Get-AzureRmApplicationGatewayAvailableWafRuleSets** получает все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="65c2b-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="65c2b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65c2b-107">EXAMPLES</span></span>

### <span data-ttu-id="65c2b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65c2b-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="65c2b-109">Эти команды возвращают все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="65c2b-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="65c2b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65c2b-110">PARAMETERS</span></span>

### <span data-ttu-id="65c2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c2b-111">-DefaultProfile</span></span>
<span data-ttu-id="65c2b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65c2b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65c2b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c2b-113">CommonParameters</span></span>
<span data-ttu-id="65c2b-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65c2b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c2b-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c2b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c2b-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65c2b-116">INPUTS</span></span>

### <span data-ttu-id="65c2b-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="65c2b-117">None</span></span>

## <span data-ttu-id="65c2b-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65c2b-118">OUTPUTS</span></span>

### <span data-ttu-id="65c2b-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="65c2b-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="65c2b-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="65c2b-120">NOTES</span></span>
<span data-ttu-id="65c2b-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** — псевдоним для командлета **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="65c2b-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="65c2b-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65c2b-122">RELATED LINKS</span></span>

