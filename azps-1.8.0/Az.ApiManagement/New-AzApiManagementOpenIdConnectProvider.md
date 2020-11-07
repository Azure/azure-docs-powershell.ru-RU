---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 3b4cec203e39401885874db5391f62a9f1663342
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901737"
---
# <span data-ttu-id="6661b-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6661b-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="6661b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6661b-102">SYNOPSIS</span></span>
<span data-ttu-id="6661b-103">Создает поставщик подключений OpenID.</span><span class="sxs-lookup"><span data-stu-id="6661b-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="6661b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6661b-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6661b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6661b-105">DESCRIPTION</span></span>
<span data-ttu-id="6661b-106">Командлет **New-AzApiManagementOpenIdConnectProvider** создает поставщик OpenID Connect в управлении API Azure.</span><span class="sxs-lookup"><span data-stu-id="6661b-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="6661b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6661b-107">EXAMPLES</span></span>

### <span data-ttu-id="6661b-108">Пример 1: создание поставщика</span><span class="sxs-lookup"><span data-stu-id="6661b-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="6661b-109">Эта команда создает **поставщик** подключений OpenID, именуемый поставщиком Contoso OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="6661b-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="6661b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6661b-110">PARAMETERS</span></span>

### <span data-ttu-id="6661b-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="6661b-111">-ClientId</span></span>
<span data-ttu-id="6661b-112">Указывает идентификатор клиента консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="6661b-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="6661b-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="6661b-113">-ClientSecret</span></span>
<span data-ttu-id="6661b-114">Указывает секрет клиента для консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="6661b-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="6661b-115">-Context</span><span class="sxs-lookup"><span data-stu-id="6661b-115">-Context</span></span>
<span data-ttu-id="6661b-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6661b-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6661b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6661b-117">-DefaultProfile</span></span>
<span data-ttu-id="6661b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6661b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6661b-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="6661b-119">-Description</span></span>
<span data-ttu-id="6661b-120">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="6661b-120">Specifies a description.</span></span>

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

### <span data-ttu-id="6661b-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="6661b-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="6661b-122">Указывает URI конечной точки метаданных поставщика.</span><span class="sxs-lookup"><span data-stu-id="6661b-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="6661b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6661b-123">-Name</span></span>
<span data-ttu-id="6661b-124">Задает понятное имя для поставщика.</span><span class="sxs-lookup"><span data-stu-id="6661b-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="6661b-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="6661b-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="6661b-126">Указывает идентификатор поставщика.</span><span class="sxs-lookup"><span data-stu-id="6661b-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="6661b-127">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="6661b-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="6661b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6661b-128">CommonParameters</span></span>
<span data-ttu-id="6661b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6661b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6661b-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6661b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6661b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6661b-131">INPUTS</span></span>

### <span data-ttu-id="6661b-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6661b-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6661b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6661b-133">System.String</span></span>

## <span data-ttu-id="6661b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6661b-134">OUTPUTS</span></span>

### <span data-ttu-id="6661b-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6661b-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="6661b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="6661b-136">NOTES</span></span>

## <span data-ttu-id="6661b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6661b-137">RELATED LINKS</span></span>

[<span data-ttu-id="6661b-138">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6661b-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="6661b-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6661b-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="6661b-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6661b-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


