---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243742"
---
# <span data-ttu-id="67965-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="67965-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="67965-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67965-102">SYNOPSIS</span></span>
<span data-ttu-id="67965-103">Обновляет кэш в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="67965-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="67965-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67965-104">SYNTAX</span></span>

### <span data-ttu-id="67965-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67965-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67965-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67965-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67965-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67965-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67965-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67965-108">DESCRIPTION</span></span>
<span data-ttu-id="67965-109">Командлет **Update-AzApiManagementCache** обновляет кэш в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="67965-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="67965-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67965-110">EXAMPLES</span></span>

### <span data-ttu-id="67965-111">Пример 1: Обновление описания кэша в centralus</span><span class="sxs-lookup"><span data-stu-id="67965-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="67965-112">Обновляет описание кэша в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="67965-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="67965-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67965-113">PARAMETERS</span></span>

### <span data-ttu-id="67965-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="67965-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="67965-115">ResourceId (ИД) для экземпляра Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="67965-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="67965-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="67965-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="67965-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="67965-117">-CacheId</span></span>
<span data-ttu-id="67965-118">Идентификатор нового кэша.</span><span class="sxs-lookup"><span data-stu-id="67965-118">Identifier of new cache.</span></span>
<span data-ttu-id="67965-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="67965-119">This parameter is required.</span></span>

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

### <span data-ttu-id="67965-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="67965-120">-ConnectionString</span></span>
<span data-ttu-id="67965-121">Строка подключения Redis.</span><span class="sxs-lookup"><span data-stu-id="67965-121">Redis Connection String.</span></span>
<span data-ttu-id="67965-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="67965-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="67965-123">-Context</span><span class="sxs-lookup"><span data-stu-id="67965-123">-Context</span></span>
<span data-ttu-id="67965-124">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="67965-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="67965-125">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="67965-125">This parameter is required.</span></span>

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

### <span data-ttu-id="67965-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67965-126">-DefaultProfile</span></span>
<span data-ttu-id="67965-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67965-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67965-128">-Описание</span><span class="sxs-lookup"><span data-stu-id="67965-128">-Description</span></span>
<span data-ttu-id="67965-129">Описание кэша.</span><span class="sxs-lookup"><span data-stu-id="67965-129">Cache Description.</span></span>
<span data-ttu-id="67965-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="67965-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="67965-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67965-131">-InputObject</span></span>
<span data-ttu-id="67965-132">Экземпляр PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="67965-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="67965-133">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="67965-133">This parameter is required.</span></span>

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

### <span data-ttu-id="67965-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67965-134">-PassThru</span></span>
<span data-ttu-id="67965-135">Если указан, то экземпляр типа Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache, который представляет измененный кэш, будет записываться в Output.</span><span class="sxs-lookup"><span data-stu-id="67965-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="67965-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67965-136">-ResourceId</span></span>
<span data-ttu-id="67965-137">ИД ресурса ARM для кэша.</span><span class="sxs-lookup"><span data-stu-id="67965-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="67965-138">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="67965-138">This parameter is required.</span></span>

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

### <span data-ttu-id="67965-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67965-139">-Confirm</span></span>
<span data-ttu-id="67965-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67965-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67965-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67965-141">-WhatIf</span></span>
<span data-ttu-id="67965-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67965-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67965-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67965-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67965-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67965-144">CommonParameters</span></span>
<span data-ttu-id="67965-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67965-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67965-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67965-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67965-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67965-147">INPUTS</span></span>

### <span data-ttu-id="67965-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="67965-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="67965-149">System. String</span><span class="sxs-lookup"><span data-stu-id="67965-149">System.String</span></span>

### <span data-ttu-id="67965-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="67965-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="67965-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="67965-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="67965-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67965-152">OUTPUTS</span></span>

### <span data-ttu-id="67965-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="67965-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="67965-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="67965-154">NOTES</span></span>

## <span data-ttu-id="67965-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67965-155">RELATED LINKS</span></span>

[<span data-ttu-id="67965-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="67965-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="67965-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="67965-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="67965-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="67965-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
