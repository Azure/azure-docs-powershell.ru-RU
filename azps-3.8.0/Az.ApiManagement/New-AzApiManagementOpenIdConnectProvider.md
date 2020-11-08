---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 37144ab119eba4f19c3b34b2b32dfd28ff305677
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066693"
---
# <span data-ttu-id="b5efb-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b5efb-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b5efb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5efb-102">SYNOPSIS</span></span>
<span data-ttu-id="b5efb-103">Создает поставщик подключений OpenID.</span><span class="sxs-lookup"><span data-stu-id="b5efb-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="b5efb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5efb-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5efb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5efb-105">DESCRIPTION</span></span>
<span data-ttu-id="b5efb-106">Командлет **New-AzApiManagementOpenIdConnectProvider** создает поставщик OpenID Connect в управлении API Azure.</span><span class="sxs-lookup"><span data-stu-id="b5efb-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="b5efb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5efb-107">EXAMPLES</span></span>

### <span data-ttu-id="b5efb-108">Пример 1: создание поставщика</span><span class="sxs-lookup"><span data-stu-id="b5efb-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="b5efb-109">Эта команда создает **поставщик** подключений OpenID, именуемый поставщиком Contoso OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="b5efb-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="b5efb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5efb-110">PARAMETERS</span></span>

### <span data-ttu-id="b5efb-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="b5efb-111">-ClientId</span></span>
<span data-ttu-id="b5efb-112">Указывает идентификатор клиента консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="b5efb-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="b5efb-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="b5efb-113">-ClientSecret</span></span>
<span data-ttu-id="b5efb-114">Указывает секрет клиента для консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="b5efb-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="b5efb-115">-Context</span><span class="sxs-lookup"><span data-stu-id="b5efb-115">-Context</span></span>
<span data-ttu-id="b5efb-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b5efb-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5efb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5efb-117">-DefaultProfile</span></span>
<span data-ttu-id="b5efb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5efb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5efb-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="b5efb-119">-Description</span></span>
<span data-ttu-id="b5efb-120">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="b5efb-120">Specifies a description.</span></span>

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

### <span data-ttu-id="b5efb-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="b5efb-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="b5efb-122">Указывает URI конечной точки метаданных поставщика.</span><span class="sxs-lookup"><span data-stu-id="b5efb-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="b5efb-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5efb-123">-Name</span></span>
<span data-ttu-id="b5efb-124">Задает понятное имя для поставщика.</span><span class="sxs-lookup"><span data-stu-id="b5efb-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="b5efb-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b5efb-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="b5efb-126">Указывает идентификатор поставщика.</span><span class="sxs-lookup"><span data-stu-id="b5efb-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="b5efb-127">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="b5efb-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="b5efb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5efb-128">CommonParameters</span></span>
<span data-ttu-id="b5efb-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5efb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5efb-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5efb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5efb-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5efb-131">INPUTS</span></span>

### <span data-ttu-id="b5efb-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b5efb-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b5efb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b5efb-133">System.String</span></span>

## <span data-ttu-id="b5efb-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5efb-134">OUTPUTS</span></span>

### <span data-ttu-id="b5efb-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b5efb-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b5efb-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5efb-136">NOTES</span></span>

## <span data-ttu-id="b5efb-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5efb-137">RELATED LINKS</span></span>

[<span data-ttu-id="b5efb-138">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b5efb-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b5efb-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b5efb-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b5efb-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b5efb-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


