---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6f568f27cf5b50cd517d8133578d6cf36060252f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558628"
---
# <span data-ttu-id="90331-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="90331-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="90331-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90331-102">SYNOPSIS</span></span>
<span data-ttu-id="90331-103">Изменение поставщика OpenID подключения.</span><span class="sxs-lookup"><span data-stu-id="90331-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90331-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90331-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90331-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90331-105">DESCRIPTION</span></span>
<span data-ttu-id="90331-106">Командлет **Set-AzureRmApiManagementOpenIdConnectProvider** изменяет поставщик соединения OpenID в Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="90331-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="90331-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90331-107">EXAMPLES</span></span>

### <span data-ttu-id="90331-108">Пример 1: изменение секрета клиента для поставщика</span><span class="sxs-lookup"><span data-stu-id="90331-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="90331-109">Эта команда изменяет поставщика с ИДЕНТИФИКАТОРом OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="90331-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="90331-110">Команда задает секрет клиента для поставщика.</span><span class="sxs-lookup"><span data-stu-id="90331-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="90331-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90331-111">PARAMETERS</span></span>

### <span data-ttu-id="90331-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="90331-112">-ClientId</span></span>
<span data-ttu-id="90331-113">Указывает идентификатор клиента консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="90331-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="90331-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="90331-114">-ClientSecret</span></span>
<span data-ttu-id="90331-115">Указывает секрет клиента для консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="90331-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="90331-116">-Context</span><span class="sxs-lookup"><span data-stu-id="90331-116">-Context</span></span>
<span data-ttu-id="90331-117">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="90331-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="90331-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90331-118">-DefaultProfile</span></span>
<span data-ttu-id="90331-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90331-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90331-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="90331-120">-Description</span></span>
<span data-ttu-id="90331-121">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="90331-121">Specifies a description.</span></span>

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

### <span data-ttu-id="90331-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="90331-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="90331-123">Указывает URI конечной точки метаданных поставщика.</span><span class="sxs-lookup"><span data-stu-id="90331-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="90331-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="90331-124">-Name</span></span>
<span data-ttu-id="90331-125">Задает понятное имя для поставщика.</span><span class="sxs-lookup"><span data-stu-id="90331-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="90331-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="90331-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="90331-127">Указывает идентификатор поставщика, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="90331-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="90331-128">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="90331-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="90331-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90331-129">-PassThru</span></span>
<span data-ttu-id="90331-130">Указывает на то, что этот командлет возвращает **PsApiManagementOpenIdConnectProvider** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="90331-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="90331-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90331-131">CommonParameters</span></span>
<span data-ttu-id="90331-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90331-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90331-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90331-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90331-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90331-134">INPUTS</span></span>

### <span data-ttu-id="90331-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="90331-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="90331-136">System. String</span><span class="sxs-lookup"><span data-stu-id="90331-136">System.String</span></span>

### <span data-ttu-id="90331-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="90331-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="90331-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90331-138">OUTPUTS</span></span>

### <span data-ttu-id="90331-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="90331-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="90331-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="90331-140">NOTES</span></span>

## <span data-ttu-id="90331-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90331-141">RELATED LINKS</span></span>

[<span data-ttu-id="90331-142">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="90331-142">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="90331-143">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="90331-143">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="90331-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="90331-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


