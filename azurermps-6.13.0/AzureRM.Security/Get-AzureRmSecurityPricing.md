---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558272"
---
# <span data-ttu-id="61b63-101">Get-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="61b63-101">Get-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="61b63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61b63-102">SYNOPSIS</span></span>
<span data-ttu-id="61b63-103">Возвращает данные о ценовой категории для центра безопасности Azure для области.</span><span class="sxs-lookup"><span data-stu-id="61b63-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61b63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61b63-104">SYNTAX</span></span>

### <span data-ttu-id="61b63-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61b63-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61b63-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="61b63-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61b63-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="61b63-107">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="61b63-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="61b63-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61b63-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="61b63-109">ResourceId</span></span>
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61b63-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61b63-110">DESCRIPTION</span></span>
<span data-ttu-id="61b63-111">Ценовая категория центра безопасности Azure выбирается для каждой области, с помощью этого командлета вы можете получить настроенную ценовую категорию.</span><span class="sxs-lookup"><span data-stu-id="61b63-111">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="61b63-112">Ценовая категория включает в себя все группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61b63-112">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="61b63-113">Ценовая группа для групп ресурсов будет переопределять ценовую категорию подписки.</span><span class="sxs-lookup"><span data-stu-id="61b63-113">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="61b63-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61b63-114">EXAMPLES</span></span>

### <span data-ttu-id="61b63-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61b63-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="61b63-116">Получает все настроенные ценовые категории для подписки и групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61b63-116">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="61b63-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="61b63-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="61b63-118">Получает настроенную ценовую категорию для ресурса "myService1" Gorup.</span><span class="sxs-lookup"><span data-stu-id="61b63-118">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="61b63-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61b63-119">PARAMETERS</span></span>

### <span data-ttu-id="61b63-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b63-120">-DefaultProfile</span></span>
<span data-ttu-id="61b63-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61b63-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61b63-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61b63-122">-Name</span></span>
<span data-ttu-id="61b63-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="61b63-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b63-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61b63-124">-ResourceGroupName</span></span>
<span data-ttu-id="61b63-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61b63-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61b63-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61b63-126">-ResourceId</span></span>
<span data-ttu-id="61b63-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="61b63-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61b63-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b63-128">CommonParameters</span></span>
<span data-ttu-id="61b63-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61b63-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b63-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b63-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b63-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61b63-131">INPUTS</span></span>

### <span data-ttu-id="61b63-132">System. String</span><span class="sxs-lookup"><span data-stu-id="61b63-132">System.String</span></span>

## <span data-ttu-id="61b63-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61b63-133">OUTPUTS</span></span>

### <span data-ttu-id="61b63-134">Microsoft. Azure. Commands. Security. Models. цен. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="61b63-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="61b63-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="61b63-135">NOTES</span></span>

## <span data-ttu-id="61b63-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61b63-136">RELATED LINKS</span></span>
