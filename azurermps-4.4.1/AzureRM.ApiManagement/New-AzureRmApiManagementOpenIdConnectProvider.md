---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f008d21e1d1d3f2aba7c87255fa7c95074bca532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565725"
---
# <span data-ttu-id="fddfe-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fddfe-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="fddfe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fddfe-102">SYNOPSIS</span></span>
<span data-ttu-id="fddfe-103">Создает поставщик подключений OpenID.</span><span class="sxs-lookup"><span data-stu-id="fddfe-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fddfe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fddfe-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fddfe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fddfe-105">DESCRIPTION</span></span>
<span data-ttu-id="fddfe-106">Командлет **New-AzureRmApiManagementOpenIdConnectProvider** создает поставщик OpenID Connect в управлении API Azure.</span><span class="sxs-lookup"><span data-stu-id="fddfe-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="fddfe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fddfe-107">EXAMPLES</span></span>

### <span data-ttu-id="fddfe-108">Пример 1: создание поставщика</span><span class="sxs-lookup"><span data-stu-id="fddfe-108">Example 1: Create a provider</span></span>
```
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="fddfe-109">Эта команда создает **поставщик** подключений OpenID, именуемый поставщиком Contoso OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="fddfe-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="fddfe-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fddfe-110">PARAMETERS</span></span>

### <span data-ttu-id="fddfe-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="fddfe-111">-ClientId</span></span>
<span data-ttu-id="fddfe-112">Указывает идентификатор клиента консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="fddfe-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="fddfe-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="fddfe-113">-ClientSecret</span></span>
<span data-ttu-id="fddfe-114">Указывает секрет клиента для консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="fddfe-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="fddfe-115">-Context</span><span class="sxs-lookup"><span data-stu-id="fddfe-115">-Context</span></span>
<span data-ttu-id="fddfe-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="fddfe-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fddfe-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="fddfe-117">-Description</span></span>
<span data-ttu-id="fddfe-118">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="fddfe-118">Specifies a description.</span></span>

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

### <span data-ttu-id="fddfe-119">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="fddfe-119">-MetadataEndpointUri</span></span>
<span data-ttu-id="fddfe-120">Указывает URI конечной точки метаданных поставщика.</span><span class="sxs-lookup"><span data-stu-id="fddfe-120">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="fddfe-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fddfe-121">-Name</span></span>
<span data-ttu-id="fddfe-122">Задает понятное имя для поставщика.</span><span class="sxs-lookup"><span data-stu-id="fddfe-122">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="fddfe-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="fddfe-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="fddfe-124">Указывает идентификатор поставщика.</span><span class="sxs-lookup"><span data-stu-id="fddfe-124">Specifies an ID for the provider.</span></span>
<span data-ttu-id="fddfe-125">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="fddfe-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="fddfe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fddfe-126">-DefaultProfile</span></span>
<span data-ttu-id="fddfe-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fddfe-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fddfe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fddfe-128">CommonParameters</span></span>
<span data-ttu-id="fddfe-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fddfe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fddfe-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fddfe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fddfe-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fddfe-131">INPUTS</span></span>

## <span data-ttu-id="fddfe-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fddfe-132">OUTPUTS</span></span>

### <span data-ttu-id="fddfe-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fddfe-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="fddfe-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="fddfe-134">NOTES</span></span>

## <span data-ttu-id="fddfe-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fddfe-135">RELATED LINKS</span></span>

[<span data-ttu-id="fddfe-136">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fddfe-136">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="fddfe-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fddfe-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="fddfe-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fddfe-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


