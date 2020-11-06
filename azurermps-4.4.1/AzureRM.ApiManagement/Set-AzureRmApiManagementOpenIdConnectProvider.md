---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f890236907ea0a717245d9345be276a6ccf04b8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566335"
---
# <span data-ttu-id="a131c-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a131c-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="a131c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a131c-102">SYNOPSIS</span></span>
<span data-ttu-id="a131c-103">Изменение поставщика OpenID подключения.</span><span class="sxs-lookup"><span data-stu-id="a131c-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a131c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a131c-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a131c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a131c-105">DESCRIPTION</span></span>
<span data-ttu-id="a131c-106">Командлет **Set-AzureRmApiManagementOpenIdConnectProvider** изменяет поставщик соединения OpenID в Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="a131c-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="a131c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a131c-107">EXAMPLES</span></span>

### <span data-ttu-id="a131c-108">Пример 1: изменение секрета клиента для поставщика</span><span class="sxs-lookup"><span data-stu-id="a131c-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="a131c-109">Эта команда изменяет поставщика с ИДЕНТИФИКАТОРом OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="a131c-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="a131c-110">Команда задает секрет клиента для поставщика.</span><span class="sxs-lookup"><span data-stu-id="a131c-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="a131c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a131c-111">PARAMETERS</span></span>

### <span data-ttu-id="a131c-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="a131c-112">-ClientId</span></span>
<span data-ttu-id="a131c-113">Указывает идентификатор клиента консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="a131c-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="a131c-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="a131c-114">-ClientSecret</span></span>
<span data-ttu-id="a131c-115">Указывает секрет клиента для консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="a131c-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="a131c-116">-Context</span><span class="sxs-lookup"><span data-stu-id="a131c-116">-Context</span></span>
<span data-ttu-id="a131c-117">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a131c-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a131c-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="a131c-118">-Description</span></span>
<span data-ttu-id="a131c-119">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="a131c-119">Specifies a description.</span></span>

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

### <span data-ttu-id="a131c-120">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="a131c-120">-MetadataEndpointUri</span></span>
<span data-ttu-id="a131c-121">Указывает URI конечной точки метаданных поставщика.</span><span class="sxs-lookup"><span data-stu-id="a131c-121">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="a131c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a131c-122">-Name</span></span>
<span data-ttu-id="a131c-123">Задает понятное имя для поставщика.</span><span class="sxs-lookup"><span data-stu-id="a131c-123">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="a131c-124">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="a131c-124">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="a131c-125">Указывает идентификатор поставщика, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a131c-125">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="a131c-126">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="a131c-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="a131c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a131c-127">-PassThru</span></span>
<span data-ttu-id="a131c-128">Указывает на то, что этот командлет возвращает **PsApiManagementOpenIdConnectProvider** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a131c-128">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a131c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a131c-129">-DefaultProfile</span></span>
<span data-ttu-id="a131c-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a131c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a131c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a131c-131">CommonParameters</span></span>
<span data-ttu-id="a131c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a131c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a131c-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a131c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a131c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a131c-134">INPUTS</span></span>

## <span data-ttu-id="a131c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a131c-135">OUTPUTS</span></span>

### <span data-ttu-id="a131c-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a131c-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="a131c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="a131c-137">NOTES</span></span>

## <span data-ttu-id="a131c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a131c-138">RELATED LINKS</span></span>

[<span data-ttu-id="a131c-139">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a131c-139">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a131c-140">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a131c-140">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a131c-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a131c-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


