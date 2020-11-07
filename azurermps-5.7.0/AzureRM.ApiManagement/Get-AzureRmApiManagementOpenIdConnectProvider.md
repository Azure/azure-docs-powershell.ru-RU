---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c26fb8991acc47ab655cb47c44194ca209423a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733593"
---
# <span data-ttu-id="4c0e4-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4c0e4-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="4c0e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0e4-103">Возвращает поставщиков OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c0e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c0e4-104">SYNTAX</span></span>

### <span data-ttu-id="4c0e4-105">GetAllOpenIdConnectProviders (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4c0e4-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c0e4-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="4c0e4-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c0e4-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="4c0e4-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c0e4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c0e4-108">DESCRIPTION</span></span>
<span data-ttu-id="4c0e4-109">Командлет **Get-AzureRmApiManagementOpenIdConnectProvider** получает поставщиков OpenID Connect в средстве управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="4c0e4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c0e4-110">EXAMPLES</span></span>

### <span data-ttu-id="4c0e4-111">Пример 1: получение всех поставщиков</span><span class="sxs-lookup"><span data-stu-id="4c0e4-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="4c0e4-112">Эта команда получает все поставщики подключений OpenID для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="4c0e4-113">Пример 2: получение поставщика с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="4c0e4-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="4c0e4-114">Эта команда получает поставщик с ИДЕНТИФИКАТОРом OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="4c0e4-115">Пример 3: получение поставщика с помощью имени</span><span class="sxs-lookup"><span data-stu-id="4c0e4-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="4c0e4-116">Эта команда получает поставщика с именем "Contoso OpenID Connect Provider".</span><span class="sxs-lookup"><span data-stu-id="4c0e4-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="4c0e4-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c0e4-117">PARAMETERS</span></span>

### <span data-ttu-id="4c0e4-118">-Context</span><span class="sxs-lookup"><span data-stu-id="4c0e4-118">-Context</span></span>
<span data-ttu-id="4c0e4-119">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4c0e4-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4c0e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0e4-120">-DefaultProfile</span></span>
<span data-ttu-id="4c0e4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="4c0e4-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c0e4-122">-Name</span></span>
<span data-ttu-id="4c0e4-123">Указывает понятное имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="4c0e4-124">Если вы указали имя, этот командлет получает этот поставщик.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0e4-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="4c0e4-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="4c0e4-126">Указывает идентификатор поставщика, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="4c0e4-127">Если вы укажете идентификатор, этот командлет получает этот поставщик.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0e4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0e4-128">CommonParameters</span></span>
<span data-ttu-id="4c0e4-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0e4-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c0e4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0e4-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c0e4-131">INPUTS</span></span>

### <span data-ttu-id="4c0e4-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="4c0e4-132">None</span></span>
<span data-ttu-id="4c0e4-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c0e4-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c0e4-134">OUTPUTS</span></span>

### <span data-ttu-id="4c0e4-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4c0e4-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>
<span data-ttu-id="4c0e4-136">Сведения о поставщике подключений OpenId, настроенном в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-136">The detail of the OpenId connect Provider configured in API Management service.</span></span>

### <span data-ttu-id="4c0e4-137">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="4c0e4-137">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>
<span data-ttu-id="4c0e4-138">Список поставщиков подключений OpenId, настроенных в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-138">The list of OpenId Connect Providers configured in API Management service.</span></span>

## <span data-ttu-id="4c0e4-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c0e4-139">NOTES</span></span>

## <span data-ttu-id="4c0e4-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c0e4-140">RELATED LINKS</span></span>

[<span data-ttu-id="4c0e4-141">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4c0e4-141">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="4c0e4-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4c0e4-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="4c0e4-143">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="4c0e4-143">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


