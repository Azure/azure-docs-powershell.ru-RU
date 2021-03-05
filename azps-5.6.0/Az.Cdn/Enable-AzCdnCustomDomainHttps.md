---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 598dd0f386e82f7b195a57c72044756343ef9f56
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972963"
---
# <span data-ttu-id="0995f-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="0995f-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="0995f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0995f-102">SYNOPSIS</span></span>
<span data-ttu-id="0995f-103">Включает настраиваемую протокол HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0995f-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="0995f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0995f-104">SYNTAX</span></span>

### <span data-ttu-id="0995f-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0995f-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0995f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0995f-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0995f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0995f-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0995f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0995f-108">DESCRIPTION</span></span>
<span data-ttu-id="0995f-109">С **помощью cmdlet Enable-AzCdnCustomDomainHttps** можно обеспечить защищенную доставку HTTPS пользовательского домена CDN.</span><span class="sxs-lookup"><span data-stu-id="0995f-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="0995f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0995f-110">EXAMPLES</span></span>

### <span data-ttu-id="0995f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0995f-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="0995f-112">Обеспечивает безопасную доставку настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="0995f-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="0995f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0995f-113">PARAMETERS</span></span>

### <span data-ttu-id="0995f-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="0995f-114">-CustomDomainName</span></span>
<span data-ttu-id="0995f-115">Отображаемые имена настраиваемой доменной записи Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="0995f-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="0995f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0995f-116">-DefaultProfile</span></span>
<span data-ttu-id="0995f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0995f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0995f-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0995f-118">-EndpointName</span></span>
<span data-ttu-id="0995f-119">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="0995f-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="0995f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0995f-120">-InputObject</span></span>
<span data-ttu-id="0995f-121">Объект настраиваемного домена.</span><span class="sxs-lookup"><span data-stu-id="0995f-121">The custom domain object.</span></span>

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

### <span data-ttu-id="0995f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0995f-122">-PassThru</span></span>
<span data-ttu-id="0995f-123">Возврат объекта, если он задан.</span><span class="sxs-lookup"><span data-stu-id="0995f-123">Return object if specified.</span></span>

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

### <span data-ttu-id="0995f-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0995f-124">-ProfileName</span></span>
<span data-ttu-id="0995f-125">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="0995f-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="0995f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0995f-126">-ResourceGroupName</span></span>
<span data-ttu-id="0995f-127">Группа ресурсов профиля AZURE CDN</span><span class="sxs-lookup"><span data-stu-id="0995f-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="0995f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0995f-128">-ResourceId</span></span>
<span data-ttu-id="0995f-129">ResourceId настраиваемого домена</span><span class="sxs-lookup"><span data-stu-id="0995f-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="0995f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0995f-130">-Confirm</span></span>
<span data-ttu-id="0995f-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0995f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0995f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0995f-132">-WhatIf</span></span>
<span data-ttu-id="0995f-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0995f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0995f-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0995f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0995f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0995f-135">CommonParameters</span></span>
<span data-ttu-id="0995f-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0995f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0995f-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0995f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0995f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0995f-138">INPUTS</span></span>

### <span data-ttu-id="0995f-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0995f-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="0995f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0995f-140">System.String</span></span>

## <span data-ttu-id="0995f-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0995f-141">OUTPUTS</span></span>

### <span data-ttu-id="0995f-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0995f-142">System.Boolean</span></span>

## <span data-ttu-id="0995f-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0995f-143">NOTES</span></span>

## <span data-ttu-id="0995f-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0995f-144">RELATED LINKS</span></span>
