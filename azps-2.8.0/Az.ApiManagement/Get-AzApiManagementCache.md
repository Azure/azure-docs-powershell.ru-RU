---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: 7f1913b5debcbe3ebd5ae436c3c30529b1fdc9d5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404740"
---
# <span data-ttu-id="f80e1-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="f80e1-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="f80e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f80e1-102">SYNOPSIS</span></span>
<span data-ttu-id="f80e1-103">Получите сведения о кэше.</span><span class="sxs-lookup"><span data-stu-id="f80e1-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="f80e1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f80e1-104">SYNTAX</span></span>

### <span data-ttu-id="f80e1-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f80e1-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f80e1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f80e1-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f80e1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f80e1-107">DESCRIPTION</span></span>
<span data-ttu-id="f80e1-108">Получите сведения о кэше, настроенной в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="f80e1-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="f80e1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f80e1-109">EXAMPLES</span></span>

### <span data-ttu-id="f80e1-110">Пример 1. Получить все кэши</span><span class="sxs-lookup"><span data-stu-id="f80e1-110">Example 1: Get all Caches</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-West-US
ServiceName       : contoso
```

<span data-ttu-id="f80e1-111">Список всех кэшей, настроенных в службе управления Api.</span><span class="sxs-lookup"><span data-stu-id="f80e1-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="f80e1-112">Пример 2. Получить кэш, заданный идентификатором Westus</span><span class="sxs-lookup"><span data-stu-id="f80e1-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext -cacheId westus
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="f80e1-113">Получить сведения об указанном кэше, настроенного для westus</span><span class="sxs-lookup"><span data-stu-id="f80e1-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="f80e1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f80e1-114">PARAMETERS</span></span>

### <span data-ttu-id="f80e1-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="f80e1-115">-CacheId</span></span>
<span data-ttu-id="f80e1-116">Идентификатор кэша.</span><span class="sxs-lookup"><span data-stu-id="f80e1-116">Identifier of a cache.</span></span>
<span data-ttu-id="f80e1-117">Если он указан, будет пытаться найти кэш по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="f80e1-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="f80e1-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f80e1-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f80e1-119">-Контекст</span><span class="sxs-lookup"><span data-stu-id="f80e1-119">-Context</span></span>
<span data-ttu-id="f80e1-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f80e1-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f80e1-121">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="f80e1-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f80e1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f80e1-122">-DefaultProfile</span></span>
<span data-ttu-id="f80e1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f80e1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f80e1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f80e1-124">-ResourceId</span></span>
<span data-ttu-id="f80e1-125">Идентификатор ресурса Arm кэша.</span><span class="sxs-lookup"><span data-stu-id="f80e1-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="f80e1-126">Если он указан, будет пытаться найти кэш по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="f80e1-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="f80e1-127">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="f80e1-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f80e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f80e1-128">CommonParameters</span></span>
<span data-ttu-id="f80e1-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f80e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f80e1-130">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f80e1-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f80e1-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f80e1-131">INPUTS</span></span>

### <span data-ttu-id="f80e1-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f80e1-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f80e1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f80e1-133">System.String</span></span>

## <span data-ttu-id="f80e1-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f80e1-134">OUTPUTS</span></span>

### <span data-ttu-id="f80e1-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="f80e1-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="f80e1-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f80e1-136">NOTES</span></span>

## <span data-ttu-id="f80e1-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f80e1-137">RELATED LINKS</span></span>

[<span data-ttu-id="f80e1-138">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="f80e1-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="f80e1-139">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="f80e1-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="f80e1-140">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="f80e1-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
