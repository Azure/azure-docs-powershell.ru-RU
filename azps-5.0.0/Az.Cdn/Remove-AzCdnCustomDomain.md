---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246254"
---
# <span data-ttu-id="b3176-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b3176-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="b3176-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3176-102">SYNOPSIS</span></span>
<span data-ttu-id="b3176-103">Удаление собственного домена.</span><span class="sxs-lookup"><span data-stu-id="b3176-103">Removes a custom domain.</span></span>

## <span data-ttu-id="b3176-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3176-104">SYNTAX</span></span>

### <span data-ttu-id="b3176-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3176-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3176-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3176-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3176-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3176-107">DESCRIPTION</span></span>
<span data-ttu-id="b3176-108">Командлет **Remove-AzCdnCustomDomain** удаляет настраиваемый домен из конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="b3176-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b3176-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3176-109">EXAMPLES</span></span>

## <span data-ttu-id="b3176-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3176-110">PARAMETERS</span></span>

### <span data-ttu-id="b3176-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b3176-111">-CdnCustomDomain</span></span>
<span data-ttu-id="b3176-112">Указывает настраиваемый домен, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b3176-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b3176-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="b3176-113">-CustomDomainName</span></span>
<span data-ttu-id="b3176-114">Указывает имя ресурса для настраиваемого домена, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b3176-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b3176-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3176-115">-DefaultProfile</span></span>
<span data-ttu-id="b3176-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b3176-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3176-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b3176-117">-EndpointName</span></span>
<span data-ttu-id="b3176-118">Указывает имя конечной точки, из которой этот командлет удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="b3176-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="b3176-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3176-119">-PassThru</span></span>
<span data-ttu-id="b3176-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b3176-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b3176-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b3176-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3176-122">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="b3176-122">-ProfileName</span></span>
<span data-ttu-id="b3176-123">Указывает имя профиля, из которого этот командлет удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="b3176-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="b3176-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3176-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3176-125">Указывает имя группы ресурсов, из которой этот командлет удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="b3176-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="b3176-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3176-126">-Confirm</span></span>
<span data-ttu-id="b3176-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b3176-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3176-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3176-128">-WhatIf</span></span>
<span data-ttu-id="b3176-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b3176-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3176-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b3176-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3176-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3176-131">CommonParameters</span></span>
<span data-ttu-id="b3176-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3176-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3176-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3176-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3176-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3176-134">INPUTS</span></span>

### <span data-ttu-id="b3176-135">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b3176-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="b3176-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3176-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b3176-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3176-137">OUTPUTS</span></span>

### <span data-ttu-id="b3176-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3176-138">System.Boolean</span></span>

## <span data-ttu-id="b3176-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3176-139">NOTES</span></span>

## <span data-ttu-id="b3176-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3176-140">RELATED LINKS</span></span>

[<span data-ttu-id="b3176-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b3176-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="b3176-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b3176-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="b3176-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="b3176-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


