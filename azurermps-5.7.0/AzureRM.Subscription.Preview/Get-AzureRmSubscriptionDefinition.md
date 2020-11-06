---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/get-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 8f9cfda051542327fdb6175da081c99e6b8b6b3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558727"
---
# <span data-ttu-id="b5581-101">Get-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="b5581-101">Get-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="b5581-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5581-102">SYNOPSIS</span></span>
<span data-ttu-id="b5581-103">Получение определения подписки.</span><span class="sxs-lookup"><span data-stu-id="b5581-103">Get a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5581-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5581-104">SYNTAX</span></span>

### <span data-ttu-id="b5581-105">Получение определений подписок.</span><span class="sxs-lookup"><span data-stu-id="b5581-105">Get subscription definitions.</span></span>
```
Get-AzureRmSubscriptionDefinition
```

## <span data-ttu-id="b5581-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5581-106">EXAMPLES</span></span>

### <span data-ttu-id="b5581-107">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b5581-107">Example 1</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition

Name                    : MyProdSubscription1
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyProdSubscription1
OfferType               : MS-AZR-0017P

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="b5581-108">Получает все определения подписок.</span><span class="sxs-lookup"><span data-stu-id="b5581-108">Gets all subscription definitions.</span></span>

### <span data-ttu-id="b5581-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b5581-109">Example 2</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition -Name MyProdSubscription2

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="b5581-110">Получает определение подписки с именем MyProdSubscription2.</span><span class="sxs-lookup"><span data-stu-id="b5581-110">Gets a subscription definition with the name MyProdSubscription2.</span></span>

## <span data-ttu-id="b5581-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5581-111">PARAMETERS</span></span>

### <span data-ttu-id="b5581-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5581-112">-Name</span></span>
<span data-ttu-id="b5581-113">Имя определения подписки, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b5581-113">The name of the subscription definition to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5581-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5581-114">CommonParameters</span></span>
<span data-ttu-id="b5581-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5581-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5581-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5581-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5581-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5581-117">INPUTS</span></span>

### <span data-ttu-id="b5581-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="b5581-118">None</span></span>

## <span data-ttu-id="b5581-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5581-119">OUTPUTS</span></span>

### <span data-ttu-id="b5581-120">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. SubscriptionDefinition. Models. PSSubscriptionDefinition, Microsoft. Azure. Commands. SubscriptionDefinition, Version = 0.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="b5581-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition, Microsoft.Azure.Commands.SubscriptionDefinition, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b5581-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5581-121">NOTES</span></span>

## <span data-ttu-id="b5581-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5581-122">RELATED LINKS</span></span>

