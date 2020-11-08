---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 833351c3abbf95eb898405f23241a20fe9affefa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079240"
---
# <span data-ttu-id="87184-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="87184-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="87184-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87184-102">SYNOPSIS</span></span>
<span data-ttu-id="87184-103">Создание новой редакции существующего API.</span><span class="sxs-lookup"><span data-stu-id="87184-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="87184-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87184-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87184-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87184-105">DESCRIPTION</span></span>

<span data-ttu-id="87184-106">Командлет **New-AzApiManagementApiRevision** создает редакцию API для существующего API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="87184-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="87184-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87184-107">EXAMPLES</span></span>

### <span data-ttu-id="87184-108">Пример 1: создание пустой редакции API для API</span><span class="sxs-lookup"><span data-stu-id="87184-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="87184-109">Эта команда создает версию API `2` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="87184-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="87184-110">Пример 2: создание редакции API из существующего API и копирование всех операций, тегов и политик</span><span class="sxs-lookup"><span data-stu-id="87184-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="87184-111">Эта команда создает версию API `5` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="87184-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="87184-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87184-112">PARAMETERS</span></span>

### <span data-ttu-id="87184-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="87184-113">-ApiId</span></span>
<span data-ttu-id="87184-114">Идентификатор API, для которого необходимо создать редакцию.</span><span class="sxs-lookup"><span data-stu-id="87184-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="87184-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="87184-115">-ApiRevision</span></span>
<span data-ttu-id="87184-116">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="87184-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="87184-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="87184-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="87184-118">Описание редакции API.</span><span class="sxs-lookup"><span data-stu-id="87184-118">Api Revision Description.</span></span> <span data-ttu-id="87184-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="87184-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="87184-120">-Context</span><span class="sxs-lookup"><span data-stu-id="87184-120">-Context</span></span>
<span data-ttu-id="87184-121">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="87184-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="87184-122">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="87184-122">This parameter is required.</span></span>

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

### <span data-ttu-id="87184-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87184-123">-DefaultProfile</span></span>
<span data-ttu-id="87184-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87184-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87184-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="87184-125">-ServiceUrl</span></span>
<span data-ttu-id="87184-126">URL веб-службы, предоставляющей API в серверной службе.</span><span class="sxs-lookup"><span data-stu-id="87184-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="87184-127">Этот URL-адрес будет использоваться только для управления API Azure и не будет открыт.</span><span class="sxs-lookup"><span data-stu-id="87184-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="87184-128">Должно содержать от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="87184-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="87184-129">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="87184-129">This parameter is required.</span></span>

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

### <span data-ttu-id="87184-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="87184-130">-SourceApiRevision</span></span>
<span data-ttu-id="87184-131">Идентификатор редакции API исходного API.</span><span class="sxs-lookup"><span data-stu-id="87184-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="87184-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="87184-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="87184-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87184-133">-Confirm</span></span>
<span data-ttu-id="87184-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87184-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87184-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87184-135">-WhatIf</span></span>
<span data-ttu-id="87184-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87184-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87184-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87184-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87184-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87184-138">CommonParameters</span></span>
<span data-ttu-id="87184-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87184-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87184-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87184-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87184-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87184-141">INPUTS</span></span>

### <span data-ttu-id="87184-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="87184-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87184-143">System. String</span><span class="sxs-lookup"><span data-stu-id="87184-143">System.String</span></span>

## <span data-ttu-id="87184-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87184-144">OUTPUTS</span></span>

### <span data-ttu-id="87184-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="87184-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="87184-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="87184-146">NOTES</span></span>

## <span data-ttu-id="87184-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87184-147">RELATED LINKS</span></span>

[<span data-ttu-id="87184-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="87184-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="87184-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="87184-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="87184-150">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="87184-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
