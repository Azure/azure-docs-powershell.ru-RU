---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079506"
---
# <span data-ttu-id="907d0-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="907d0-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="907d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="907d0-102">SYNOPSIS</span></span>
<span data-ttu-id="907d0-103">Получает все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="907d0-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="907d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="907d0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="907d0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="907d0-105">DESCRIPTION</span></span>
<span data-ttu-id="907d0-106">Командлет **Get-AzApplicationGatewayAvailableWafRuleSet** получает все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="907d0-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="907d0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="907d0-107">EXAMPLES</span></span>

### <span data-ttu-id="907d0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="907d0-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="907d0-109">Эти команды возвращают все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="907d0-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="907d0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="907d0-110">PARAMETERS</span></span>

### <span data-ttu-id="907d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907d0-111">-DefaultProfile</span></span>
<span data-ttu-id="907d0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="907d0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="907d0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907d0-113">CommonParameters</span></span>
<span data-ttu-id="907d0-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="907d0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907d0-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="907d0-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907d0-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="907d0-116">INPUTS</span></span>

### <span data-ttu-id="907d0-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="907d0-117">None</span></span>

## <span data-ttu-id="907d0-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="907d0-118">OUTPUTS</span></span>

### <span data-ttu-id="907d0-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="907d0-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="907d0-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="907d0-120">NOTES</span></span>
<span data-ttu-id="907d0-121">**List-AzApplicationGatewayAvailableWafRuleSets** — псевдоним для командлета **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="907d0-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="907d0-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="907d0-122">RELATED LINKS</span></span>
