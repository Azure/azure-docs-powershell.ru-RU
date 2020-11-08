---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: cb11377c4ee18278dee2a3dc97c16bb58a02f5d5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235686"
---
# <span data-ttu-id="9b2f6-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="9b2f6-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="9b2f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2f6-103">Включает настраиваемый HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="9b2f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b2f6-104">SYNTAX</span></span>

### <span data-ttu-id="9b2f6-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b2f6-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b2f6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b2f6-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b2f6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b2f6-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b2f6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b2f6-108">DESCRIPTION</span></span>
<span data-ttu-id="9b2f6-109">Командлет **Enable-AzCdnCustomDomainHttps** обеспечивает защищенную доставку HTTPS для настраиваемого домена CDN.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="9b2f6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b2f6-110">EXAMPLES</span></span>

### <span data-ttu-id="9b2f6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b2f6-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="9b2f6-112">Включите безопасную доставку настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="9b2f6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b2f6-113">PARAMETERS</span></span>

### <span data-ttu-id="9b2f6-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="9b2f6-114">-CustomDomainName</span></span>
<span data-ttu-id="9b2f6-115">Отображаемое имя настраиваемого домена CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="9b2f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2f6-116">-DefaultProfile</span></span>
<span data-ttu-id="9b2f6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b2f6-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9b2f6-118">-EndpointName</span></span>
<span data-ttu-id="9b2f6-119">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="9b2f6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b2f6-120">-InputObject</span></span>
<span data-ttu-id="9b2f6-121">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-121">The custom domain object.</span></span>

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

### <span data-ttu-id="9b2f6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b2f6-122">-PassThru</span></span>
<span data-ttu-id="9b2f6-123">Возвращаемый объект, если он указан.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-123">Return object if specified.</span></span>

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

### <span data-ttu-id="9b2f6-124">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="9b2f6-124">-ProfileName</span></span>
<span data-ttu-id="9b2f6-125">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="9b2f6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b2f6-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b2f6-127">Группа ресурсов в профиле CDN для Azure</span><span class="sxs-lookup"><span data-stu-id="9b2f6-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="9b2f6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b2f6-128">-ResourceId</span></span>
<span data-ttu-id="9b2f6-129">ResourceId для настраиваемого домена</span><span class="sxs-lookup"><span data-stu-id="9b2f6-129">ResourceId of the Custom Domain</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2f6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b2f6-130">-Confirm</span></span>
<span data-ttu-id="9b2f6-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b2f6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b2f6-132">-WhatIf</span></span>
<span data-ttu-id="9b2f6-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b2f6-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b2f6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2f6-135">CommonParameters</span></span>
<span data-ttu-id="9b2f6-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2f6-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b2f6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2f6-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b2f6-138">INPUTS</span></span>

### <span data-ttu-id="9b2f6-139">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="9b2f6-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="9b2f6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9b2f6-140">System.String</span></span>

## <span data-ttu-id="9b2f6-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b2f6-141">OUTPUTS</span></span>

### <span data-ttu-id="9b2f6-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b2f6-142">System.Boolean</span></span>

## <span data-ttu-id="9b2f6-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b2f6-143">NOTES</span></span>

## <span data-ttu-id="9b2f6-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b2f6-144">RELATED LINKS</span></span>
