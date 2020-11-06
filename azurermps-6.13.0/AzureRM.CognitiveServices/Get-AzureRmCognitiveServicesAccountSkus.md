---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: e1bacc62ca7efc3bd453be93196e83b0b6d67853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566831"
---
# <span data-ttu-id="30827-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="30827-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="30827-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30827-102">SYNOPSIS</span></span>
<span data-ttu-id="30827-103">Возвращает доступные SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="30827-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30827-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30827-104">SYNTAX</span></span>

### <span data-ttu-id="30827-105">GetSkusWithAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30827-105">GetSkusWithAccount (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30827-106">GetSkusWithFilter</span><span class="sxs-lookup"><span data-stu-id="30827-106">GetSkusWithFilter</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30827-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30827-107">DESCRIPTION</span></span>
<span data-ttu-id="30827-108">Командлет **Get-AzureRmCognitiveServicesAccountSkus** получает доступные SKU для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="30827-108">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="30827-109">SKU — это ярусный план для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="30827-109">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="30827-110">Она определяет цену, ограничение на звонки и ставку для счета.</span><span class="sxs-lookup"><span data-stu-id="30827-110">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="30827-111">F0 SKU является бесплатным уровнем.</span><span class="sxs-lookup"><span data-stu-id="30827-111">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="30827-112">Оплаченные уровни включают в себя S0, S1, S2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="30827-112">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="30827-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30827-113">EXAMPLES</span></span>

### <span data-ttu-id="30827-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30827-114">Example 1</span></span>
```powershell
PS C:\> (Get-AzureRmCognitiveServicesAccountSkus -ResourceGroupName cognitive-services-resource-group -Name myluis).Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="30827-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30827-115">PARAMETERS</span></span>

### <span data-ttu-id="30827-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30827-116">-DefaultProfile</span></span>
<span data-ttu-id="30827-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="30827-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30827-118">-Location</span><span class="sxs-lookup"><span data-stu-id="30827-118">-Location</span></span>
<span data-ttu-id="30827-119">Расположение учетной записи для пересчета служб.</span><span class="sxs-lookup"><span data-stu-id="30827-119">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30827-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30827-120">-Name</span></span>
<span data-ttu-id="30827-121">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="30827-121">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30827-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30827-122">-ResourceGroupName</span></span>
<span data-ttu-id="30827-123">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="30827-123">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30827-124">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="30827-124">-Type</span></span>
<span data-ttu-id="30827-125">Тип учетной записи для самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="30827-125">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30827-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30827-126">CommonParameters</span></span>
<span data-ttu-id="30827-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30827-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30827-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30827-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30827-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30827-129">INPUTS</span></span>

### <span data-ttu-id="30827-130">System. String</span><span class="sxs-lookup"><span data-stu-id="30827-130">System.String</span></span>

## <span data-ttu-id="30827-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30827-131">OUTPUTS</span></span>

### <span data-ttu-id="30827-132">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="30827-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="30827-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="30827-133">NOTES</span></span>

## <span data-ttu-id="30827-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30827-134">RELATED LINKS</span></span>
