---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391028"
---
# <span data-ttu-id="4ee89-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="4ee89-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="4ee89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ee89-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee89-103">Принятие и отклонение условий для заданного имени издателя (Publisher), предложения id(Product) и плана id(Name).</span><span class="sxs-lookup"><span data-stu-id="4ee89-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="4ee89-104">Используйте Get-AzMarketplaceTerms, чтобы получить условия соглашения.</span><span class="sxs-lookup"><span data-stu-id="4ee89-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="4ee89-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ee89-105">SYNTAX</span></span>

### <span data-ttu-id="4ee89-106">AgreementAcceptParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ee89-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ee89-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ee89-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ee89-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ee89-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ee89-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ee89-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee89-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ee89-110">DESCRIPTION</span></span>
<span data-ttu-id="4ee89-111">**Cmdlet Set-AzMarketplaceTerms** сохраняет объект условий для заданного id издателя(Publisher), offer id(Product) and plan id(Name) tuple.</span><span class="sxs-lookup"><span data-stu-id="4ee89-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="4ee89-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ee89-112">EXAMPLES</span></span>

### <span data-ttu-id="4ee89-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ee89-113">Example 1</span></span>
<span data-ttu-id="4ee89-114">Получить соглашение об издателе marketplace</span><span class="sxs-lookup"><span data-stu-id="4ee89-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="4ee89-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4ee89-115">Example 2</span></span>
<span data-ttu-id="4ee89-116">Установите для соглашения издателя "Принять".</span><span class="sxs-lookup"><span data-stu-id="4ee89-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="4ee89-117">Получите значение параметра "Terms" из cmdlet 'Get-AzMarketplaceTerms'.</span><span class="sxs-lookup"><span data-stu-id="4ee89-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="4ee89-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ee89-118">PARAMETERS</span></span>

### <span data-ttu-id="4ee89-119">-Accept</span><span class="sxs-lookup"><span data-stu-id="4ee89-119">-Accept</span></span>
<span data-ttu-id="4ee89-120">Передай это, чтобы принять юридические условия.</span><span class="sxs-lookup"><span data-stu-id="4ee89-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="4ee89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee89-121">-DefaultProfile</span></span>
<span data-ttu-id="4ee89-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee89-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ee89-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ee89-123">-InputObject</span></span>
<span data-ttu-id="4ee89-124">Объект Terms, возвращаемый Get-AzMarketplaceTerms- или Get-AzMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="4ee89-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="4ee89-125">Это обязательный параметр, если параметр Accepted имеет true.</span><span class="sxs-lookup"><span data-stu-id="4ee89-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="4ee89-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4ee89-126">-Name</span></span>
<span data-ttu-id="4ee89-127">Развертывается строка идентификатора плана.</span><span class="sxs-lookup"><span data-stu-id="4ee89-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="4ee89-128">-Product</span><span class="sxs-lookup"><span data-stu-id="4ee89-128">-Product</span></span>
<span data-ttu-id="4ee89-129">Развертывается строка идентификатора предложения изображения.</span><span class="sxs-lookup"><span data-stu-id="4ee89-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="4ee89-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4ee89-130">-Publisher</span></span>
<span data-ttu-id="4ee89-131">Развертываемая строка идентификатора изображения в Publisher.</span><span class="sxs-lookup"><span data-stu-id="4ee89-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="4ee89-132">-Reject</span><span class="sxs-lookup"><span data-stu-id="4ee89-132">-Reject</span></span>
<span data-ttu-id="4ee89-133">Передай это, чтобы отклонить юридические условия.</span><span class="sxs-lookup"><span data-stu-id="4ee89-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="4ee89-134">-Terms</span><span class="sxs-lookup"><span data-stu-id="4ee89-134">-Terms</span></span>
<span data-ttu-id="4ee89-135">Объект Terms, возвращаемый Get-AzMarketplaceTerms- или Get-AzMarketplaceTerms.</span><span class="sxs-lookup"><span data-stu-id="4ee89-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="4ee89-136">Это обязательный параметр, если параметр Accepted имеет true.</span><span class="sxs-lookup"><span data-stu-id="4ee89-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="4ee89-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ee89-137">-Confirm</span></span>
<span data-ttu-id="4ee89-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4ee89-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee89-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee89-139">-WhatIf</span></span>
<span data-ttu-id="4ee89-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ee89-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ee89-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4ee89-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ee89-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee89-142">CommonParameters</span></span>
<span data-ttu-id="4ee89-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee89-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee89-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee89-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee89-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ee89-145">INPUTS</span></span>

### <span data-ttu-id="4ee89-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="4ee89-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="4ee89-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ee89-147">OUTPUTS</span></span>

### <span data-ttu-id="4ee89-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="4ee89-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="4ee89-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ee89-149">NOTES</span></span>

## <span data-ttu-id="4ee89-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ee89-150">RELATED LINKS</span></span>
