---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: b39ae66a5881acca72143274c479685ef1282854
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073877"
---
# <span data-ttu-id="68325-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="68325-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="68325-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68325-102">SYNOPSIS</span></span>
<span data-ttu-id="68325-103">Возвращает поставщиков OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="68325-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="68325-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68325-104">SYNTAX</span></span>

### <span data-ttu-id="68325-105">GetAllOpenIdConnectProviders (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="68325-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68325-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="68325-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68325-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="68325-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68325-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68325-108">DESCRIPTION</span></span>
<span data-ttu-id="68325-109">Командлет **Get-AzApiManagementOpenIdConnectProvider** получает поставщиков OpenID Connect в средстве управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="68325-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="68325-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68325-110">EXAMPLES</span></span>

### <span data-ttu-id="68325-111">Пример 1: получение всех поставщиков</span><span class="sxs-lookup"><span data-stu-id="68325-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="68325-112">Эта команда получает все поставщики подключений OpenID для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="68325-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="68325-113">Пример 2: получение поставщика с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="68325-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="68325-114">Эта команда получает поставщик с ИДЕНТИФИКАТОРом OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="68325-114">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="68325-115">Пример 3: получение поставщика с помощью имени</span><span class="sxs-lookup"><span data-stu-id="68325-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="68325-116">Эта команда получает поставщика с именем "Contoso OpenID Connect Provider".</span><span class="sxs-lookup"><span data-stu-id="68325-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="68325-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68325-117">PARAMETERS</span></span>

### <span data-ttu-id="68325-118">-Context</span><span class="sxs-lookup"><span data-stu-id="68325-118">-Context</span></span>
<span data-ttu-id="68325-119">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="68325-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="68325-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68325-120">-DefaultProfile</span></span>
<span data-ttu-id="68325-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68325-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68325-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="68325-122">-Name</span></span>
<span data-ttu-id="68325-123">Указывает понятное имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="68325-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="68325-124">Если вы указали имя, этот командлет получает этот поставщик.</span><span class="sxs-lookup"><span data-stu-id="68325-124">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="68325-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="68325-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="68325-126">Указывает идентификатор поставщика, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="68325-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="68325-127">Если вы укажете идентификатор, этот командлет получает этот поставщик.</span><span class="sxs-lookup"><span data-stu-id="68325-127">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="68325-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68325-128">CommonParameters</span></span>
<span data-ttu-id="68325-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68325-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68325-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68325-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68325-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68325-131">INPUTS</span></span>

### <span data-ttu-id="68325-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="68325-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="68325-133">System. String</span><span class="sxs-lookup"><span data-stu-id="68325-133">System.String</span></span>

## <span data-ttu-id="68325-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68325-134">OUTPUTS</span></span>

### <span data-ttu-id="68325-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="68325-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="68325-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="68325-136">NOTES</span></span>

## <span data-ttu-id="68325-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68325-137">RELATED LINKS</span></span>

[<span data-ttu-id="68325-138">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="68325-138">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="68325-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="68325-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="68325-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="68325-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


