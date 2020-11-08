---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: a1b07c5fb76d912ec117d42497f0d0b14bfb298c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246552"
---
# <span data-ttu-id="6ddb0-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="6ddb0-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="6ddb0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ddb0-102">SYNOPSIS</span></span>
<span data-ttu-id="6ddb0-103">Возвращает данные о ценовой категории для центра безопасности Azure для области.</span><span class="sxs-lookup"><span data-stu-id="6ddb0-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="6ddb0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ddb0-104">SYNTAX</span></span>

### <span data-ttu-id="6ddb0-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ddb0-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ddb0-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="6ddb0-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ddb0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ddb0-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ddb0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ddb0-108">DESCRIPTION</span></span>
<span data-ttu-id="6ddb0-109">Ценовая категория центра безопасности Azure выбирается для каждой области, с помощью этого командлета вы можете получить настроенную ценовую категорию.</span><span class="sxs-lookup"><span data-stu-id="6ddb0-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="6ddb0-110">Ценовая категория включает в себя все группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ddb0-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="6ddb0-111">Ценовая группа для групп ресурсов будет переопределять ценовую категорию подписки.</span><span class="sxs-lookup"><span data-stu-id="6ddb0-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="6ddb0-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ddb0-112">EXAMPLES</span></span>

### <span data-ttu-id="6ddb0-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ddb0-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
Id--/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines
--                                                                                                                             ----       -----------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServers
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServerVirtualMachin…
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults
```

<span data-ttu-id="6ddb0-114">Получает все настроенные ценовые категории для подписки и групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ddb0-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="6ddb0-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6ddb0-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="6ddb0-116">Получает настроенную ценовую категорию для группы ресурсов "myService1".</span><span class="sxs-lookup"><span data-stu-id="6ddb0-116">Gets the configured pricing tier for the "myService1" resource group.</span></span>

## <span data-ttu-id="6ddb0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ddb0-117">PARAMETERS</span></span>

### <span data-ttu-id="6ddb0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ddb0-118">-DefaultProfile</span></span>
<span data-ttu-id="6ddb0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ddb0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ddb0-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6ddb0-120">-Name</span></span>
<span data-ttu-id="6ddb0-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="6ddb0-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddb0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ddb0-122">-ResourceId</span></span>
<span data-ttu-id="6ddb0-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6ddb0-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ddb0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ddb0-124">CommonParameters</span></span>
<span data-ttu-id="6ddb0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ddb0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ddb0-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ddb0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ddb0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ddb0-127">INPUTS</span></span>

### <span data-ttu-id="6ddb0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6ddb0-128">System.String</span></span>

## <span data-ttu-id="6ddb0-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ddb0-129">OUTPUTS</span></span>

### <span data-ttu-id="6ddb0-130">Microsoft. Azure. Commands. Security. Models. цен. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="6ddb0-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="6ddb0-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ddb0-131">NOTES</span></span>

## <span data-ttu-id="6ddb0-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ddb0-132">RELATED LINKS</span></span>
