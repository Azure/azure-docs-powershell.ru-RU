---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 59d1c7fa5d546652d8976dc42739c2e483164999
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517697"
---
# <span data-ttu-id="68b18-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="68b18-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="68b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68b18-102">SYNOPSIS</span></span>

<span data-ttu-id="68b18-103">Получает планы Защитника Azure для подписки в Центре безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="68b18-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="68b18-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="68b18-104">SYNTAX</span></span>

### <span data-ttu-id="68b18-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="68b18-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68b18-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="68b18-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68b18-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="68b18-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68b18-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68b18-108">DESCRIPTION</span></span>

<span data-ttu-id="68b18-109">С помощью этого cmdlet можно просмотреть каждый план Защитника Azure для каждой подписки.</span><span class="sxs-lookup"><span data-stu-id="68b18-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="68b18-110">Дополнительные сведения о Защитнике Azure и доступных планах см. [в обзоре защитника Azure.](https://docs.microsoft.com/azure/security-center/azure-defender)</span><span class="sxs-lookup"><span data-stu-id="68b18-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="68b18-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="68b18-111">EXAMPLES</span></span>

### <span data-ttu-id="68b18-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="68b18-112">Example 1</span></span>

```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                   Name                      PricingTier    FreeTrialRemainingTime
--                                                                                                                   ----                      -----------    ----------------------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines            VirtualMachines           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/Sqlservers                 SqlServers                Standard       00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices                AppServices               Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts            StorageAccounts           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlserverVirtualMachines   SqlservervirtualMachines  Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService          KubernetesService         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry          ContainerRegistry         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults                  KeyVaults                 Free           00:00:00
```

<span data-ttu-id="68b18-113">Получает состояние каждого плана Защитника Azure для подписки.</span><span class="sxs-lookup"><span data-stu-id="68b18-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="68b18-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="68b18-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="68b18-115">Сведения о ценах на определенный ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="68b18-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="68b18-116">Где ResourceId — один из возвращаемого `Get-AzSecurityPricing` ИД.</span><span class="sxs-lookup"><span data-stu-id="68b18-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="68b18-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="68b18-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="68b18-118">Сведения о ценах для именоваемого плана Защитника Azure.</span><span class="sxs-lookup"><span data-stu-id="68b18-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="68b18-119">Где `name` находится одно из имен, возвращенных `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="68b18-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="68b18-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68b18-120">PARAMETERS</span></span>

### <span data-ttu-id="68b18-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b18-121">-DefaultProfile</span></span>

<span data-ttu-id="68b18-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68b18-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68b18-123">-Name</span><span class="sxs-lookup"><span data-stu-id="68b18-123">-Name</span></span>

<span data-ttu-id="68b18-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="68b18-124">Resource name.</span></span>

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

### <span data-ttu-id="68b18-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68b18-125">-ResourceId</span></span>

<span data-ttu-id="68b18-126">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="68b18-126">Resource ID.</span></span>

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

### <span data-ttu-id="68b18-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b18-127">CommonParameters</span></span>

<span data-ttu-id="68b18-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68b18-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b18-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68b18-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b18-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68b18-130">INPUTS</span></span>

### <span data-ttu-id="68b18-131">System.String</span><span class="sxs-lookup"><span data-stu-id="68b18-131">System.String</span></span>

## <span data-ttu-id="68b18-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68b18-132">OUTPUTS</span></span>

### <span data-ttu-id="68b18-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="68b18-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="68b18-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="68b18-134">NOTES</span></span>

## <span data-ttu-id="68b18-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68b18-135">RELATED LINKS</span></span>
