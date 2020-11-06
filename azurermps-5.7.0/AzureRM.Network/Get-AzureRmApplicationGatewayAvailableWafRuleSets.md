---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: fb16474d8a23f528aaaeb498ced4fa5a3e952236
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93570480"
---
# <span data-ttu-id="699a6-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="699a6-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="699a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="699a6-102">SYNOPSIS</span></span>
<span data-ttu-id="699a6-103">Получает все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="699a6-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="699a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="699a6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="699a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="699a6-105">DESCRIPTION</span></span>
<span data-ttu-id="699a6-106">Командлет **Get-AzureRmApplicationGatewayAvailableWafRuleSets** получает все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="699a6-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="699a6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="699a6-107">EXAMPLES</span></span>

### <span data-ttu-id="699a6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="699a6-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="699a6-109">Эти команды возвращают все доступные наборы правил брандмауэра для веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="699a6-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="699a6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="699a6-110">PARAMETERS</span></span>

### <span data-ttu-id="699a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699a6-111">-DefaultProfile</span></span>
<span data-ttu-id="699a6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="699a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="699a6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699a6-113">CommonParameters</span></span>
<span data-ttu-id="699a6-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="699a6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699a6-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699a6-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699a6-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="699a6-116">INPUTS</span></span>

### <span data-ttu-id="699a6-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="699a6-117">None</span></span>

## <span data-ttu-id="699a6-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="699a6-118">OUTPUTS</span></span>

### <span data-ttu-id="699a6-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="699a6-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="699a6-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="699a6-120">NOTES</span></span>
<span data-ttu-id="699a6-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** — псевдоним для командлета **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="699a6-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="699a6-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="699a6-122">RELATED LINKS</span></span>

