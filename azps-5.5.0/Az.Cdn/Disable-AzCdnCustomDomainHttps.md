---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: be3e4d0437e24a282c1933cf82e1818dd9f88221
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215948"
---
# <span data-ttu-id="d9ac0-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="d9ac0-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="d9ac0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ac0-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ac0-103">Отключение пользовательского домена HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="d9ac0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d9ac0-104">SYNTAX</span></span>

### <span data-ttu-id="d9ac0-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d9ac0-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9ac0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9ac0-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ac0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9ac0-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9ac0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9ac0-108">DESCRIPTION</span></span>
<span data-ttu-id="d9ac0-109">Cmdlet **Disable-AzCdnCustomDomainHttps** отключает защищенную доставку HTTPS пользовательского домена CDN.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="d9ac0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d9ac0-110">EXAMPLES</span></span>

### <span data-ttu-id="d9ac0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9ac0-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="d9ac0-112">Отключать безопасную доставку настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="d9ac0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9ac0-113">PARAMETERS</span></span>

### <span data-ttu-id="d9ac0-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d9ac0-114">-CustomDomainName</span></span>
<span data-ttu-id="d9ac0-115">Отображаемые имена настраиваемой доменной записи Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="d9ac0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ac0-116">-DefaultProfile</span></span>
<span data-ttu-id="d9ac0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9ac0-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d9ac0-118">-EndpointName</span></span>
<span data-ttu-id="d9ac0-119">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d9ac0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9ac0-120">-InputObject</span></span>
<span data-ttu-id="d9ac0-121">Объект настраиваемного домена.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-121">The custom domain object.</span></span>

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

### <span data-ttu-id="d9ac0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9ac0-122">-PassThru</span></span>
<span data-ttu-id="d9ac0-123">Возврат объекта, если он задан.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-123">Return object if specified.</span></span>

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

### <span data-ttu-id="d9ac0-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d9ac0-124">-ProfileName</span></span>
<span data-ttu-id="d9ac0-125">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d9ac0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ac0-126">-ResourceGroupName</span></span>
<span data-ttu-id="d9ac0-127">Группа ресурсов профиля AZURE CDN</span><span class="sxs-lookup"><span data-stu-id="d9ac0-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="d9ac0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9ac0-128">-ResourceId</span></span>
<span data-ttu-id="d9ac0-129">ResourceId настраиваемого домена</span><span class="sxs-lookup"><span data-stu-id="d9ac0-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="d9ac0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9ac0-130">-Confirm</span></span>
<span data-ttu-id="d9ac0-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9ac0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9ac0-132">-WhatIf</span></span>
<span data-ttu-id="d9ac0-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9ac0-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9ac0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ac0-135">CommonParameters</span></span>
<span data-ttu-id="d9ac0-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ac0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ac0-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9ac0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ac0-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d9ac0-138">INPUTS</span></span>

### <span data-ttu-id="d9ac0-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d9ac0-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="d9ac0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d9ac0-140">System.String</span></span>

## <span data-ttu-id="d9ac0-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d9ac0-141">OUTPUTS</span></span>

### <span data-ttu-id="d9ac0-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d9ac0-142">System.Boolean</span></span>

## <span data-ttu-id="d9ac0-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d9ac0-143">NOTES</span></span>

## <span data-ttu-id="d9ac0-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9ac0-144">RELATED LINKS</span></span>
