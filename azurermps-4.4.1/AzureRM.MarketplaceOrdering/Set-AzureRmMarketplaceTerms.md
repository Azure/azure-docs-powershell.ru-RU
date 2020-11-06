---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 843bb68c5aebc18af60e1cc74915b269738059f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569351"
---
# <span data-ttu-id="21f3b-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="21f3b-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="21f3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="21f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="21f3b-103">Принять или отклонить условия для определенного идентификатора издателя (издателя), идентификатора предложения (продукта) и кода плана (имя).</span><span class="sxs-lookup"><span data-stu-id="21f3b-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="21f3b-104">Пожалуйста, используй Get-AzureRmMarketplaceTerms, чтобы получить условия соглашения.</span><span class="sxs-lookup"><span data-stu-id="21f3b-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21f3b-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="21f3b-105">SYNTAX</span></span>

### <span data-ttu-id="21f3b-106">AgreementAcceptParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="21f3b-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21f3b-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f3b-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21f3b-108">InputObjectAcceptParametrSet</span><span class="sxs-lookup"><span data-stu-id="21f3b-108">InputObjectAcceptParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f3b-109">InputObjectRejectParametrSet</span><span class="sxs-lookup"><span data-stu-id="21f3b-109">InputObjectRejectParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21f3b-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21f3b-110">DESCRIPTION</span></span>
<span data-ttu-id="21f3b-111">Командлет **Set-AzureRmMarketplaceTerms** сохраняет объект термов для указанного идентификатора издателя (издателя), кода предложения ID (Product) и кода плана (имени).</span><span class="sxs-lookup"><span data-stu-id="21f3b-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="21f3b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="21f3b-112">EXAMPLES</span></span>

### <span data-ttu-id="21f3b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="21f3b-113">Example 1</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### <span data-ttu-id="21f3b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="21f3b-114">Example 2</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## <span data-ttu-id="21f3b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="21f3b-115">PARAMETERS</span></span>

### <span data-ttu-id="21f3b-116">-Принято</span><span class="sxs-lookup"><span data-stu-id="21f3b-116">-Accept</span></span>
<span data-ttu-id="21f3b-117">Передайте его, чтобы получить юридические условия.</span><span class="sxs-lookup"><span data-stu-id="21f3b-117">Pass this to accept the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f3b-118">-DefaultProfile</span></span>
<span data-ttu-id="21f3b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="21f3b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21f3b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21f3b-120">-InputObject</span></span>
<span data-ttu-id="21f3b-121">Объект термов, возвращаемый в командлете Get-AzureRmMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="21f3b-121">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="21f3b-122">Это обязательный параметр, если допустимые условия имеют значение истина.</span><span class="sxs-lookup"><span data-stu-id="21f3b-122">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21f3b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="21f3b-123">-Name</span></span>
<span data-ttu-id="21f3b-124">Строка идентификатора плана развертываемого изображения.</span><span class="sxs-lookup"><span data-stu-id="21f3b-124">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3b-125">-Product</span><span class="sxs-lookup"><span data-stu-id="21f3b-125">-Product</span></span>
<span data-ttu-id="21f3b-126">Строка идентификатора предложения с развернутым изображением.</span><span class="sxs-lookup"><span data-stu-id="21f3b-126">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3b-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="21f3b-127">-Publisher</span></span>
<span data-ttu-id="21f3b-128">Строка идентификатора издателя развертываемого изображения.</span><span class="sxs-lookup"><span data-stu-id="21f3b-128">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3b-129">-Отклонить</span><span class="sxs-lookup"><span data-stu-id="21f3b-129">-Reject</span></span>
<span data-ttu-id="21f3b-130">Передайте это, чтобы отклонить юридические условия.</span><span class="sxs-lookup"><span data-stu-id="21f3b-130">Pass this to reject the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3b-131">-Условия</span><span class="sxs-lookup"><span data-stu-id="21f3b-131">-Terms</span></span>
<span data-ttu-id="21f3b-132">Объект термов, возвращаемый в командлете Get-AzureRmMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="21f3b-132">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="21f3b-133">Это обязательный параметр, если допустимые условия имеют значение истина.</span><span class="sxs-lookup"><span data-stu-id="21f3b-133">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21f3b-134">-Confirm</span></span>
<span data-ttu-id="21f3b-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="21f3b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f3b-136">-WhatIf</span></span>
<span data-ttu-id="21f3b-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="21f3b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21f3b-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="21f3b-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f3b-139">CommonParameters</span></span>
<span data-ttu-id="21f3b-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="21f3b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f3b-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21f3b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f3b-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="21f3b-142">INPUTS</span></span>

### <span data-ttu-id="21f3b-143">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="21f3b-143">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="21f3b-144">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="21f3b-144">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="21f3b-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="21f3b-145">OUTPUTS</span></span>

### <span data-ttu-id="21f3b-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="21f3b-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="21f3b-147">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="21f3b-147">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="21f3b-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="21f3b-148">NOTES</span></span>

## <span data-ttu-id="21f3b-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21f3b-149">RELATED LINKS</span></span>

