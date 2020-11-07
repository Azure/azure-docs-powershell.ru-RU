---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 7932a733fcd672d8ee92e6452765745281ee0a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732244"
---
# <span data-ttu-id="ba094-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ba094-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="ba094-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba094-102">SYNOPSIS</span></span>
<span data-ttu-id="ba094-103">Принять или отклонить условия для определенного идентификатора издателя (издателя), идентификатора предложения (продукта) и кода плана (имя).</span><span class="sxs-lookup"><span data-stu-id="ba094-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ba094-104">Пожалуйста, используй Get-AzureRmMarketplaceTerms, чтобы получить условия соглашения.</span><span class="sxs-lookup"><span data-stu-id="ba094-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba094-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba094-105">SYNTAX</span></span>

### <span data-ttu-id="ba094-106">AgreementAcceptParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba094-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba094-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba094-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba094-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba094-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba094-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba094-109">InputObjectRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba094-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba094-110">DESCRIPTION</span></span>
<span data-ttu-id="ba094-111">Командлет **Set-AzureRmMarketplaceTerms** сохраняет объект термов для указанного идентификатора издателя (издателя), кода предложения ID (Product) и кода плана (имени).</span><span class="sxs-lookup"><span data-stu-id="ba094-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="ba094-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba094-112">EXAMPLES</span></span>

### <span data-ttu-id="ba094-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba094-113">Example 1</span></span>
<span data-ttu-id="ba094-114">Получение соглашения об издателе Marketplace</span><span class="sxs-lookup"><span data-stu-id="ba094-114">Get the marketplace publisher agreement</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

### <span data-ttu-id="ba094-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ba094-115">Example 2</span></span>
<span data-ttu-id="ba094-116">Установите для соглашения об издателе значение "принято".</span><span class="sxs-lookup"><span data-stu-id="ba094-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="ba094-117">Получение значения параметра "термины" из командлета Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ba094-117">Get the value for the 'Terms' parameter from the 'Get-AzureRmMarketplaceTerms' cmdlet</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```


## <span data-ttu-id="ba094-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba094-118">PARAMETERS</span></span>

### <span data-ttu-id="ba094-119">-Принято</span><span class="sxs-lookup"><span data-stu-id="ba094-119">-Accept</span></span>
<span data-ttu-id="ba094-120">Передайте его, чтобы получить юридические условия.</span><span class="sxs-lookup"><span data-stu-id="ba094-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba094-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba094-121">-DefaultProfile</span></span>
<span data-ttu-id="ba094-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba094-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba094-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba094-123">-InputObject</span></span>
<span data-ttu-id="ba094-124">Объект термов, возвращаемый в командлете Get-AzureRmMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="ba094-124">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="ba094-125">Это обязательный параметр, если допустимые условия имеют значение истина.</span><span class="sxs-lookup"><span data-stu-id="ba094-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba094-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba094-126">-Name</span></span>
<span data-ttu-id="ba094-127">Строка идентификатора плана развертываемого изображения.</span><span class="sxs-lookup"><span data-stu-id="ba094-127">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba094-128">-Product</span><span class="sxs-lookup"><span data-stu-id="ba094-128">-Product</span></span>
<span data-ttu-id="ba094-129">Строка идентификатора предложения с развернутым изображением.</span><span class="sxs-lookup"><span data-stu-id="ba094-129">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba094-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ba094-130">-Publisher</span></span>
<span data-ttu-id="ba094-131">Строка идентификатора издателя развертываемого изображения.</span><span class="sxs-lookup"><span data-stu-id="ba094-131">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba094-132">-Отклонить</span><span class="sxs-lookup"><span data-stu-id="ba094-132">-Reject</span></span>
<span data-ttu-id="ba094-133">Передайте это, чтобы отклонить юридические условия.</span><span class="sxs-lookup"><span data-stu-id="ba094-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba094-134">-Условия</span><span class="sxs-lookup"><span data-stu-id="ba094-134">-Terms</span></span>
<span data-ttu-id="ba094-135">Объект термов, возвращаемый в командлете Get-AzureRmMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="ba094-135">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="ba094-136">Это обязательный параметр, если допустимые условия имеют значение истина.</span><span class="sxs-lookup"><span data-stu-id="ba094-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba094-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba094-137">-Confirm</span></span>
<span data-ttu-id="ba094-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba094-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba094-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba094-139">-WhatIf</span></span>
<span data-ttu-id="ba094-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba094-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba094-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba094-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba094-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba094-142">CommonParameters</span></span>
<span data-ttu-id="ba094-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba094-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba094-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba094-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba094-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba094-145">INPUTS</span></span>

### <span data-ttu-id="ba094-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="ba094-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="ba094-147">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ba094-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ba094-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba094-148">OUTPUTS</span></span>

### <span data-ttu-id="ba094-149">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="ba094-149">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="ba094-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba094-150">NOTES</span></span>

## <span data-ttu-id="ba094-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba094-151">RELATED LINKS</span></span>
