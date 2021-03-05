---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: 13fe16c2612a267df0760aad939b46e427d6fab1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960904"
---
# <span data-ttu-id="17e91-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="17e91-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="17e91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17e91-102">SYNOPSIS</span></span>
<span data-ttu-id="17e91-103">Создание новой сущности кэша</span><span class="sxs-lookup"><span data-stu-id="17e91-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="17e91-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="17e91-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17e91-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17e91-105">DESCRIPTION</span></span>
<span data-ttu-id="17e91-106">Для выполнения cmdlet **New-AzApiManagementCache** создается новая сущность кэша в службе управления Api.</span><span class="sxs-lookup"><span data-stu-id="17e91-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="17e91-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="17e91-107">EXAMPLES</span></span>

### <span data-ttu-id="17e91-108">Пример 1. Создание новой сущности кэша</span><span class="sxs-lookup"><span data-stu-id="17e91-108">Example 1 : Create a new Cache entity</span></span>
```powershell
PS c:\> New-AzApiManagementCache -Context $context -ConnectionString "teamdemo.redis.cache.windows.net:6380,password=xxxxxx+xxxxx=,ssl=True,abortConnect=False" -Description "Team Cache"

CacheId           : centralus
Description       : Team Cache
ConnectionString  : {{5cc19889e6ed3b0524c3f7d3}}
ResourceId        :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsof
                    t.ApiManagement/service/contoso/caches/centralus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="17e91-109">С их мастерами создается новый объект кэша в расположении, которое является главный расположением службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="17e91-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="17e91-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17e91-110">PARAMETERS</span></span>

### <span data-ttu-id="17e91-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="17e91-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="17e91-112">Arm ResourceId экземпляра Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="17e91-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="17e91-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="17e91-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="17e91-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="17e91-114">-CacheId</span></span>
<span data-ttu-id="17e91-115">Идентификатор нового кэша.</span><span class="sxs-lookup"><span data-stu-id="17e91-115">Identifier of new cache.</span></span>
<span data-ttu-id="17e91-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="17e91-116">This parameter is optional.</span></span>
<span data-ttu-id="17e91-117">Если он не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="17e91-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="17e91-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="17e91-118">-ConnectionString</span></span>
<span data-ttu-id="17e91-119">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="17e91-119">Redis Connection String.</span></span>
<span data-ttu-id="17e91-120">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="17e91-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17e91-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="17e91-121">-Context</span></span>
<span data-ttu-id="17e91-122">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="17e91-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="17e91-123">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="17e91-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17e91-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e91-124">-DefaultProfile</span></span>
<span data-ttu-id="17e91-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17e91-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17e91-126">-Description</span><span class="sxs-lookup"><span data-stu-id="17e91-126">-Description</span></span>
<span data-ttu-id="17e91-127">Описание кэша.</span><span class="sxs-lookup"><span data-stu-id="17e91-127">Cache Description.</span></span>
<span data-ttu-id="17e91-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="17e91-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="17e91-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17e91-129">-Confirm</span></span>
<span data-ttu-id="17e91-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="17e91-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17e91-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e91-131">-WhatIf</span></span>
<span data-ttu-id="17e91-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17e91-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17e91-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="17e91-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17e91-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e91-134">CommonParameters</span></span>
<span data-ttu-id="17e91-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17e91-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e91-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17e91-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e91-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17e91-137">INPUTS</span></span>

### <span data-ttu-id="17e91-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="17e91-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="17e91-139">System.String</span><span class="sxs-lookup"><span data-stu-id="17e91-139">System.String</span></span>

## <span data-ttu-id="17e91-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17e91-140">OUTPUTS</span></span>

### <span data-ttu-id="17e91-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="17e91-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="17e91-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="17e91-142">NOTES</span></span>

## <span data-ttu-id="17e91-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17e91-143">RELATED LINKS</span></span>

[<span data-ttu-id="17e91-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="17e91-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="17e91-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="17e91-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="17e91-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="17e91-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
