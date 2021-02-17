---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: d4095c1a20c4cebc3fb5f9b58f6f696c9cf41dc7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399419"
---
# <span data-ttu-id="53c5b-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="53c5b-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="53c5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53c5b-102">SYNOPSIS</span></span>
<span data-ttu-id="53c5b-103">Создание новой сущности кэша</span><span class="sxs-lookup"><span data-stu-id="53c5b-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="53c5b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53c5b-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53c5b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53c5b-105">DESCRIPTION</span></span>
<span data-ttu-id="53c5b-106">Для выполнения cmdlet **New-AzApiManagementCache** создается новая сущность кэша в службе управления Api.</span><span class="sxs-lookup"><span data-stu-id="53c5b-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="53c5b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53c5b-107">EXAMPLES</span></span>

### <span data-ttu-id="53c5b-108">Пример 1. Создание новой сущности кэша</span><span class="sxs-lookup"><span data-stu-id="53c5b-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="53c5b-109">С их мастерами создается новый объект кэша в расположении, которое является главный расположением службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="53c5b-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="53c5b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53c5b-110">PARAMETERS</span></span>

### <span data-ttu-id="53c5b-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="53c5b-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="53c5b-112">Arm ResourceId экземпляра Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="53c5b-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="53c5b-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="53c5b-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="53c5b-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="53c5b-114">-CacheId</span></span>
<span data-ttu-id="53c5b-115">Идентификатор нового кэша.</span><span class="sxs-lookup"><span data-stu-id="53c5b-115">Identifier of new cache.</span></span>
<span data-ttu-id="53c5b-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="53c5b-116">This parameter is optional.</span></span>
<span data-ttu-id="53c5b-117">Если он не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="53c5b-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="53c5b-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="53c5b-118">-ConnectionString</span></span>
<span data-ttu-id="53c5b-119">Redis Connection String.</span><span class="sxs-lookup"><span data-stu-id="53c5b-119">Redis Connection String.</span></span>
<span data-ttu-id="53c5b-120">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="53c5b-120">This parameter is required.</span></span>

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

### <span data-ttu-id="53c5b-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="53c5b-121">-Context</span></span>
<span data-ttu-id="53c5b-122">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="53c5b-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="53c5b-123">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="53c5b-123">This parameter is required.</span></span>

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

### <span data-ttu-id="53c5b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c5b-124">-DefaultProfile</span></span>
<span data-ttu-id="53c5b-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53c5b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53c5b-126">-Description</span><span class="sxs-lookup"><span data-stu-id="53c5b-126">-Description</span></span>
<span data-ttu-id="53c5b-127">Описание кэша.</span><span class="sxs-lookup"><span data-stu-id="53c5b-127">Cache Description.</span></span>
<span data-ttu-id="53c5b-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="53c5b-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="53c5b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53c5b-129">-Confirm</span></span>
<span data-ttu-id="53c5b-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="53c5b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c5b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c5b-131">-WhatIf</span></span>
<span data-ttu-id="53c5b-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53c5b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c5b-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="53c5b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c5b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c5b-134">CommonParameters</span></span>
<span data-ttu-id="53c5b-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c5b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c5b-136">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53c5b-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c5b-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53c5b-137">INPUTS</span></span>

### <span data-ttu-id="53c5b-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="53c5b-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="53c5b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="53c5b-139">System.String</span></span>

## <span data-ttu-id="53c5b-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53c5b-140">OUTPUTS</span></span>

### <span data-ttu-id="53c5b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="53c5b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="53c5b-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53c5b-142">NOTES</span></span>

## <span data-ttu-id="53c5b-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53c5b-143">RELATED LINKS</span></span>

[<span data-ttu-id="53c5b-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="53c5b-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="53c5b-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="53c5b-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="53c5b-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="53c5b-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
