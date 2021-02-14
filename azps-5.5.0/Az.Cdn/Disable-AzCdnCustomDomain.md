---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234900"
---
# <span data-ttu-id="558cf-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="558cf-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="558cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="558cf-102">SYNOPSIS</span></span>
<span data-ttu-id="558cf-103">Отключение протокола HTTPS (неподготовленного домена).</span><span class="sxs-lookup"><span data-stu-id="558cf-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="558cf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="558cf-104">SYNTAX</span></span>

### <span data-ttu-id="558cf-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="558cf-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="558cf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="558cf-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="558cf-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="558cf-107">DESCRIPTION</span></span>
<span data-ttu-id="558cf-108">**Cmdlet Disable-AzCdnCustomDomain** отключает защищенную доставку HTTPS пользовательского домена CDN.</span><span class="sxs-lookup"><span data-stu-id="558cf-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="558cf-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="558cf-109">EXAMPLES</span></span>

### <span data-ttu-id="558cf-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="558cf-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="558cf-111">Отключать доставку https для пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="558cf-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="558cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="558cf-112">PARAMETERS</span></span>

### <span data-ttu-id="558cf-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="558cf-113">-CustomDomainName</span></span>
<span data-ttu-id="558cf-114">Отображаемые имена настраиваемой доменной записи Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="558cf-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="558cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="558cf-115">-DefaultProfile</span></span>
<span data-ttu-id="558cf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="558cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="558cf-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="558cf-117">-EndpointName</span></span>
<span data-ttu-id="558cf-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="558cf-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="558cf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="558cf-119">-InputObject</span></span>
<span data-ttu-id="558cf-120">Объект пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="558cf-120">The custom domain object.</span></span>

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

### <span data-ttu-id="558cf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="558cf-121">-PassThru</span></span>
<span data-ttu-id="558cf-122">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="558cf-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="558cf-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="558cf-123">-ProfileName</span></span>
<span data-ttu-id="558cf-124">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="558cf-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="558cf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="558cf-125">-ResourceGroupName</span></span>
<span data-ttu-id="558cf-126">Группа ресурсов профиля Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="558cf-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="558cf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="558cf-127">-Confirm</span></span>
<span data-ttu-id="558cf-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="558cf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="558cf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="558cf-129">-WhatIf</span></span>
<span data-ttu-id="558cf-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="558cf-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="558cf-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="558cf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="558cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="558cf-132">CommonParameters</span></span>
<span data-ttu-id="558cf-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="558cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="558cf-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="558cf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="558cf-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="558cf-135">INPUTS</span></span>

### <span data-ttu-id="558cf-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="558cf-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="558cf-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="558cf-137">OUTPUTS</span></span>

### <span data-ttu-id="558cf-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="558cf-138">System.Boolean</span></span>

## <span data-ttu-id="558cf-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="558cf-139">NOTES</span></span>

## <span data-ttu-id="558cf-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="558cf-140">RELATED LINKS</span></span>
