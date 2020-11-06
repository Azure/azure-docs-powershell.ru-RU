---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558035"
---
# <span data-ttu-id="877aa-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="877aa-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="877aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="877aa-102">SYNOPSIS</span></span>
<span data-ttu-id="877aa-103">Возвращает поставщиков OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="877aa-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="877aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="877aa-104">SYNTAX</span></span>

### <span data-ttu-id="877aa-105">Получение всех поставщиков OpenID Connect (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="877aa-105">Get all OpenID Connect Providers (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="877aa-106">Получить с помощью идентификатора поставщика OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="877aa-106">Get by OpenID Connect Provider ID</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="877aa-107">Поиск по понятному имени поставщика OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="877aa-107">Find by OpenID Connect Provider friendly Name</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="877aa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="877aa-108">DESCRIPTION</span></span>
<span data-ttu-id="877aa-109">Командлет **Get-AzureRmApiManagementOpenIdConnectProvider** получает поставщиков OpenID Connect в средстве управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="877aa-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="877aa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="877aa-110">EXAMPLES</span></span>

### <span data-ttu-id="877aa-111">Пример 1: получение всех поставщиков</span><span class="sxs-lookup"><span data-stu-id="877aa-111">Example 1: Get all providers</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

<span data-ttu-id="877aa-112">Эта команда получает все поставщики подключений OpenID для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="877aa-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="877aa-113">Пример 2: получение поставщика с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="877aa-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="877aa-114">Эта команда получает поставщик с ИДЕНТИФИКАТОРом OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="877aa-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="877aa-115">Пример 3: получение поставщика с помощью имени</span><span class="sxs-lookup"><span data-stu-id="877aa-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="877aa-116">Эта команда получает поставщика с именем "Contoso OpenID Connect Provider".</span><span class="sxs-lookup"><span data-stu-id="877aa-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="877aa-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="877aa-117">PARAMETERS</span></span>

### <span data-ttu-id="877aa-118">-Context</span><span class="sxs-lookup"><span data-stu-id="877aa-118">-Context</span></span>
<span data-ttu-id="877aa-119">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="877aa-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="877aa-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="877aa-120">-Name</span></span>
<span data-ttu-id="877aa-121">Указывает понятное имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="877aa-121">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="877aa-122">Если вы указали имя, этот командлет получает этот поставщик.</span><span class="sxs-lookup"><span data-stu-id="877aa-122">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877aa-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="877aa-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="877aa-124">Указывает идентификатор поставщика, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="877aa-124">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="877aa-125">Если вы укажете идентификатор, этот командлет получает этот поставщик.</span><span class="sxs-lookup"><span data-stu-id="877aa-125">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877aa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="877aa-126">-DefaultProfile</span></span>
<span data-ttu-id="877aa-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="877aa-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="877aa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877aa-128">CommonParameters</span></span>
<span data-ttu-id="877aa-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="877aa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877aa-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="877aa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877aa-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="877aa-131">INPUTS</span></span>

## <span data-ttu-id="877aa-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="877aa-132">OUTPUTS</span></span>

### <span data-ttu-id="877aa-133">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="877aa-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>

## <span data-ttu-id="877aa-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="877aa-134">NOTES</span></span>

## <span data-ttu-id="877aa-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="877aa-135">RELATED LINKS</span></span>

[<span data-ttu-id="877aa-136">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="877aa-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="877aa-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="877aa-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="877aa-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="877aa-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


