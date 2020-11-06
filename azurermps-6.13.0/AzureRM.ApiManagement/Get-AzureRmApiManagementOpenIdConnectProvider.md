---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 0ffe2dfbd1ccbb05ef1ad828861e1d439373caa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556987"
---
# <span data-ttu-id="3f29c-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3f29c-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="3f29c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f29c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f29c-103">Возвращает поставщиков OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="3f29c-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f29c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f29c-104">SYNTAX</span></span>

### <span data-ttu-id="3f29c-105">GetAllOpenIdConnectProviders (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f29c-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f29c-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="3f29c-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f29c-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="3f29c-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f29c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f29c-108">DESCRIPTION</span></span>
<span data-ttu-id="3f29c-109">Командлет **Get-AzureRmApiManagementOpenIdConnectProvider** получает поставщиков OpenID Connect в средстве управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="3f29c-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="3f29c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f29c-110">EXAMPLES</span></span>

### <span data-ttu-id="3f29c-111">Пример 1: получение всех поставщиков</span><span class="sxs-lookup"><span data-stu-id="3f29c-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="3f29c-112">Эта команда получает все поставщики подключений OpenID для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="3f29c-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="3f29c-113">Пример 2: получение поставщика с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="3f29c-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="3f29c-114">Эта команда получает поставщик с ИДЕНТИФИКАТОРом OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="3f29c-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="3f29c-115">Пример 3: получение поставщика с помощью имени</span><span class="sxs-lookup"><span data-stu-id="3f29c-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="3f29c-116">Эта команда получает поставщика с именем "Contoso OpenID Connect Provider".</span><span class="sxs-lookup"><span data-stu-id="3f29c-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="3f29c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f29c-117">PARAMETERS</span></span>

### <span data-ttu-id="3f29c-118">-Context</span><span class="sxs-lookup"><span data-stu-id="3f29c-118">-Context</span></span>
<span data-ttu-id="3f29c-119">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3f29c-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3f29c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f29c-120">-DefaultProfile</span></span>
<span data-ttu-id="3f29c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f29c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f29c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f29c-122">-Name</span></span>
<span data-ttu-id="3f29c-123">Указывает понятное имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="3f29c-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="3f29c-124">Если вы указали имя, этот командлет получает этот поставщик.</span><span class="sxs-lookup"><span data-stu-id="3f29c-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f29c-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="3f29c-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="3f29c-126">Указывает идентификатор поставщика, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3f29c-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="3f29c-127">Если вы укажете идентификатор, этот командлет получает этот поставщик.</span><span class="sxs-lookup"><span data-stu-id="3f29c-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f29c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f29c-128">CommonParameters</span></span>
<span data-ttu-id="3f29c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f29c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f29c-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f29c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f29c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f29c-131">INPUTS</span></span>

### <span data-ttu-id="3f29c-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3f29c-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3f29c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3f29c-133">System.String</span></span>

## <span data-ttu-id="3f29c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f29c-134">OUTPUTS</span></span>

### <span data-ttu-id="3f29c-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3f29c-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="3f29c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f29c-136">NOTES</span></span>

## <span data-ttu-id="3f29c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f29c-137">RELATED LINKS</span></span>

[<span data-ttu-id="3f29c-138">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3f29c-138">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3f29c-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3f29c-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="3f29c-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="3f29c-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


