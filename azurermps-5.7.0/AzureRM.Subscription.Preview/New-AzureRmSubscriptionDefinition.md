---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567361"
---
# <span data-ttu-id="c71ec-101">New-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="c71ec-101">New-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="c71ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c71ec-102">SYNOPSIS</span></span>
<span data-ttu-id="c71ec-103">Создание определения подписки.</span><span class="sxs-lookup"><span data-stu-id="c71ec-103">Creates a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c71ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c71ec-104">SYNTAX</span></span>

### <span data-ttu-id="c71ec-105">Создание определения подписки</span><span class="sxs-lookup"><span data-stu-id="c71ec-105">Create subscription definition</span></span>
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## <span data-ttu-id="c71ec-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c71ec-106">DESCRIPTION</span></span>
<span data-ttu-id="c71ec-107">Командлет **New-AzureRmSubscriptionDefinition** создает определение подписки.</span><span class="sxs-lookup"><span data-stu-id="c71ec-107">The **New-AzureRmSubscriptionDefinition** cmdlet creates a subscription definition.</span></span>

## <span data-ttu-id="c71ec-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c71ec-108">EXAMPLES</span></span>

### <span data-ttu-id="c71ec-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c71ec-109">Example 1</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="c71ec-110">Создание определения подписки с отображаемым именем по умолчанию подписки.</span><span class="sxs-lookup"><span data-stu-id="c71ec-110">Creates a subscription definition with a default subscription display name.</span></span>

### <span data-ttu-id="c71ec-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c71ec-111">Example 2</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="c71ec-112">Создает определение подписки с отображаемым именем для настраиваемой подписки.</span><span class="sxs-lookup"><span data-stu-id="c71ec-112">Creates a subscription definition with a custom subscription display name.</span></span>

## <span data-ttu-id="c71ec-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c71ec-113">PARAMETERS</span></span>

### <span data-ttu-id="c71ec-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c71ec-114">-Name</span></span>
<span data-ttu-id="c71ec-115">Имя создаваемого определения подписки.</span><span class="sxs-lookup"><span data-stu-id="c71ec-115">The name of the subscription definition to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71ec-116">-OfferType</span><span class="sxs-lookup"><span data-stu-id="c71ec-116">-OfferType</span></span>
<span data-ttu-id="c71ec-117">Тип предложения, которое следует использовать при создании базовой подписки.</span><span class="sxs-lookup"><span data-stu-id="c71ec-117">The type of offer to use when creating the underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71ec-118">-SubscriptionDisplayName</span><span class="sxs-lookup"><span data-stu-id="c71ec-118">-SubscriptionDisplayName</span></span>
<span data-ttu-id="c71ec-119">Отображаемое имя, используемое при создании подписки на подписку на определенную подписку.</span><span class="sxs-lookup"><span data-stu-id="c71ec-119">The display name to use when creating the subscription definition's underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c71ec-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c71ec-120">CommonParameters</span></span>
<span data-ttu-id="c71ec-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c71ec-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c71ec-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c71ec-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c71ec-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c71ec-123">INPUTS</span></span>

### <span data-ttu-id="c71ec-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="c71ec-124">None</span></span>

## <span data-ttu-id="c71ec-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c71ec-125">OUTPUTS</span></span>

### <span data-ttu-id="c71ec-126">Microsoft. Azure. Commands. SubscriptionDefinition. Models. PSSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="c71ec-126">Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition</span></span>

## <span data-ttu-id="c71ec-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="c71ec-127">NOTES</span></span>

## <span data-ttu-id="c71ec-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c71ec-128">RELATED LINKS</span></span>

