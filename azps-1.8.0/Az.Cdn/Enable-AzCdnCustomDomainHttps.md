---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 87c6928b6b1a8863bdde7126b782d07d4c496207
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731424"
---
# <span data-ttu-id="d476a-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="d476a-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="d476a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d476a-102">SYNOPSIS</span></span>
<span data-ttu-id="d476a-103">Включает настраиваемый HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d476a-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="d476a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d476a-104">SYNTAX</span></span>

### <span data-ttu-id="d476a-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d476a-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d476a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d476a-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d476a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d476a-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d476a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d476a-108">DESCRIPTION</span></span>
<span data-ttu-id="d476a-109">Командлет **Enable-AzCdnCustomDomainHttps** обеспечивает защищенную доставку HTTPS для настраиваемого домена CDN.</span><span class="sxs-lookup"><span data-stu-id="d476a-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="d476a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d476a-110">EXAMPLES</span></span>

### <span data-ttu-id="d476a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d476a-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="d476a-112">Включите безопасную доставку настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="d476a-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="d476a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d476a-113">PARAMETERS</span></span>

### <span data-ttu-id="d476a-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d476a-114">-CustomDomainName</span></span>
<span data-ttu-id="d476a-115">Отображаемое имя настраиваемого домена CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="d476a-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="d476a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d476a-116">-DefaultProfile</span></span>
<span data-ttu-id="d476a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d476a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d476a-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d476a-118">-EndpointName</span></span>
<span data-ttu-id="d476a-119">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="d476a-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d476a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d476a-120">-InputObject</span></span>
<span data-ttu-id="d476a-121">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="d476a-121">The custom domain object.</span></span>

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

### <span data-ttu-id="d476a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d476a-122">-PassThru</span></span>
<span data-ttu-id="d476a-123">Возвращаемый объект, если он указан.</span><span class="sxs-lookup"><span data-stu-id="d476a-123">Return object if specified.</span></span>

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

### <span data-ttu-id="d476a-124">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="d476a-124">-ProfileName</span></span>
<span data-ttu-id="d476a-125">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="d476a-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d476a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d476a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d476a-127">Группа ресурсов в профиле CDN для Azure</span><span class="sxs-lookup"><span data-stu-id="d476a-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="d476a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d476a-128">-ResourceId</span></span>
<span data-ttu-id="d476a-129">ResourceId для настраиваемого домена</span><span class="sxs-lookup"><span data-stu-id="d476a-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="d476a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d476a-130">-Confirm</span></span>
<span data-ttu-id="d476a-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d476a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d476a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d476a-132">-WhatIf</span></span>
<span data-ttu-id="d476a-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d476a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d476a-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d476a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d476a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d476a-135">CommonParameters</span></span>
<span data-ttu-id="d476a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d476a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d476a-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d476a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d476a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d476a-138">INPUTS</span></span>

### <span data-ttu-id="d476a-139">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d476a-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="d476a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d476a-140">System.String</span></span>

## <span data-ttu-id="d476a-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d476a-141">OUTPUTS</span></span>

### <span data-ttu-id="d476a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d476a-142">System.Boolean</span></span>

## <span data-ttu-id="d476a-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="d476a-143">NOTES</span></span>

## <span data-ttu-id="d476a-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d476a-144">RELATED LINKS</span></span>
