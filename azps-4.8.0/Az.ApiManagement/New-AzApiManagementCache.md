---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078005"
---
# <span data-ttu-id="6a523-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="6a523-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="6a523-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a523-102">SYNOPSIS</span></span>
<span data-ttu-id="6a523-103">Создание новой сущности кэша</span><span class="sxs-lookup"><span data-stu-id="6a523-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="6a523-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a523-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a523-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a523-105">DESCRIPTION</span></span>
<span data-ttu-id="6a523-106">Командлет **New-AzApiManagementCache** создает новую сущность кэша в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="6a523-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="6a523-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a523-107">EXAMPLES</span></span>

### <span data-ttu-id="6a523-108">Пример 1: создание новой сущности кэша</span><span class="sxs-lookup"><span data-stu-id="6a523-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="6a523-109">Командлеты создают новую сущность кэша в главном расположении службы управления API.</span><span class="sxs-lookup"><span data-stu-id="6a523-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="6a523-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a523-110">PARAMETERS</span></span>

### <span data-ttu-id="6a523-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="6a523-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="6a523-112">ResourceId (ИД) для экземпляра Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="6a523-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="6a523-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6a523-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="6a523-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="6a523-114">-CacheId</span></span>
<span data-ttu-id="6a523-115">Идентификатор нового кэша.</span><span class="sxs-lookup"><span data-stu-id="6a523-115">Identifier of new cache.</span></span>
<span data-ttu-id="6a523-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6a523-116">This parameter is optional.</span></span>
<span data-ttu-id="6a523-117">Если не указано, будет создано.</span><span class="sxs-lookup"><span data-stu-id="6a523-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="6a523-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="6a523-118">-ConnectionString</span></span>
<span data-ttu-id="6a523-119">Строка подключения Redis.</span><span class="sxs-lookup"><span data-stu-id="6a523-119">Redis Connection String.</span></span>
<span data-ttu-id="6a523-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6a523-120">This parameter is required.</span></span>

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

### <span data-ttu-id="6a523-121">-Context</span><span class="sxs-lookup"><span data-stu-id="6a523-121">-Context</span></span>
<span data-ttu-id="6a523-122">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6a523-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6a523-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6a523-123">This parameter is required.</span></span>

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

### <span data-ttu-id="6a523-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a523-124">-DefaultProfile</span></span>
<span data-ttu-id="6a523-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a523-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a523-126">-Описание</span><span class="sxs-lookup"><span data-stu-id="6a523-126">-Description</span></span>
<span data-ttu-id="6a523-127">Описание кэша.</span><span class="sxs-lookup"><span data-stu-id="6a523-127">Cache Description.</span></span>
<span data-ttu-id="6a523-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6a523-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="6a523-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a523-129">-Confirm</span></span>
<span data-ttu-id="6a523-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6a523-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a523-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a523-131">-WhatIf</span></span>
<span data-ttu-id="6a523-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6a523-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a523-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6a523-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a523-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a523-134">CommonParameters</span></span>
<span data-ttu-id="6a523-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a523-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a523-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a523-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a523-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a523-137">INPUTS</span></span>

### <span data-ttu-id="6a523-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6a523-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6a523-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6a523-139">System.String</span></span>

## <span data-ttu-id="6a523-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a523-140">OUTPUTS</span></span>

### <span data-ttu-id="6a523-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="6a523-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="6a523-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a523-142">NOTES</span></span>

## <span data-ttu-id="6a523-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a523-143">RELATED LINKS</span></span>

[<span data-ttu-id="6a523-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="6a523-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="6a523-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="6a523-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="6a523-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="6a523-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
