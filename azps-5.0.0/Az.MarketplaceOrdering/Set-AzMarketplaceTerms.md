---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250087"
---
# <span data-ttu-id="a053d-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a053d-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="a053d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a053d-102">SYNOPSIS</span></span>
<span data-ttu-id="a053d-103">Принять или отклонить условия для определенного идентификатора издателя (издателя), идентификатора предложения (продукта) и кода плана (имя).</span><span class="sxs-lookup"><span data-stu-id="a053d-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="a053d-104">Пожалуйста, используй Get-AzMarketplaceTerms, чтобы получить условия соглашения.</span><span class="sxs-lookup"><span data-stu-id="a053d-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="a053d-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a053d-105">SYNTAX</span></span>

### <span data-ttu-id="a053d-106">AgreementAcceptParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a053d-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a053d-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a053d-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a053d-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="a053d-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a053d-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a053d-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a053d-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a053d-110">DESCRIPTION</span></span>
<span data-ttu-id="a053d-111">Командлет **Set-AzMarketplaceTerms** сохраняет объект термов для указанного идентификатора издателя (издателя), кода предложения ID (Product) и кода плана (имени).</span><span class="sxs-lookup"><span data-stu-id="a053d-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="a053d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a053d-112">EXAMPLES</span></span>

### <span data-ttu-id="a053d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a053d-113">Example 1</span></span>
<span data-ttu-id="a053d-114">Получение соглашения об издателе Marketplace</span><span class="sxs-lookup"><span data-stu-id="a053d-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="a053d-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a053d-115">Example 2</span></span>
<span data-ttu-id="a053d-116">Установите для соглашения об издателе значение "принято".</span><span class="sxs-lookup"><span data-stu-id="a053d-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="a053d-117">Получение значения параметра "термины" из командлета Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a053d-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="a053d-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a053d-118">PARAMETERS</span></span>

### <span data-ttu-id="a053d-119">-Принято</span><span class="sxs-lookup"><span data-stu-id="a053d-119">-Accept</span></span>
<span data-ttu-id="a053d-120">Передайте его, чтобы получить юридические условия.</span><span class="sxs-lookup"><span data-stu-id="a053d-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a053d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a053d-121">-DefaultProfile</span></span>
<span data-ttu-id="a053d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a053d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a053d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a053d-123">-InputObject</span></span>
<span data-ttu-id="a053d-124">Объект термов, возвращаемый в командлете Get-AzMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="a053d-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="a053d-125">Этот параметр является обязательным, если параметр "принято" имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="a053d-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a053d-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a053d-126">-Name</span></span>
<span data-ttu-id="a053d-127">Строка идентификатора плана развертываемого изображения.</span><span class="sxs-lookup"><span data-stu-id="a053d-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="a053d-128">-Product</span><span class="sxs-lookup"><span data-stu-id="a053d-128">-Product</span></span>
<span data-ttu-id="a053d-129">Строка идентификатора предложения с развернутым изображением.</span><span class="sxs-lookup"><span data-stu-id="a053d-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="a053d-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a053d-130">-Publisher</span></span>
<span data-ttu-id="a053d-131">Строка идентификатора издателя развертываемого изображения.</span><span class="sxs-lookup"><span data-stu-id="a053d-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="a053d-132">-Отклонить</span><span class="sxs-lookup"><span data-stu-id="a053d-132">-Reject</span></span>
<span data-ttu-id="a053d-133">Передайте это, чтобы отклонить юридические условия.</span><span class="sxs-lookup"><span data-stu-id="a053d-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a053d-134">-Условия</span><span class="sxs-lookup"><span data-stu-id="a053d-134">-Terms</span></span>
<span data-ttu-id="a053d-135">Объект термов, возвращаемый в командлете Get-AzMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="a053d-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="a053d-136">Этот параметр является обязательным, если параметр "принято" имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="a053d-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="a053d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a053d-137">-Confirm</span></span>
<span data-ttu-id="a053d-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a053d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a053d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a053d-139">-WhatIf</span></span>
<span data-ttu-id="a053d-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a053d-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a053d-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a053d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a053d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a053d-142">CommonParameters</span></span>
<span data-ttu-id="a053d-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a053d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a053d-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a053d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a053d-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a053d-145">INPUTS</span></span>

### <span data-ttu-id="a053d-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a053d-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="a053d-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a053d-147">OUTPUTS</span></span>

### <span data-ttu-id="a053d-148">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a053d-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="a053d-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="a053d-149">NOTES</span></span>

## <span data-ttu-id="a053d-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a053d-150">RELATED LINKS</span></span>
