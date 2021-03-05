---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 1a46cccc38e1b562786e9eda88f3336430559fc0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014376"
---
# <span data-ttu-id="9b2af-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="9b2af-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="9b2af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b2af-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2af-103">Получает поставщики OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="9b2af-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="9b2af-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b2af-104">SYNTAX</span></span>

### <span data-ttu-id="9b2af-105">GetAllOpenIdConnectProviders (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b2af-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2af-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="9b2af-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2af-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="9b2af-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b2af-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b2af-108">DESCRIPTION</span></span>
<span data-ttu-id="9b2af-109">Для управления API Azure поставщики OpenID Connect получаются с использованием cmdlet **Get-AzApiManagementOpenIdProvider.**</span><span class="sxs-lookup"><span data-stu-id="9b2af-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="9b2af-110">ClientSecret не включается в сведения о результатах.</span><span class="sxs-lookup"><span data-stu-id="9b2af-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="9b2af-111">Чтобы получить секрет клиента, используйте **Get-AzApiManagementOpenIdConnectProviderClientSecret.**</span><span class="sxs-lookup"><span data-stu-id="9b2af-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="9b2af-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b2af-112">EXAMPLES</span></span>

### <span data-ttu-id="9b2af-113">Пример 1. Получить всех поставщиков</span><span class="sxs-lookup"><span data-stu-id="9b2af-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="9b2af-114">Эта команда получает все поставщики OpenID Connect для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="9b2af-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="9b2af-115">Пример 2. Как получить поставщика с помощью ИД</span><span class="sxs-lookup"><span data-stu-id="9b2af-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="9b2af-116">Эта команда возвращает поставщика ID OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="9b2af-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="9b2af-117">Пример 3. Как получить поставщика по имени</span><span class="sxs-lookup"><span data-stu-id="9b2af-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="9b2af-118">Эта команда возвращает поставщика Contoso OpenID Connect Provider.</span><span class="sxs-lookup"><span data-stu-id="9b2af-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="9b2af-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b2af-119">PARAMETERS</span></span>

### <span data-ttu-id="9b2af-120">-Контекст</span><span class="sxs-lookup"><span data-stu-id="9b2af-120">-Context</span></span>
<span data-ttu-id="9b2af-121">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="9b2af-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9b2af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2af-122">-DefaultProfile</span></span>
<span data-ttu-id="9b2af-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2af-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b2af-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9b2af-124">-Name</span></span>
<span data-ttu-id="9b2af-125">Указывает имя, которое удобно для поставщика.</span><span class="sxs-lookup"><span data-stu-id="9b2af-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="9b2af-126">Если указать имя, этот cmdlet получит этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="9b2af-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="9b2af-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="9b2af-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="9b2af-128">Определяет код поставщика, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b2af-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="9b2af-129">Если указать код, этот cmdlet получит этого поставщика.</span><span class="sxs-lookup"><span data-stu-id="9b2af-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="9b2af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2af-130">CommonParameters</span></span>
<span data-ttu-id="9b2af-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b2af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2af-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b2af-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2af-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b2af-133">INPUTS</span></span>

### <span data-ttu-id="9b2af-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b2af-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9b2af-135">System.String</span><span class="sxs-lookup"><span data-stu-id="9b2af-135">System.String</span></span>

## <span data-ttu-id="9b2af-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b2af-136">OUTPUTS</span></span>

### <span data-ttu-id="9b2af-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="9b2af-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="9b2af-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b2af-138">NOTES</span></span>

## <span data-ttu-id="9b2af-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b2af-139">RELATED LINKS</span></span>

[<span data-ttu-id="9b2af-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="9b2af-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="9b2af-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="9b2af-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="9b2af-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="9b2af-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


