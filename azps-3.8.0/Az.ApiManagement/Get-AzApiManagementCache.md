---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: 757332267d2db2f797bb2f7ca2a39dbb32ee06c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066412"
---
# <span data-ttu-id="a2efe-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a2efe-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="a2efe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2efe-102">SYNOPSIS</span></span>
<span data-ttu-id="a2efe-103">Получение сведений о кэше.</span><span class="sxs-lookup"><span data-stu-id="a2efe-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="a2efe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2efe-104">SYNTAX</span></span>

### <span data-ttu-id="a2efe-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2efe-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2efe-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2efe-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2efe-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2efe-107">DESCRIPTION</span></span>
<span data-ttu-id="a2efe-108">Получение подробностей кэша, настроенного в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="a2efe-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="a2efe-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2efe-109">EXAMPLES</span></span>

### <span data-ttu-id="a2efe-110">Пример 1: получение всех кэшей</span><span class="sxs-lookup"><span data-stu-id="a2efe-110">Example 1: Get all Caches</span></span>
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

<span data-ttu-id="a2efe-111">Получает список всех кэшей, настроенных в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="a2efe-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="a2efe-112">Пример 2: получение кэша, указанного идентификатором westus</span><span class="sxs-lookup"><span data-stu-id="a2efe-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
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

<span data-ttu-id="a2efe-113">Получение сведений об указанном кэше, настроенном для westus</span><span class="sxs-lookup"><span data-stu-id="a2efe-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="a2efe-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2efe-114">PARAMETERS</span></span>

### <span data-ttu-id="a2efe-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="a2efe-115">-CacheId</span></span>
<span data-ttu-id="a2efe-116">Идентификатор кэша.</span><span class="sxs-lookup"><span data-stu-id="a2efe-116">Identifier of a cache.</span></span>
<span data-ttu-id="a2efe-117">Если задано значение, оно попытается найти кэш по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="a2efe-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="a2efe-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a2efe-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="a2efe-119">-Context</span><span class="sxs-lookup"><span data-stu-id="a2efe-119">-Context</span></span>
<span data-ttu-id="a2efe-120">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a2efe-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a2efe-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a2efe-121">This parameter is required.</span></span>

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

### <span data-ttu-id="a2efe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2efe-122">-DefaultProfile</span></span>
<span data-ttu-id="a2efe-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2efe-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2efe-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2efe-124">-ResourceId</span></span>
<span data-ttu-id="a2efe-125">Идентификатор ресурса ARM для кэша.</span><span class="sxs-lookup"><span data-stu-id="a2efe-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="a2efe-126">Если задано значение, оно попытается найти кэш по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="a2efe-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="a2efe-127">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a2efe-127">This parameter is required.</span></span>

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

### <span data-ttu-id="a2efe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2efe-128">CommonParameters</span></span>
<span data-ttu-id="a2efe-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2efe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2efe-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2efe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2efe-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2efe-131">INPUTS</span></span>

### <span data-ttu-id="a2efe-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a2efe-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a2efe-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a2efe-133">System.String</span></span>

## <span data-ttu-id="a2efe-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2efe-134">OUTPUTS</span></span>

### <span data-ttu-id="a2efe-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a2efe-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="a2efe-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2efe-136">NOTES</span></span>

## <span data-ttu-id="a2efe-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2efe-137">RELATED LINKS</span></span>

[<span data-ttu-id="a2efe-138">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a2efe-138">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="a2efe-139">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a2efe-139">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="a2efe-140">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a2efe-140">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)