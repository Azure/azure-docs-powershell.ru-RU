---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 81a80acdfb89f30cc1add6b1cfc10bcd7d745dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720116"
---
# <span data-ttu-id="57860-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="57860-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="57860-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57860-102">SYNOPSIS</span></span>
<span data-ttu-id="57860-103">Создание новой редакции существующего API.</span><span class="sxs-lookup"><span data-stu-id="57860-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="57860-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57860-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57860-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57860-105">DESCRIPTION</span></span>

<span data-ttu-id="57860-106">Командлет **New-AzApiManagementApiRevision** создает редакцию API для существующего API в контексте управления API.</span><span class="sxs-lookup"><span data-stu-id="57860-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="57860-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57860-107">EXAMPLES</span></span>

### <span data-ttu-id="57860-108">Пример 1: создание редакции API для API</span><span class="sxs-lookup"><span data-stu-id="57860-108">Example 1: Create an API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $ApiMgmtContext  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6


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

<span data-ttu-id="57860-109">Эта команда создает версию API `2` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="57860-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

## <span data-ttu-id="57860-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57860-110">PARAMETERS</span></span>

### <span data-ttu-id="57860-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="57860-111">-ApiId</span></span>
<span data-ttu-id="57860-112">Идентификатор API, для которого необходимо создать редакцию.</span><span class="sxs-lookup"><span data-stu-id="57860-112">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="57860-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="57860-113">-ApiRevision</span></span>
<span data-ttu-id="57860-114">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="57860-114">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="57860-115">-Context</span><span class="sxs-lookup"><span data-stu-id="57860-115">-Context</span></span>
<span data-ttu-id="57860-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="57860-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="57860-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="57860-117">This parameter is required.</span></span>

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

### <span data-ttu-id="57860-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57860-118">-DefaultProfile</span></span>
<span data-ttu-id="57860-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57860-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57860-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57860-120">-Confirm</span></span>
<span data-ttu-id="57860-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="57860-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57860-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57860-122">-WhatIf</span></span>
<span data-ttu-id="57860-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="57860-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57860-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="57860-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57860-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57860-125">CommonParameters</span></span>
<span data-ttu-id="57860-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57860-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57860-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57860-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57860-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57860-128">INPUTS</span></span>

### <span data-ttu-id="57860-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="57860-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="57860-130">System. String</span><span class="sxs-lookup"><span data-stu-id="57860-130">System.String</span></span>

## <span data-ttu-id="57860-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57860-131">OUTPUTS</span></span>

### <span data-ttu-id="57860-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="57860-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="57860-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="57860-133">NOTES</span></span>

## <span data-ttu-id="57860-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57860-134">RELATED LINKS</span></span>

[<span data-ttu-id="57860-135">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="57860-135">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="57860-136">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="57860-136">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="57860-137">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="57860-137">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
