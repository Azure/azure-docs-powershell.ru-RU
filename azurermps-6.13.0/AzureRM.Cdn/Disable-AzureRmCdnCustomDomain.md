---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/disable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Disable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 1f0694d93f95f9fed6f23d7912003a179598ac91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565898"
---
# <span data-ttu-id="7c7ad-101">Disable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7c7ad-101">Disable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="7c7ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7ad-103">Отключает настраиваемый HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-103">Disables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c7ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c7ad-104">SYNTAX</span></span>

### <span data-ttu-id="7c7ad-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7c7ad-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c7ad-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c7ad-106">ByObjectParameterSet</span></span>
```
Disable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c7ad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c7ad-107">DESCRIPTION</span></span>
<span data-ttu-id="7c7ad-108">Командлет **Disable-AzureRmCdnCustomDomain** отключает защищенную доставку HTTPS для настраиваемого домена CDN.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-108">The **Disable-AzureRmCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="7c7ad-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c7ad-109">EXAMPLES</span></span>

### <span data-ttu-id="7c7ad-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7c7ad-110">Example 1</span></span>
```powershell
Disable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="7c7ad-111">Отключите доставку по протоколу HTTPS для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="7c7ad-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c7ad-112">PARAMETERS</span></span>

### <span data-ttu-id="7c7ad-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7c7ad-113">-CustomDomainName</span></span>
<span data-ttu-id="7c7ad-114">Отображаемое имя настраиваемого домена CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="7c7ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7ad-115">-DefaultProfile</span></span>
<span data-ttu-id="7c7ad-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c7ad-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7c7ad-117">-EndpointName</span></span>
<span data-ttu-id="7c7ad-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="7c7ad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c7ad-119">-InputObject</span></span>
<span data-ttu-id="7c7ad-120">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-120">The custom domain object.</span></span>

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

### <span data-ttu-id="7c7ad-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c7ad-121">-PassThru</span></span>
<span data-ttu-id="7c7ad-122">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="7c7ad-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="7c7ad-123">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="7c7ad-123">-ProfileName</span></span>
<span data-ttu-id="7c7ad-124">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="7c7ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c7ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="7c7ad-126">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="7c7ad-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c7ad-127">-Confirm</span></span>
<span data-ttu-id="7c7ad-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c7ad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c7ad-129">-WhatIf</span></span>
<span data-ttu-id="7c7ad-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c7ad-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c7ad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7ad-132">CommonParameters</span></span>
<span data-ttu-id="7c7ad-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c7ad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7ad-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c7ad-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7ad-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c7ad-135">INPUTS</span></span>

### <span data-ttu-id="7c7ad-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7c7ad-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="7c7ad-137">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7c7ad-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7c7ad-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c7ad-138">OUTPUTS</span></span>

### <span data-ttu-id="7c7ad-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c7ad-139">System.Boolean</span></span>

## <span data-ttu-id="7c7ad-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c7ad-140">NOTES</span></span>

## <span data-ttu-id="7c7ad-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c7ad-141">RELATED LINKS</span></span>
