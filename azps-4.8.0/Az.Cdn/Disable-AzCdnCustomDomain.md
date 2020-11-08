---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242899"
---
# <span data-ttu-id="e2f8f-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e2f8f-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="e2f8f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f8f-103">Отключение пользовательского доменного HTTPS (устарело).</span><span class="sxs-lookup"><span data-stu-id="e2f8f-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="e2f8f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2f8f-104">SYNTAX</span></span>

### <span data-ttu-id="e2f8f-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2f8f-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2f8f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2f8f-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2f8f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f8f-107">DESCRIPTION</span></span>
<span data-ttu-id="e2f8f-108">Командлет **Disable-AzCdnCustomDomain** отключает защищенную доставку HTTPS для настраиваемого домена CDN.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="e2f8f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2f8f-109">EXAMPLES</span></span>

### <span data-ttu-id="e2f8f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2f8f-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="e2f8f-111">Отключите доставку по протоколу HTTPS для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="e2f8f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2f8f-112">PARAMETERS</span></span>

### <span data-ttu-id="e2f8f-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="e2f8f-113">-CustomDomainName</span></span>
<span data-ttu-id="e2f8f-114">Отображаемое имя настраиваемого домена CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="e2f8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f8f-115">-DefaultProfile</span></span>
<span data-ttu-id="e2f8f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2f8f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e2f8f-117">-EndpointName</span></span>
<span data-ttu-id="e2f8f-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="e2f8f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2f8f-119">-InputObject</span></span>
<span data-ttu-id="e2f8f-120">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-120">The custom domain object.</span></span>

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

### <span data-ttu-id="e2f8f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2f8f-121">-PassThru</span></span>
<span data-ttu-id="e2f8f-122">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="e2f8f-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f8f-123">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="e2f8f-123">-ProfileName</span></span>
<span data-ttu-id="e2f8f-124">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="e2f8f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f8f-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2f8f-126">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="e2f8f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2f8f-127">-Confirm</span></span>
<span data-ttu-id="e2f8f-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2f8f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f8f-129">-WhatIf</span></span>
<span data-ttu-id="e2f8f-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2f8f-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2f8f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f8f-132">CommonParameters</span></span>
<span data-ttu-id="e2f8f-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2f8f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f8f-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2f8f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f8f-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2f8f-135">INPUTS</span></span>

### <span data-ttu-id="e2f8f-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="e2f8f-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="e2f8f-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f8f-137">OUTPUTS</span></span>

### <span data-ttu-id="e2f8f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2f8f-138">System.Boolean</span></span>

## <span data-ttu-id="e2f8f-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2f8f-139">NOTES</span></span>

## <span data-ttu-id="e2f8f-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2f8f-140">RELATED LINKS</span></span>
