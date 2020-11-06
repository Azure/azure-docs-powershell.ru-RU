---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: fa0e3682d62f01d7d305d190c6765aab709bed15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565891"
---
# <span data-ttu-id="be346-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be346-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="be346-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be346-102">SYNOPSIS</span></span>
<span data-ttu-id="be346-103">Удаление собственного домена.</span><span class="sxs-lookup"><span data-stu-id="be346-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be346-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be346-104">SYNTAX</span></span>

### <span data-ttu-id="be346-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be346-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be346-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be346-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be346-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be346-107">DESCRIPTION</span></span>
<span data-ttu-id="be346-108">Командлет **Remove-AzureRmCdnCustomDomain** удаляет настраиваемый домен из конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="be346-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="be346-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be346-109">EXAMPLES</span></span>

## <span data-ttu-id="be346-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be346-110">PARAMETERS</span></span>

### <span data-ttu-id="be346-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be346-111">-CdnCustomDomain</span></span>
<span data-ttu-id="be346-112">Указывает настраиваемый домен, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="be346-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be346-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="be346-113">-CustomDomainName</span></span>
<span data-ttu-id="be346-114">Указывает имя ресурса для настраиваемого домена, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="be346-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be346-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be346-115">-DefaultProfile</span></span>
<span data-ttu-id="be346-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="be346-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be346-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="be346-117">-EndpointName</span></span>
<span data-ttu-id="be346-118">Указывает имя конечной точки, из которой этот командлет удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="be346-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be346-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be346-119">-PassThru</span></span>
<span data-ttu-id="be346-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="be346-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="be346-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="be346-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be346-122">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="be346-122">-ProfileName</span></span>
<span data-ttu-id="be346-123">Указывает имя профиля, из которого этот командлет удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="be346-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be346-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be346-124">-ResourceGroupName</span></span>
<span data-ttu-id="be346-125">Указывает имя группы ресурсов, из которой этот командлет удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="be346-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be346-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be346-126">-Confirm</span></span>
<span data-ttu-id="be346-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be346-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be346-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be346-128">-WhatIf</span></span>
<span data-ttu-id="be346-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be346-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be346-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be346-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be346-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be346-131">CommonParameters</span></span>
<span data-ttu-id="be346-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be346-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be346-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be346-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be346-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be346-134">INPUTS</span></span>

### <span data-ttu-id="be346-135">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be346-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="be346-136">Параметры: CdnCustomDomain (ByValue)</span><span class="sxs-lookup"><span data-stu-id="be346-136">Parameters: CdnCustomDomain (ByValue)</span></span>

### <span data-ttu-id="be346-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="be346-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="be346-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be346-138">OUTPUTS</span></span>

### <span data-ttu-id="be346-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="be346-139">System.Boolean</span></span>

## <span data-ttu-id="be346-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="be346-140">NOTES</span></span>

## <span data-ttu-id="be346-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be346-141">RELATED LINKS</span></span>

[<span data-ttu-id="be346-142">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be346-142">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="be346-143">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be346-143">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="be346-144">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="be346-144">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


