---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423100"
---
# <span data-ttu-id="8e592-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8e592-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="8e592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e592-102">SYNOPSIS</span></span>
<span data-ttu-id="8e592-103">обновляет кэш в службе управления Api.</span><span class="sxs-lookup"><span data-stu-id="8e592-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="8e592-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e592-104">SYNTAX</span></span>

### <span data-ttu-id="8e592-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e592-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e592-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8e592-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e592-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e592-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e592-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e592-108">DESCRIPTION</span></span>
<span data-ttu-id="8e592-109">Cmdlet **Update-AzApiManagementCache** обновляет кэш в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8e592-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="8e592-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e592-110">EXAMPLES</span></span>

### <span data-ttu-id="8e592-111">Пример 1. Обновляет описание кэша в центрелуса.</span><span class="sxs-lookup"><span data-stu-id="8e592-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
```powershell
PS D:\github\azure-powershell> $context=New-AzApiManagementContext -ResourceGroupName Api-Default-Central-US -ServiceName contoso
PS D:\github\azure-powershell> Update-AzApiManagementCache -Context $context -CacheId centralus -Description "Team new cache" -PassThru


CacheId              : centralus
Description          : Team new cache
ConnectionString     : {{5cc19889e6ed3b0524c3f7d3}}
AzureRedisResourceId :
Id                   : /subscriptions/subid/resourceGroups/Api-Default-Central-US/providers/M
                       icrosoft.ApiManagement/service/contoso/caches/centralus
ResourceGroupName    : Api-Default-Central-US
ServiceName          : contoso
```

<span data-ttu-id="8e592-112">Обновляет описание кэша в Центре США.</span><span class="sxs-lookup"><span data-stu-id="8e592-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="8e592-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e592-113">PARAMETERS</span></span>

### <span data-ttu-id="8e592-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="8e592-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="8e592-115">Arm ResourceId экземпляра Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="8e592-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="8e592-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8e592-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e592-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="8e592-117">-CacheId</span></span>
<span data-ttu-id="8e592-118">Идентификатор нового кэша.</span><span class="sxs-lookup"><span data-stu-id="8e592-118">Identifier of new cache.</span></span>
<span data-ttu-id="8e592-119">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="8e592-119">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e592-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="8e592-120">-ConnectionString</span></span>
<span data-ttu-id="8e592-121">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="8e592-121">Redis Connection String.</span></span>
<span data-ttu-id="8e592-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8e592-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e592-123">-Контекст</span><span class="sxs-lookup"><span data-stu-id="8e592-123">-Context</span></span>
<span data-ttu-id="8e592-124">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8e592-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8e592-125">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="8e592-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e592-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e592-126">-DefaultProfile</span></span>
<span data-ttu-id="8e592-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e592-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e592-128">-Description</span><span class="sxs-lookup"><span data-stu-id="8e592-128">-Description</span></span>
<span data-ttu-id="8e592-129">Описание кэша.</span><span class="sxs-lookup"><span data-stu-id="8e592-129">Cache Description.</span></span>
<span data-ttu-id="8e592-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8e592-130">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e592-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e592-131">-InputObject</span></span>
<span data-ttu-id="8e592-132">Экземпляр PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="8e592-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="8e592-133">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="8e592-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e592-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e592-134">-PassThru</span></span>
<span data-ttu-id="8e592-135">Если задан этот экземпляр, экземпляр Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache, представляющий измененный кэш, будет записан для вывода.</span><span class="sxs-lookup"><span data-stu-id="8e592-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e592-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e592-136">-ResourceId</span></span>
<span data-ttu-id="8e592-137">Arm ResourceId кэша.</span><span class="sxs-lookup"><span data-stu-id="8e592-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="8e592-138">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="8e592-138">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e592-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e592-139">-Confirm</span></span>
<span data-ttu-id="8e592-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e592-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e592-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e592-141">-WhatIf</span></span>
<span data-ttu-id="8e592-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e592-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e592-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8e592-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e592-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e592-144">CommonParameters</span></span>
<span data-ttu-id="8e592-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e592-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e592-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e592-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e592-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e592-147">INPUTS</span></span>

### <span data-ttu-id="8e592-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8e592-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8e592-149">System.String</span><span class="sxs-lookup"><span data-stu-id="8e592-149">System.String</span></span>

### <span data-ttu-id="8e592-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8e592-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="8e592-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8e592-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8e592-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e592-152">OUTPUTS</span></span>

### <span data-ttu-id="8e592-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8e592-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="8e592-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e592-154">NOTES</span></span>

## <span data-ttu-id="8e592-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e592-155">RELATED LINKS</span></span>

[<span data-ttu-id="8e592-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8e592-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="8e592-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8e592-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="8e592-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8e592-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
