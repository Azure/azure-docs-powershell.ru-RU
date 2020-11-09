---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: eebc75ba8f8f1a55fb4c1db2e7929ce233d93a23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249211"
---
# <span data-ttu-id="c6292-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c6292-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="c6292-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6292-102">SYNOPSIS</span></span>
<span data-ttu-id="c6292-103">Включает настраиваемый домен HTTPS (устаревший).</span><span class="sxs-lookup"><span data-stu-id="c6292-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="c6292-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6292-104">SYNTAX</span></span>

### <span data-ttu-id="c6292-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6292-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6292-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6292-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6292-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6292-107">DESCRIPTION</span></span>
<span data-ttu-id="c6292-108">Командлет **Enable-AzCdnCustomDomain** обеспечивает защищенную доставку HTTPS для настраиваемого домена CDN.</span><span class="sxs-lookup"><span data-stu-id="c6292-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="c6292-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6292-109">EXAMPLES</span></span>

### <span data-ttu-id="c6292-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c6292-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="c6292-111">Разрешите доставку по протоколу HTTPS для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="c6292-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="c6292-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6292-112">PARAMETERS</span></span>

### <span data-ttu-id="c6292-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c6292-113">-CustomDomainName</span></span>
<span data-ttu-id="c6292-114">Отображаемое имя настраиваемого домена CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="c6292-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="c6292-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6292-115">-DefaultProfile</span></span>
<span data-ttu-id="c6292-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6292-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6292-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c6292-117">-EndpointName</span></span>
<span data-ttu-id="c6292-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="c6292-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="c6292-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6292-119">-InputObject</span></span>
<span data-ttu-id="c6292-120">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="c6292-120">The custom domain object.</span></span>

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

### <span data-ttu-id="c6292-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6292-121">-PassThru</span></span>
<span data-ttu-id="c6292-122">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="c6292-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="c6292-123">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="c6292-123">-ProfileName</span></span>
<span data-ttu-id="c6292-124">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="c6292-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="c6292-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6292-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6292-126">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="c6292-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="c6292-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6292-127">-Confirm</span></span>
<span data-ttu-id="c6292-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6292-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6292-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6292-129">-WhatIf</span></span>
<span data-ttu-id="c6292-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6292-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6292-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6292-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6292-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6292-132">CommonParameters</span></span>
<span data-ttu-id="c6292-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6292-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6292-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6292-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6292-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6292-135">INPUTS</span></span>

### <span data-ttu-id="c6292-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c6292-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="c6292-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6292-137">OUTPUTS</span></span>

### <span data-ttu-id="c6292-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6292-138">System.Boolean</span></span>

## <span data-ttu-id="c6292-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6292-139">NOTES</span></span>

## <span data-ttu-id="c6292-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6292-140">RELATED LINKS</span></span>