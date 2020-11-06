---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: 2ee3954569067000d445ecd7dab034db41734829
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561248"
---
# <span data-ttu-id="c9fd4-101">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c9fd4-101">New-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="c9fd4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="c9fd4-103">Создание новой редакции существующего API.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-103">Creates a new Revision of an Existing API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9fd4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9fd4-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9fd4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9fd4-105">DESCRIPTION</span></span>

<span data-ttu-id="c9fd4-106">Командлет **New-AzureRmApiManagementApiRevision** создает редакцию API для существующего API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-106">The **New-AzureRmApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="c9fd4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9fd4-107">EXAMPLES</span></span>

### <span data-ttu-id="c9fd4-108">Пример 1: создание редакции API для API</span><span class="sxs-lookup"><span data-stu-id="c9fd4-108">Example 1: Create an API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApiRevision -Context $ApiMgmtContext  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6


ApiId                         : 5adf6fbf0faadf3ad8558065;rev=6
Name                          : httpbin.org
Description                   : API Management facade for a very handy and free online HTTP tool.
ServiceUrl                    : https://httpbin.org/
Path                          : httpbin
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         : contoso-oauth
AuthorizationScope            : contoso-oauth
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 6
ApiVersion                    : v1
IsCurrent                     : False
IsOnline                      : False
Id                            : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065;rev=6
ResourceGroupName             : Api-Default-WestUS
ServiceName                   : contoso
```

<span data-ttu-id="c9fd4-109">Эта команда создает версию API `2` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

## <span data-ttu-id="c9fd4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9fd4-110">PARAMETERS</span></span>

### <span data-ttu-id="c9fd4-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c9fd4-111">-ApiId</span></span>
<span data-ttu-id="c9fd4-112">Идентификатор API, для которого необходимо создать редакцию.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-112">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="c9fd4-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c9fd4-113">-ApiRevision</span></span>
<span data-ttu-id="c9fd4-114">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-114">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="c9fd4-115">-Context</span><span class="sxs-lookup"><span data-stu-id="c9fd4-115">-Context</span></span>
<span data-ttu-id="c9fd4-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c9fd4-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-117">This parameter is required.</span></span>

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

### <span data-ttu-id="c9fd4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9fd4-118">-DefaultProfile</span></span>
<span data-ttu-id="c9fd4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9fd4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9fd4-120">-Confirm</span></span>
<span data-ttu-id="c9fd4-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9fd4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9fd4-122">-WhatIf</span></span>
<span data-ttu-id="c9fd4-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9fd4-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9fd4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9fd4-125">CommonParameters</span></span>
<span data-ttu-id="c9fd4-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9fd4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9fd4-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9fd4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9fd4-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9fd4-128">INPUTS</span></span>

### <span data-ttu-id="c9fd4-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c9fd4-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="c9fd4-130">Параметры: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c9fd4-130">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="c9fd4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c9fd4-131">System.String</span></span>

## <span data-ttu-id="c9fd4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9fd4-132">OUTPUTS</span></span>

### <span data-ttu-id="c9fd4-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c9fd4-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="c9fd4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9fd4-134">NOTES</span></span>

## <span data-ttu-id="c9fd4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9fd4-135">RELATED LINKS</span></span>

[<span data-ttu-id="c9fd4-136">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c9fd4-136">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="c9fd4-137">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c9fd4-137">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="c9fd4-138">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c9fd4-138">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)
