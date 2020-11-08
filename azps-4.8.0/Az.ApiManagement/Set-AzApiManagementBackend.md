---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 41d10720bbce8a9d5498fe954908d817ce79af5d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080109"
---
# <span data-ttu-id="3a41b-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3a41b-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="3a41b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a41b-102">SYNOPSIS</span></span>
<span data-ttu-id="3a41b-103">Обновляет сервер.</span><span class="sxs-lookup"><span data-stu-id="3a41b-103">Updates a Backend.</span></span>

## <span data-ttu-id="3a41b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a41b-104">SYNTAX</span></span>

### <span data-ttu-id="3a41b-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a41b-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a41b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3a41b-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a41b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a41b-107">DESCRIPTION</span></span>
<span data-ttu-id="3a41b-108">Обновляет существующую базу данных в управлении API.</span><span class="sxs-lookup"><span data-stu-id="3a41b-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="3a41b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a41b-109">EXAMPLES</span></span>

### <span data-ttu-id="3a41b-110">Пример 1: Обновление описания серверной части 123</span><span class="sxs-lookup"><span data-stu-id="3a41b-110">Example 1: Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

### <span data-ttu-id="3a41b-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3a41b-111">Example 2</span></span>

<span data-ttu-id="3a41b-112">Обновляет сервер.</span><span class="sxs-lookup"><span data-stu-id="3a41b-112">Updates a Backend.</span></span> <span data-ttu-id="3a41b-113">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="3a41b-113">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementBackend -BackendId 123 -Context <PsApiManagementContext> -Credential <PsApiManagementBackendCredential> -Protocol http -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso -Url 'https://contoso.com/awesomeapi'
```

## <span data-ttu-id="3a41b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a41b-114">PARAMETERS</span></span>

### <span data-ttu-id="3a41b-115">-BackendId</span><span class="sxs-lookup"><span data-stu-id="3a41b-115">-BackendId</span></span>
<span data-ttu-id="3a41b-116">Идентификатор нового внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="3a41b-116">Identifier of new backend.</span></span>
<span data-ttu-id="3a41b-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-117">This parameter is required.</span></span>

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

### <span data-ttu-id="3a41b-118">-Context</span><span class="sxs-lookup"><span data-stu-id="3a41b-118">-Context</span></span>
<span data-ttu-id="3a41b-119">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3a41b-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3a41b-120">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-120">This parameter is required.</span></span>

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

### <span data-ttu-id="3a41b-121">-Credential</span><span class="sxs-lookup"><span data-stu-id="3a41b-121">-Credential</span></span>
<span data-ttu-id="3a41b-122">Сведения об учетных данных, которые следует использовать при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="3a41b-122">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="3a41b-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a41b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a41b-124">-DefaultProfile</span></span>
<span data-ttu-id="3a41b-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a41b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a41b-126">-Описание</span><span class="sxs-lookup"><span data-stu-id="3a41b-126">-Description</span></span>
<span data-ttu-id="3a41b-127">Описание внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="3a41b-127">Backend Description.</span></span>
<span data-ttu-id="3a41b-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a41b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a41b-129">-InputObject</span></span>
<span data-ttu-id="3a41b-130">Экземпляр PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="3a41b-130">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="3a41b-131">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-131">This parameter is required.</span></span>

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

### <span data-ttu-id="3a41b-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a41b-132">-PassThru</span></span>
<span data-ttu-id="3a41b-133">Указывает на то, что этот командлет возвращает  **PsApiManagementBackend** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3a41b-133">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3a41b-134">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="3a41b-134">-Protocol</span></span>
<span data-ttu-id="3a41b-135">Внутренний протокол передачи данных (HTTP или SOAP).</span><span class="sxs-lookup"><span data-stu-id="3a41b-135">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="3a41b-136">Это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="3a41b-136">This parameter is optional</span></span>

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

### <span data-ttu-id="3a41b-137">-Прокси</span><span class="sxs-lookup"><span data-stu-id="3a41b-137">-Proxy</span></span>
<span data-ttu-id="3a41b-138">Сведения о прокси-сервере, которые необходимо использовать при отправке запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="3a41b-138">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="3a41b-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a41b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a41b-140">-ResourceId</span></span>
<span data-ttu-id="3a41b-141">Универсальный код ресурса (URI) для управления ресурсом во внешней системе.</span><span class="sxs-lookup"><span data-stu-id="3a41b-141">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="3a41b-142">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-142">This parameter is optional.</span></span>
<span data-ttu-id="3a41b-143">Этот URL-адрес может представлять собой идентификатор ресурса ARM для логических приложений, приложений-функций или приложений API.</span><span class="sxs-lookup"><span data-stu-id="3a41b-143">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="3a41b-144">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="3a41b-144">-ServiceFabricCluster</span></span>
<span data-ttu-id="3a41b-145">Сведения о внутреннем кластере кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="3a41b-145">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="3a41b-146">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a41b-147">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="3a41b-147">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="3a41b-148">Необходимость пропуска проверки цепочки сертификатов при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="3a41b-148">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="3a41b-149">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a41b-150">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="3a41b-150">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="3a41b-151">Следует ли пропускать проверку имени сертификата при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="3a41b-151">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="3a41b-152">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a41b-153">-Title</span><span class="sxs-lookup"><span data-stu-id="3a41b-153">-Title</span></span>
<span data-ttu-id="3a41b-154">Название внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="3a41b-154">Backend Title.</span></span>
<span data-ttu-id="3a41b-155">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a41b-156">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="3a41b-156">-Url</span></span>
<span data-ttu-id="3a41b-157">URL-адрес среды выполнения для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="3a41b-157">Runtime Url for the Backend.</span></span>
<span data-ttu-id="3a41b-158">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3a41b-158">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a41b-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a41b-159">-Confirm</span></span>
<span data-ttu-id="3a41b-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a41b-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a41b-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a41b-161">-WhatIf</span></span>
<span data-ttu-id="3a41b-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a41b-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a41b-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a41b-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a41b-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a41b-164">CommonParameters</span></span>
<span data-ttu-id="3a41b-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a41b-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a41b-166">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a41b-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a41b-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a41b-167">INPUTS</span></span>

### <span data-ttu-id="3a41b-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3a41b-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3a41b-169">System. String</span><span class="sxs-lookup"><span data-stu-id="3a41b-169">System.String</span></span>

### <span data-ttu-id="3a41b-170">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3a41b-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3a41b-171">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="3a41b-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="3a41b-172">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="3a41b-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="3a41b-173">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a41b-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="3a41b-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3a41b-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3a41b-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a41b-175">OUTPUTS</span></span>

### <span data-ttu-id="3a41b-176">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3a41b-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="3a41b-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a41b-177">NOTES</span></span>

## <span data-ttu-id="3a41b-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a41b-178">RELATED LINKS</span></span>

[<span data-ttu-id="3a41b-179">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3a41b-179">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="3a41b-180">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3a41b-180">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="3a41b-181">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="3a41b-181">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="3a41b-182">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="3a41b-182">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="3a41b-183">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3a41b-183">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)