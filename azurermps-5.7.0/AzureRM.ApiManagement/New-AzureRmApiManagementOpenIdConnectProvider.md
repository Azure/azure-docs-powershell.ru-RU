---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 088b88bcaa7f0d493552060c150e9d76a4b16c7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557640"
---
# <span data-ttu-id="1fe7b-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1fe7b-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="1fe7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fe7b-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe7b-103">Создает поставщик подключений OpenID.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fe7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fe7b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fe7b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fe7b-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe7b-106">Командлет **New-AzureRmApiManagementOpenIdConnectProvider** создает поставщик OpenID Connect в управлении API Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="1fe7b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fe7b-107">EXAMPLES</span></span>

### <span data-ttu-id="1fe7b-108">Пример 1: создание поставщика</span><span class="sxs-lookup"><span data-stu-id="1fe7b-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="1fe7b-109">Эта команда создает **поставщик** подключений OpenID, именуемый поставщиком Contoso OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="1fe7b-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="1fe7b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fe7b-110">PARAMETERS</span></span>

### <span data-ttu-id="1fe7b-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="1fe7b-111">-ClientId</span></span>
<span data-ttu-id="1fe7b-112">Указывает идентификатор клиента консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-112">Specifies the client ID of the developer console.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe7b-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="1fe7b-113">-ClientSecret</span></span>
<span data-ttu-id="1fe7b-114">Указывает секрет клиента для консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-114">Specifies the client secret of the developer console.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe7b-115">-Context</span><span class="sxs-lookup"><span data-stu-id="1fe7b-115">-Context</span></span>
<span data-ttu-id="1fe7b-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1fe7b-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe7b-117">-DefaultProfile</span></span>
<span data-ttu-id="1fe7b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe7b-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="1fe7b-119">-Description</span></span>
<span data-ttu-id="1fe7b-120">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-120">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe7b-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="1fe7b-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="1fe7b-122">Указывает URI конечной точки метаданных поставщика.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-122">Specifies a metadata endpoint URI of the provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe7b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fe7b-123">-Name</span></span>
<span data-ttu-id="1fe7b-124">Задает понятное имя для поставщика.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-124">Specifies a friendly name for the provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe7b-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="1fe7b-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="1fe7b-126">Указывает идентификатор поставщика.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="1fe7b-127">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-127">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe7b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe7b-128">CommonParameters</span></span>
<span data-ttu-id="1fe7b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe7b-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe7b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe7b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fe7b-131">INPUTS</span></span>

### <span data-ttu-id="1fe7b-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="1fe7b-132">None</span></span>
<span data-ttu-id="1fe7b-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1fe7b-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1fe7b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fe7b-134">OUTPUTS</span></span>

### <span data-ttu-id="1fe7b-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1fe7b-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="1fe7b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fe7b-136">NOTES</span></span>

## <span data-ttu-id="1fe7b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fe7b-137">RELATED LINKS</span></span>

[<span data-ttu-id="1fe7b-138">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1fe7b-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="1fe7b-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1fe7b-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="1fe7b-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1fe7b-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


