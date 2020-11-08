---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 30947e52e5a7afaa8bf2890b95f48f6bb6f36bce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073859"
---
# <span data-ttu-id="8ddd9-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8ddd9-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="8ddd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ddd9-102">SYNOPSIS</span></span>
<span data-ttu-id="8ddd9-103">Обновляет сервер.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-103">Updates a Backend.</span></span>

## <span data-ttu-id="8ddd9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ddd9-104">SYNTAX</span></span>

### <span data-ttu-id="8ddd9-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ddd9-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ddd9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ddd9-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ddd9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ddd9-107">DESCRIPTION</span></span>
<span data-ttu-id="8ddd9-108">Обновляет существующую базу данных в управлении API.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="8ddd9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ddd9-109">EXAMPLES</span></span>

### <span data-ttu-id="8ddd9-110">Обновляет описание внутреннего сервера 123</span><span class="sxs-lookup"><span data-stu-id="8ddd9-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="8ddd9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ddd9-111">PARAMETERS</span></span>

### <span data-ttu-id="8ddd9-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="8ddd9-112">-BackendId</span></span>
<span data-ttu-id="8ddd9-113">Идентификатор нового внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-113">Identifier of new backend.</span></span>
<span data-ttu-id="8ddd9-114">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd9-115">-Context</span><span class="sxs-lookup"><span data-stu-id="8ddd9-115">-Context</span></span>
<span data-ttu-id="8ddd9-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8ddd9-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd9-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="8ddd9-118">-Credential</span></span>
<span data-ttu-id="8ddd9-119">Сведения об учетных данных, которые следует использовать при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="8ddd9-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ddd9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ddd9-121">-DefaultProfile</span></span>
<span data-ttu-id="8ddd9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ddd9-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="8ddd9-123">-Description</span></span>
<span data-ttu-id="8ddd9-124">Описание внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-124">Backend Description.</span></span>
<span data-ttu-id="8ddd9-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ddd9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ddd9-126">-InputObject</span></span>
<span data-ttu-id="8ddd9-127">Экземпляр PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="8ddd9-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ddd9-129">-PassThru</span></span>
<span data-ttu-id="8ddd9-130">Указывает на то, что этот командлет возвращает  **PsApiManagementBackend** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8ddd9-131">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="8ddd9-131">-Protocol</span></span>
<span data-ttu-id="8ddd9-132">Внутренний протокол передачи данных (HTTP или SOAP).</span><span class="sxs-lookup"><span data-stu-id="8ddd9-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="8ddd9-133">Это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="8ddd9-133">This parameter is optional</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ddd9-134">-Прокси</span><span class="sxs-lookup"><span data-stu-id="8ddd9-134">-Proxy</span></span>
<span data-ttu-id="8ddd9-135">Сведения о прокси-сервере, которые необходимо использовать при отправке запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="8ddd9-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ddd9-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ddd9-137">-ResourceId</span></span>
<span data-ttu-id="8ddd9-138">Универсальный код ресурса (URI) для управления ресурсом во внешней системе.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="8ddd9-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-139">This parameter is optional.</span></span>
<span data-ttu-id="8ddd9-140">Этот URL-адрес может представлять собой идентификатор ресурса ARM для логических приложений, приложений-функций или приложений API.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="8ddd9-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="8ddd9-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="8ddd9-142">Сведения о внутреннем кластере кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="8ddd9-143">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ddd9-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="8ddd9-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="8ddd9-145">Необходимость пропуска проверки цепочки сертификатов при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="8ddd9-146">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ddd9-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="8ddd9-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="8ddd9-148">Следует ли пропускать проверку имени сертификата при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="8ddd9-149">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ddd9-150">-Title</span><span class="sxs-lookup"><span data-stu-id="8ddd9-150">-Title</span></span>
<span data-ttu-id="8ddd9-151">Название внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-151">Backend Title.</span></span>
<span data-ttu-id="8ddd9-152">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ddd9-153">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="8ddd9-153">-Url</span></span>
<span data-ttu-id="8ddd9-154">URL-адрес среды выполнения для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="8ddd9-155">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="8ddd9-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ddd9-156">-Confirm</span></span>
<span data-ttu-id="8ddd9-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ddd9-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ddd9-158">-WhatIf</span></span>
<span data-ttu-id="8ddd9-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ddd9-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ddd9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ddd9-161">CommonParameters</span></span>
<span data-ttu-id="8ddd9-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ddd9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ddd9-163">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ddd9-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ddd9-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ddd9-164">INPUTS</span></span>

### <span data-ttu-id="8ddd9-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8ddd9-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8ddd9-166">System. String</span><span class="sxs-lookup"><span data-stu-id="8ddd9-166">System.String</span></span>

### <span data-ttu-id="8ddd9-167">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ddd9-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8ddd9-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8ddd9-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="8ddd9-169">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8ddd9-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="8ddd9-170">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8ddd9-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="8ddd9-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8ddd9-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8ddd9-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ddd9-172">OUTPUTS</span></span>

### <span data-ttu-id="8ddd9-173">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8ddd9-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="8ddd9-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ddd9-174">NOTES</span></span>

## <span data-ttu-id="8ddd9-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ddd9-175">RELATED LINKS</span></span>

[<span data-ttu-id="8ddd9-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8ddd9-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="8ddd9-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8ddd9-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="8ddd9-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8ddd9-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="8ddd9-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8ddd9-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="8ddd9-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8ddd9-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
