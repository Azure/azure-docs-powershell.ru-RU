---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080125"
---
# <span data-ttu-id="c10f8-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c10f8-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="c10f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c10f8-102">SYNOPSIS</span></span>
<span data-ttu-id="c10f8-103">Получает сервер авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="c10f8-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="c10f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c10f8-104">SYNTAX</span></span>

### <span data-ttu-id="c10f8-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c10f8-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c10f8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c10f8-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c10f8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c10f8-107">DESCRIPTION</span></span>
<span data-ttu-id="c10f8-108">Командлет **Get-AzApiManagementAuthorizationServer** получает доступ ко всем серверам авторизации управления API Azure или указанному серверу авторизации.</span><span class="sxs-lookup"><span data-stu-id="c10f8-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="c10f8-109">ClientSecret не будет включаться в данные результата.</span><span class="sxs-lookup"><span data-stu-id="c10f8-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="c10f8-110">Чтобы получить секрет клиента, используйте **Get-AzApiManagementAuthorizationServerClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="c10f8-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="c10f8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c10f8-111">EXAMPLES</span></span>

### <span data-ttu-id="c10f8-112">Пример 1: получение всех серверов авторизации</span><span class="sxs-lookup"><span data-stu-id="c10f8-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="c10f8-113">Эта команда получает все серверы авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="c10f8-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="c10f8-114">Пример 2: получение указанного сервера авторизации</span><span class="sxs-lookup"><span data-stu-id="c10f8-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="c10f8-115">Эта команда получает указанный сервер авторизации.</span><span class="sxs-lookup"><span data-stu-id="c10f8-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="c10f8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c10f8-116">PARAMETERS</span></span>

### <span data-ttu-id="c10f8-117">-Context</span><span class="sxs-lookup"><span data-stu-id="c10f8-117">-Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c10f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c10f8-118">-DefaultProfile</span></span>
<span data-ttu-id="c10f8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c10f8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c10f8-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c10f8-120">-ResourceId</span></span>
<span data-ttu-id="c10f8-121">Идентификатор ресурса ARM сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="c10f8-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="c10f8-122">Если задано значение, это попытается найти сервер авторизации по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="c10f8-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="c10f8-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c10f8-123">This parameter is required.</span></span>

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

### <span data-ttu-id="c10f8-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="c10f8-124">-ServerId</span></span>
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

### <span data-ttu-id="c10f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c10f8-125">CommonParameters</span></span>
<span data-ttu-id="c10f8-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c10f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c10f8-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c10f8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c10f8-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c10f8-128">INPUTS</span></span>

### <span data-ttu-id="c10f8-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c10f8-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c10f8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c10f8-130">System.String</span></span>

## <span data-ttu-id="c10f8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c10f8-131">OUTPUTS</span></span>

### <span data-ttu-id="c10f8-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c10f8-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="c10f8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c10f8-133">NOTES</span></span>

## <span data-ttu-id="c10f8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c10f8-134">RELATED LINKS</span></span>

[<span data-ttu-id="c10f8-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c10f8-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="c10f8-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c10f8-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="c10f8-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="c10f8-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)

