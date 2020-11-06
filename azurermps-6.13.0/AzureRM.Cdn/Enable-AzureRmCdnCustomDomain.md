---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/enable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 50c1bf02a8952bbbddd2bbb82e55441adacd6a2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556804"
---
# <span data-ttu-id="77ae6-101">Enable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="77ae6-101">Enable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="77ae6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="77ae6-103">Включает настраиваемый HTTPS.</span><span class="sxs-lookup"><span data-stu-id="77ae6-103">Enables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77ae6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77ae6-104">SYNTAX</span></span>

### <span data-ttu-id="77ae6-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77ae6-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77ae6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77ae6-106">ByObjectParameterSet</span></span>
```
Enable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77ae6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77ae6-107">DESCRIPTION</span></span>
<span data-ttu-id="77ae6-108">Командлет **Enable-AzureRmCdnCustomDomain** обеспечивает защищенную доставку HTTPS для настраиваемого домена CDN.</span><span class="sxs-lookup"><span data-stu-id="77ae6-108">The **Enable-AzureRmCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="77ae6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77ae6-109">EXAMPLES</span></span>

### <span data-ttu-id="77ae6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77ae6-110">Example 1</span></span>
```powershell
Enable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="77ae6-111">Разрешите доставку по протоколу HTTPS для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="77ae6-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="77ae6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77ae6-112">PARAMETERS</span></span>

### <span data-ttu-id="77ae6-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="77ae6-113">-CustomDomainName</span></span>
<span data-ttu-id="77ae6-114">Отображаемое имя настраиваемого домена CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="77ae6-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="77ae6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ae6-115">-DefaultProfile</span></span>
<span data-ttu-id="77ae6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77ae6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77ae6-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="77ae6-117">-EndpointName</span></span>
<span data-ttu-id="77ae6-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="77ae6-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="77ae6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77ae6-119">-InputObject</span></span>
<span data-ttu-id="77ae6-120">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="77ae6-120">The custom domain object.</span></span>

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

### <span data-ttu-id="77ae6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77ae6-121">-PassThru</span></span>
<span data-ttu-id="77ae6-122">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="77ae6-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="77ae6-123">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="77ae6-123">-ProfileName</span></span>
<span data-ttu-id="77ae6-124">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="77ae6-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="77ae6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ae6-125">-ResourceGroupName</span></span>
<span data-ttu-id="77ae6-126">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="77ae6-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="77ae6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77ae6-127">-Confirm</span></span>
<span data-ttu-id="77ae6-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="77ae6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77ae6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77ae6-129">-WhatIf</span></span>
<span data-ttu-id="77ae6-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="77ae6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77ae6-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="77ae6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77ae6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ae6-132">CommonParameters</span></span>
<span data-ttu-id="77ae6-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77ae6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ae6-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77ae6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ae6-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77ae6-135">INPUTS</span></span>

### <span data-ttu-id="77ae6-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="77ae6-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="77ae6-137">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77ae6-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="77ae6-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77ae6-138">OUTPUTS</span></span>

### <span data-ttu-id="77ae6-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77ae6-139">System.Boolean</span></span>

## <span data-ttu-id="77ae6-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="77ae6-140">NOTES</span></span>

## <span data-ttu-id="77ae6-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77ae6-141">RELATED LINKS</span></span>
