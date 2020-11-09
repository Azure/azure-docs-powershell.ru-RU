---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317414"
---
# <span data-ttu-id="534b7-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="534b7-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="534b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="534b7-102">SYNOPSIS</span></span>
<span data-ttu-id="534b7-103">Получает сервер авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="534b7-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="534b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="534b7-104">SYNTAX</span></span>

### <span data-ttu-id="534b7-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="534b7-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="534b7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="534b7-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="534b7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="534b7-107">DESCRIPTION</span></span>
<span data-ttu-id="534b7-108">Командлет **Get-AzApiManagementAuthorizationServer** получает доступ ко всем серверам авторизации управления API Azure или указанному серверу авторизации.</span><span class="sxs-lookup"><span data-stu-id="534b7-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="534b7-109">ClientSecret не будет включаться в данные результата.</span><span class="sxs-lookup"><span data-stu-id="534b7-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="534b7-110">Чтобы получить секрет клиента, используйте **Get-AzApiManagementAuthorizationServerClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="534b7-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="534b7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="534b7-111">EXAMPLES</span></span>

### <span data-ttu-id="534b7-112">Пример 1: получение всех серверов авторизации</span><span class="sxs-lookup"><span data-stu-id="534b7-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="534b7-113">Эта команда получает все серверы авторизации управления API.</span><span class="sxs-lookup"><span data-stu-id="534b7-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="534b7-114">Пример 2: получение указанного сервера авторизации</span><span class="sxs-lookup"><span data-stu-id="534b7-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="534b7-115">Эта команда получает указанный сервер авторизации.</span><span class="sxs-lookup"><span data-stu-id="534b7-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="534b7-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="534b7-116">PARAMETERS</span></span>

### <span data-ttu-id="534b7-117">-Context</span><span class="sxs-lookup"><span data-stu-id="534b7-117">-Context</span></span>

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

### <span data-ttu-id="534b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534b7-118">-DefaultProfile</span></span>
<span data-ttu-id="534b7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="534b7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="534b7-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="534b7-120">-ResourceId</span></span>
<span data-ttu-id="534b7-121">Идентификатор ресурса ARM сервера авторизации.</span><span class="sxs-lookup"><span data-stu-id="534b7-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="534b7-122">Если задано значение, это попытается найти сервер авторизации по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="534b7-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="534b7-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="534b7-123">This parameter is required.</span></span>

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

### <span data-ttu-id="534b7-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="534b7-124">-ServerId</span></span>
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

### <span data-ttu-id="534b7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534b7-125">CommonParameters</span></span>
<span data-ttu-id="534b7-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="534b7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534b7-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="534b7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534b7-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="534b7-128">INPUTS</span></span>

### <span data-ttu-id="534b7-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="534b7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="534b7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="534b7-130">System.String</span></span>

## <span data-ttu-id="534b7-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="534b7-131">OUTPUTS</span></span>

### <span data-ttu-id="534b7-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="534b7-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="534b7-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="534b7-133">NOTES</span></span>

## <span data-ttu-id="534b7-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="534b7-134">RELATED LINKS</span></span>

[<span data-ttu-id="534b7-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="534b7-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="534b7-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="534b7-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="534b7-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="534b7-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


