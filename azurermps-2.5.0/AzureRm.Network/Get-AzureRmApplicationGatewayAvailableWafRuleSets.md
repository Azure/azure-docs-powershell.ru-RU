---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
ms.openlocfilehash: 83ee8e673271079690c24691f22badfe5193ba50
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913852"
---
# <span data-ttu-id="a4fc2-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="a4fc2-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="a4fc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="a4fc2-103">Получает все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="a4fc2-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4fc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4fc2-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4fc2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4fc2-105">DESCRIPTION</span></span>
<span data-ttu-id="a4fc2-106">Командлет **Get-AzureRmApplicationGatewayAvailableWafRuleSets** получает все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="a4fc2-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="a4fc2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4fc2-107">EXAMPLES</span></span>

### <span data-ttu-id="a4fc2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4fc2-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="a4fc2-109">Эти команды возвращают все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="a4fc2-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="a4fc2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4fc2-110">PARAMETERS</span></span>

### <span data-ttu-id="a4fc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4fc2-111">-DefaultProfile</span></span>
<span data-ttu-id="a4fc2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4fc2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4fc2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4fc2-113">CommonParameters</span></span>
<span data-ttu-id="a4fc2-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4fc2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4fc2-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4fc2-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4fc2-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4fc2-116">INPUTS</span></span>

### <span data-ttu-id="a4fc2-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="a4fc2-117">None</span></span>

## <span data-ttu-id="a4fc2-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4fc2-118">OUTPUTS</span></span>

### <span data-ttu-id="a4fc2-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="a4fc2-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="a4fc2-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4fc2-120">NOTES</span></span>
<span data-ttu-id="a4fc2-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** — псевдоним для командлета **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="a4fc2-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="a4fc2-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4fc2-122">RELATED LINKS</span></span>

