---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: fe320af601fad9d905471525b1a418c12c355f63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901569"
---
# <span data-ttu-id="a4dcf-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a4dcf-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="a4dcf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dcf-103">Изменение поставщика OpenID подключения.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="a4dcf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4dcf-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4dcf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4dcf-105">DESCRIPTION</span></span>
<span data-ttu-id="a4dcf-106">Командлет **Set-AzApiManagementOpenIdConnectProvider** изменяет поставщик соединения OpenID в Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="a4dcf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4dcf-107">EXAMPLES</span></span>

### <span data-ttu-id="a4dcf-108">Пример 1: изменение секрета клиента для поставщика</span><span class="sxs-lookup"><span data-stu-id="a4dcf-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="a4dcf-109">Эта команда изменяет поставщика с ИДЕНТИФИКАТОРом OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="a4dcf-110">Команда задает секрет клиента для поставщика.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="a4dcf-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4dcf-111">PARAMETERS</span></span>

### <span data-ttu-id="a4dcf-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="a4dcf-112">-ClientId</span></span>
<span data-ttu-id="a4dcf-113">Указывает идентификатор клиента консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="a4dcf-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="a4dcf-114">-ClientSecret</span></span>
<span data-ttu-id="a4dcf-115">Указывает секрет клиента для консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="a4dcf-116">-Context</span><span class="sxs-lookup"><span data-stu-id="a4dcf-116">-Context</span></span>
<span data-ttu-id="a4dcf-117">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a4dcf-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a4dcf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4dcf-118">-DefaultProfile</span></span>
<span data-ttu-id="a4dcf-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4dcf-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="a4dcf-120">-Description</span></span>
<span data-ttu-id="a4dcf-121">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-121">Specifies a description.</span></span>

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

### <span data-ttu-id="a4dcf-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="a4dcf-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="a4dcf-123">Указывает URI конечной точки метаданных поставщика.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="a4dcf-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4dcf-124">-Name</span></span>
<span data-ttu-id="a4dcf-125">Задает понятное имя для поставщика.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="a4dcf-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="a4dcf-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="a4dcf-127">Указывает идентификатор поставщика, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="a4dcf-128">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="a4dcf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4dcf-129">-PassThru</span></span>
<span data-ttu-id="a4dcf-130">Указывает на то, что этот командлет возвращает **PsApiManagementOpenIdConnectProvider** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a4dcf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dcf-131">CommonParameters</span></span>
<span data-ttu-id="a4dcf-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4dcf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dcf-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4dcf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dcf-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4dcf-134">INPUTS</span></span>

### <span data-ttu-id="a4dcf-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a4dcf-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a4dcf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a4dcf-136">System.String</span></span>

### <span data-ttu-id="a4dcf-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a4dcf-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a4dcf-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4dcf-138">OUTPUTS</span></span>

### <span data-ttu-id="a4dcf-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a4dcf-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="a4dcf-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4dcf-140">NOTES</span></span>

## <span data-ttu-id="a4dcf-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4dcf-141">RELATED LINKS</span></span>

[<span data-ttu-id="a4dcf-142">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a4dcf-142">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a4dcf-143">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a4dcf-143">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a4dcf-144">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a4dcf-144">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


