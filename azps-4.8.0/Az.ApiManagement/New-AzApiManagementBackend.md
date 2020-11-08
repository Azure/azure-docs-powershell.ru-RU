---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 4ed63d0e3b801572698b123038a2022e89672a88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079893"
---
# <span data-ttu-id="1a293-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1a293-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="1a293-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a293-102">SYNOPSIS</span></span>
<span data-ttu-id="1a293-103">Создание новой серверной сущности.</span><span class="sxs-lookup"><span data-stu-id="1a293-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="1a293-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a293-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a293-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a293-105">DESCRIPTION</span></span>
<span data-ttu-id="1a293-106">Создает новую серверную сущность в управлении API.</span><span class="sxs-lookup"><span data-stu-id="1a293-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="1a293-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a293-107">EXAMPLES</span></span>

### <span data-ttu-id="1a293-108">Пример 1: создание базы данных в 123 с помощью базовой схемы авторизации</span><span class="sxs-lookup"><span data-stu-id="1a293-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="1a293-109">Создание новой базы данных</span><span class="sxs-lookup"><span data-stu-id="1a293-109">Creates a new Backend</span></span>

## <span data-ttu-id="1a293-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a293-110">PARAMETERS</span></span>

### <span data-ttu-id="1a293-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="1a293-111">-BackendId</span></span>
<span data-ttu-id="1a293-112">Идентификатор нового внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1a293-112">Identifier of new backend.</span></span>
<span data-ttu-id="1a293-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-113">This parameter is optional.</span></span>
<span data-ttu-id="1a293-114">Если не указано, будет создано.</span><span class="sxs-lookup"><span data-stu-id="1a293-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="1a293-115">-Context</span><span class="sxs-lookup"><span data-stu-id="1a293-115">-Context</span></span>
<span data-ttu-id="1a293-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1a293-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1a293-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-117">This parameter is required.</span></span>

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

### <span data-ttu-id="1a293-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="1a293-118">-Credential</span></span>
<span data-ttu-id="1a293-119">Сведения об учетных данных, которые следует использовать при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="1a293-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="1a293-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-120">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a293-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a293-121">-DefaultProfile</span></span>
<span data-ttu-id="1a293-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a293-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a293-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="1a293-123">-Description</span></span>
<span data-ttu-id="1a293-124">Описание внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1a293-124">Backend Description.</span></span>
<span data-ttu-id="1a293-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="1a293-126">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="1a293-126">-Protocol</span></span>
<span data-ttu-id="1a293-127">Внутренний протокол связи.</span><span class="sxs-lookup"><span data-stu-id="1a293-127">Backend Communication protocol.</span></span>
<span data-ttu-id="1a293-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-128">This parameter is required.</span></span>
<span data-ttu-id="1a293-129">Допустимые значения: "http" и "SOAP".</span><span class="sxs-lookup"><span data-stu-id="1a293-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a293-130">-Прокси</span><span class="sxs-lookup"><span data-stu-id="1a293-130">-Proxy</span></span>
<span data-ttu-id="1a293-131">Сведения о прокси-сервере, которые необходимо использовать при отправке запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="1a293-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="1a293-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-132">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a293-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a293-133">-ResourceId</span></span>
<span data-ttu-id="1a293-134">Универсальный код ресурса (URI) для управления ресурсом во внешней системе.</span><span class="sxs-lookup"><span data-stu-id="1a293-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="1a293-135">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-135">This parameter is optional.</span></span>
<span data-ttu-id="1a293-136">Этот URL-адрес может представлять собой идентификатор ресурса ARM для логических приложений, приложений-функций или приложений API.</span><span class="sxs-lookup"><span data-stu-id="1a293-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="1a293-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1a293-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="1a293-138">Сведения о внутреннем кластере кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="1a293-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="1a293-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a293-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="1a293-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="1a293-141">Необходимость пропуска проверки цепочки сертификатов при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="1a293-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="1a293-142">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-142">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a293-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="1a293-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="1a293-144">Следует ли пропускать проверку имени сертификата при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="1a293-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="1a293-145">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-145">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a293-146">-Title</span><span class="sxs-lookup"><span data-stu-id="1a293-146">-Title</span></span>
<span data-ttu-id="1a293-147">Название внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1a293-147">Backend Title.</span></span>
<span data-ttu-id="1a293-148">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="1a293-149">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="1a293-149">-Url</span></span>
<span data-ttu-id="1a293-150">URL-адрес среды выполнения для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1a293-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="1a293-151">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1a293-151">This parameter is required.</span></span>

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

### <span data-ttu-id="1a293-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a293-152">-Confirm</span></span>
<span data-ttu-id="1a293-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1a293-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a293-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a293-154">-WhatIf</span></span>
<span data-ttu-id="1a293-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1a293-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a293-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1a293-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a293-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a293-157">CommonParameters</span></span>
<span data-ttu-id="1a293-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a293-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a293-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a293-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a293-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a293-160">INPUTS</span></span>

### <span data-ttu-id="1a293-161">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1a293-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1a293-162">System. String</span><span class="sxs-lookup"><span data-stu-id="1a293-162">System.String</span></span>

### <span data-ttu-id="1a293-163">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1a293-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1a293-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1a293-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="1a293-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1a293-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="1a293-166">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1a293-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="1a293-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a293-167">OUTPUTS</span></span>

### <span data-ttu-id="1a293-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1a293-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="1a293-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a293-169">NOTES</span></span>

## <span data-ttu-id="1a293-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a293-170">RELATED LINKS</span></span>

[<span data-ttu-id="1a293-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1a293-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="1a293-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1a293-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="1a293-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1a293-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="1a293-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1a293-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="1a293-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1a293-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

