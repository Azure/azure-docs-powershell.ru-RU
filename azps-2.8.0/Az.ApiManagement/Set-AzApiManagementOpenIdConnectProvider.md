---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 880c44e3edf8a5d2c95144d2af8910e73d366192
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727931"
---
# <span data-ttu-id="dcc9c-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dcc9c-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="dcc9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcc9c-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc9c-103">Изменение поставщика OpenID подключения.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="dcc9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcc9c-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcc9c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcc9c-105">DESCRIPTION</span></span>
<span data-ttu-id="dcc9c-106">Командлет **Set-AzApiManagementOpenIdConnectProvider** изменяет поставщик соединения OpenID в Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="dcc9c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcc9c-107">EXAMPLES</span></span>

### <span data-ttu-id="dcc9c-108">Пример 1: изменение секрета клиента для поставщика</span><span class="sxs-lookup"><span data-stu-id="dcc9c-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="dcc9c-109">Эта команда изменяет поставщика с ИДЕНТИФИКАТОРом OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-109">This command modifies the provider that has the ID OICProvider01.</span></span>
<span data-ttu-id="dcc9c-110">Команда задает секрет клиента для поставщика.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="dcc9c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcc9c-111">PARAMETERS</span></span>

### <span data-ttu-id="dcc9c-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="dcc9c-112">-ClientId</span></span>
<span data-ttu-id="dcc9c-113">Указывает идентификатор клиента консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="dcc9c-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="dcc9c-114">-ClientSecret</span></span>
<span data-ttu-id="dcc9c-115">Указывает секрет клиента для консоли разработчика.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="dcc9c-116">-Context</span><span class="sxs-lookup"><span data-stu-id="dcc9c-116">-Context</span></span>
<span data-ttu-id="dcc9c-117">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="dcc9c-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dcc9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc9c-118">-DefaultProfile</span></span>
<span data-ttu-id="dcc9c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcc9c-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="dcc9c-120">-Description</span></span>
<span data-ttu-id="dcc9c-121">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-121">Specifies a description.</span></span>

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

### <span data-ttu-id="dcc9c-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="dcc9c-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="dcc9c-123">Указывает URI конечной точки метаданных поставщика.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="dcc9c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dcc9c-124">-Name</span></span>
<span data-ttu-id="dcc9c-125">Задает понятное имя для поставщика.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="dcc9c-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="dcc9c-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="dcc9c-127">Указывает идентификатор поставщика, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="dcc9c-128">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="dcc9c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcc9c-129">-PassThru</span></span>
<span data-ttu-id="dcc9c-130">Указывает на то, что этот командлет возвращает **PsApiManagementOpenIdConnectProvider** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="dcc9c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcc9c-131">-Confirm</span></span>
<span data-ttu-id="dcc9c-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc9c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcc9c-133">-WhatIf</span></span>
<span data-ttu-id="dcc9c-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcc9c-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc9c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc9c-136">CommonParameters</span></span>
<span data-ttu-id="dcc9c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcc9c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc9c-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcc9c-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc9c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcc9c-139">INPUTS</span></span>

### <span data-ttu-id="dcc9c-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dcc9c-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dcc9c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="dcc9c-141">System.String</span></span>

### <span data-ttu-id="dcc9c-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dcc9c-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dcc9c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcc9c-143">OUTPUTS</span></span>

### <span data-ttu-id="dcc9c-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dcc9c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="dcc9c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcc9c-145">NOTES</span></span>

## <span data-ttu-id="dcc9c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcc9c-146">RELATED LINKS</span></span>

[<span data-ttu-id="dcc9c-147">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dcc9c-147">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="dcc9c-148">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dcc9c-148">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="dcc9c-149">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="dcc9c-149">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


