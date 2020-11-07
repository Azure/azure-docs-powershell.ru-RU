---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: c3b2cadcdcc57ffc2cba8281af804e0c98c800bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727618"
---
# <span data-ttu-id="f81b2-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="f81b2-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="f81b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f81b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f81b2-103">Отключение настраиваемого HTTPS домена.</span><span class="sxs-lookup"><span data-stu-id="f81b2-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="f81b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f81b2-104">SYNTAX</span></span>

### <span data-ttu-id="f81b2-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f81b2-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f81b2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f81b2-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f81b2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f81b2-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f81b2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f81b2-108">DESCRIPTION</span></span>
<span data-ttu-id="f81b2-109">Командлет **Disable-AzCdnCustomDomainHttps** отключает защищенную доставку HTTPS для настраиваемого домена CDN.</span><span class="sxs-lookup"><span data-stu-id="f81b2-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="f81b2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f81b2-110">EXAMPLES</span></span>

### <span data-ttu-id="f81b2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f81b2-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="f81b2-112">Отключите безопасную доставку настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="f81b2-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="f81b2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f81b2-113">PARAMETERS</span></span>

### <span data-ttu-id="f81b2-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="f81b2-114">-CustomDomainName</span></span>
<span data-ttu-id="f81b2-115">Отображаемое имя настраиваемого домена CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="f81b2-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="f81b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f81b2-116">-DefaultProfile</span></span>
<span data-ttu-id="f81b2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f81b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f81b2-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f81b2-118">-EndpointName</span></span>
<span data-ttu-id="f81b2-119">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="f81b2-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="f81b2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f81b2-120">-InputObject</span></span>
<span data-ttu-id="f81b2-121">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="f81b2-121">The custom domain object.</span></span>

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

### <span data-ttu-id="f81b2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f81b2-122">-PassThru</span></span>
<span data-ttu-id="f81b2-123">Возвращаемый объект, если он указан.</span><span class="sxs-lookup"><span data-stu-id="f81b2-123">Return object if specified.</span></span>

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

### <span data-ttu-id="f81b2-124">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="f81b2-124">-ProfileName</span></span>
<span data-ttu-id="f81b2-125">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="f81b2-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="f81b2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f81b2-126">-ResourceGroupName</span></span>
<span data-ttu-id="f81b2-127">Группа ресурсов в профиле CDN для Azure</span><span class="sxs-lookup"><span data-stu-id="f81b2-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="f81b2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f81b2-128">-ResourceId</span></span>
<span data-ttu-id="f81b2-129">ResourceId для настраиваемого домена</span><span class="sxs-lookup"><span data-stu-id="f81b2-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="f81b2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f81b2-130">-Confirm</span></span>
<span data-ttu-id="f81b2-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f81b2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f81b2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f81b2-132">-WhatIf</span></span>
<span data-ttu-id="f81b2-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f81b2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f81b2-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f81b2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f81b2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f81b2-135">CommonParameters</span></span>
<span data-ttu-id="f81b2-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f81b2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f81b2-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f81b2-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f81b2-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f81b2-138">INPUTS</span></span>

### <span data-ttu-id="f81b2-139">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f81b2-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="f81b2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f81b2-140">System.String</span></span>

## <span data-ttu-id="f81b2-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f81b2-141">OUTPUTS</span></span>

### <span data-ttu-id="f81b2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f81b2-142">System.Boolean</span></span>

## <span data-ttu-id="f81b2-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="f81b2-143">NOTES</span></span>

## <span data-ttu-id="f81b2-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f81b2-144">RELATED LINKS</span></span>
