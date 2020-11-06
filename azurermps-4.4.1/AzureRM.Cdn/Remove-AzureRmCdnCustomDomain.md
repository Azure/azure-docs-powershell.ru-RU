---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 2aa6b3932424f7a8375cca2584a7fc7916124c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567155"
---
# <span data-ttu-id="e6ce4-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e6ce4-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="e6ce4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ce4-103">Удаление собственного домена.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6ce4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6ce4-104">SYNTAX</span></span>

### <span data-ttu-id="e6ce4-105">Параметры, заданные для параметров полей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6ce4-105">Parameter Set for fields parameters (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6ce4-106">Параметр, заданный для параметров объекта</span><span class="sxs-lookup"><span data-stu-id="e6ce4-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6ce4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6ce4-107">DESCRIPTION</span></span>
<span data-ttu-id="e6ce4-108">Командлет **Remove-AzureRmCdnCustomDomain** удаляет настраиваемый домен из конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e6ce4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6ce4-109">EXAMPLES</span></span>

## <span data-ttu-id="e6ce4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6ce4-110">PARAMETERS</span></span>

### <span data-ttu-id="e6ce4-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e6ce4-111">-CdnCustomDomain</span></span>
<span data-ttu-id="e6ce4-112">Указывает настраиваемый домен, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ce4-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e6ce4-113">-CustomDomainName</span></span>
<span data-ttu-id="e6ce4-114">Указывает имя ресурса для настраиваемого домена, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ce4-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e6ce4-115">-EndpointName</span></span>
<span data-ttu-id="e6ce4-116">Указывает имя конечной точки, из которой этот командлет удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-116">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ce4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6ce4-117">-PassThru</span></span>
<span data-ttu-id="e6ce4-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e6ce4-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6ce4-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="e6ce4-120">-ProfileName</span></span>
<span data-ttu-id="e6ce4-121">Указывает имя профиля, из которого этот командлет удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-121">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ce4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ce4-122">-ResourceGroupName</span></span>
<span data-ttu-id="e6ce4-123">Указывает имя группы ресурсов, из которой этот командлет удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-123">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ce4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6ce4-124">-Confirm</span></span>
<span data-ttu-id="e6ce4-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6ce4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6ce4-126">-WhatIf</span></span>
<span data-ttu-id="e6ce4-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6ce4-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6ce4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ce4-129">-DefaultProfile</span></span>
<span data-ttu-id="e6ce4-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6ce4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ce4-131">CommonParameters</span></span>
<span data-ttu-id="e6ce4-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ce4-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6ce4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ce4-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6ce4-134">INPUTS</span></span>

### <span data-ttu-id="e6ce4-135">PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e6ce4-135">PSCustomDomain</span></span>
<span data-ttu-id="e6ce4-136">Параметр "CdnCustomDomain" принимает значение типа "PSCustomDomain" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e6ce4-136">Parameter 'CdnCustomDomain' accepts value of type 'PSCustomDomain' from the pipeline</span></span>

## <span data-ttu-id="e6ce4-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6ce4-137">OUTPUTS</span></span>

### <span data-ttu-id="e6ce4-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6ce4-138">System.Boolean</span></span>

## <span data-ttu-id="e6ce4-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6ce4-139">NOTES</span></span>

## <span data-ttu-id="e6ce4-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6ce4-140">RELATED LINKS</span></span>

[<span data-ttu-id="e6ce4-141">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e6ce4-141">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="e6ce4-142">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e6ce4-142">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="e6ce4-143">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e6ce4-143">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


