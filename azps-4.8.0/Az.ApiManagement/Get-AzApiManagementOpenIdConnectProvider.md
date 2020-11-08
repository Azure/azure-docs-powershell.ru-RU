---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078017"
---
# <span data-ttu-id="0aa1b-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0aa1b-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0aa1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0aa1b-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa1b-103">Возвращает поставщиков OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="0aa1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0aa1b-104">SYNTAX</span></span>

### <span data-ttu-id="0aa1b-105">GetAllOpenIdConnectProviders (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0aa1b-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0aa1b-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0aa1b-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0aa1b-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="0aa1b-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0aa1b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0aa1b-108">DESCRIPTION</span></span>
<span data-ttu-id="0aa1b-109">Командлет **Get-AzApiManagementOpenIdConnectProvider** получает поставщиков OpenID Connect в средстве управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="0aa1b-110">ClientSecret не будет включаться в данные результата.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="0aa1b-111">Чтобы получить секрет клиента, используйте **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="0aa1b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0aa1b-112">EXAMPLES</span></span>

### <span data-ttu-id="0aa1b-113">Пример 1: получение всех поставщиков</span><span class="sxs-lookup"><span data-stu-id="0aa1b-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="0aa1b-114">Эта команда получает все поставщики подключений OpenID для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="0aa1b-115">Пример 2: получение поставщика с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="0aa1b-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="0aa1b-116">Эта команда получает поставщик с ИДЕНТИФИКАТОРом OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="0aa1b-117">Пример 3: получение поставщика с помощью имени</span><span class="sxs-lookup"><span data-stu-id="0aa1b-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="0aa1b-118">Эта команда получает поставщика с именем "Contoso OpenID Connect Provider".</span><span class="sxs-lookup"><span data-stu-id="0aa1b-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="0aa1b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0aa1b-119">PARAMETERS</span></span>

### <span data-ttu-id="0aa1b-120">-Context</span><span class="sxs-lookup"><span data-stu-id="0aa1b-120">-Context</span></span>
<span data-ttu-id="0aa1b-121">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0aa1b-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0aa1b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aa1b-122">-DefaultProfile</span></span>
<span data-ttu-id="0aa1b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aa1b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0aa1b-124">-Name</span></span>
<span data-ttu-id="0aa1b-125">Указывает понятное имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="0aa1b-126">Если вы указали имя, этот командлет получает этот поставщик.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="0aa1b-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0aa1b-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="0aa1b-128">Указывает идентификатор поставщика, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="0aa1b-129">Если вы укажете идентификатор, этот командлет получает этот поставщик.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="0aa1b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa1b-130">CommonParameters</span></span>
<span data-ttu-id="0aa1b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0aa1b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa1b-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0aa1b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa1b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0aa1b-133">INPUTS</span></span>

### <span data-ttu-id="0aa1b-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0aa1b-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0aa1b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0aa1b-135">System.String</span></span>

## <span data-ttu-id="0aa1b-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0aa1b-136">OUTPUTS</span></span>

### <span data-ttu-id="0aa1b-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0aa1b-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0aa1b-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="0aa1b-138">NOTES</span></span>

## <span data-ttu-id="0aa1b-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0aa1b-139">RELATED LINKS</span></span>

[<span data-ttu-id="0aa1b-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0aa1b-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0aa1b-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0aa1b-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0aa1b-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0aa1b-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


