---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: ce27a151ebb6d778ed647fb81909c44c11edbf8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901586"
---
# <span data-ttu-id="7d414-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7d414-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="7d414-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d414-102">SYNOPSIS</span></span>
<span data-ttu-id="7d414-103">Обновляет сервер.</span><span class="sxs-lookup"><span data-stu-id="7d414-103">Updates a Backend.</span></span>

## <span data-ttu-id="7d414-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d414-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d414-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d414-105">DESCRIPTION</span></span>
<span data-ttu-id="7d414-106">Обновляет существующую базу данных в управлении API.</span><span class="sxs-lookup"><span data-stu-id="7d414-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="7d414-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d414-107">EXAMPLES</span></span>

### <span data-ttu-id="7d414-108">Обновляет описание внутреннего сервера 123</span><span class="sxs-lookup"><span data-stu-id="7d414-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="7d414-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d414-109">PARAMETERS</span></span>

### <span data-ttu-id="7d414-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="7d414-110">-BackendId</span></span>
<span data-ttu-id="7d414-111">Идентификатор нового внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="7d414-111">Identifier of new backend.</span></span>
<span data-ttu-id="7d414-112">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="7d414-112">This parameter is required.</span></span>

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

### <span data-ttu-id="7d414-113">-Context</span><span class="sxs-lookup"><span data-stu-id="7d414-113">-Context</span></span>
<span data-ttu-id="7d414-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7d414-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7d414-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="7d414-115">This parameter is required.</span></span>

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

### <span data-ttu-id="7d414-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="7d414-116">-Credential</span></span>
<span data-ttu-id="7d414-117">Сведения об учетных данных, которые следует использовать при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="7d414-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="7d414-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7d414-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d414-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d414-119">-DefaultProfile</span></span>
<span data-ttu-id="7d414-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d414-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d414-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="7d414-121">-Description</span></span>
<span data-ttu-id="7d414-122">Описание внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="7d414-122">Backend Description.</span></span>
<span data-ttu-id="7d414-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7d414-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d414-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d414-124">-PassThru</span></span>
<span data-ttu-id="7d414-125">Указывает на то, что этот командлет возвращает  **PsApiManagementBackend** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7d414-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7d414-126">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="7d414-126">-Protocol</span></span>
<span data-ttu-id="7d414-127">Внутренний протокол передачи данных (HTTP или SOAP).</span><span class="sxs-lookup"><span data-stu-id="7d414-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="7d414-128">Это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="7d414-128">This parameter is optional</span></span>

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

### <span data-ttu-id="7d414-129">-Прокси</span><span class="sxs-lookup"><span data-stu-id="7d414-129">-Proxy</span></span>
<span data-ttu-id="7d414-130">Сведения о прокси-сервере, которые необходимо использовать при отправке запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="7d414-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="7d414-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7d414-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d414-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d414-132">-ResourceId</span></span>
<span data-ttu-id="7d414-133">Универсальный код ресурса (URI) для управления ресурсом во внешней системе.</span><span class="sxs-lookup"><span data-stu-id="7d414-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="7d414-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7d414-134">This parameter is optional.</span></span>
<span data-ttu-id="7d414-135">Этот URL-адрес может представлять собой идентификатор ресурса ARM для логических приложений, приложений-функций или приложений API.</span><span class="sxs-lookup"><span data-stu-id="7d414-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="7d414-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="7d414-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="7d414-137">Сведения о внутреннем кластере кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="7d414-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="7d414-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7d414-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d414-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="7d414-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="7d414-140">Необходимость пропуска проверки цепочки сертификатов при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="7d414-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="7d414-141">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7d414-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d414-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="7d414-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="7d414-143">Следует ли пропускать проверку имени сертификата при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="7d414-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="7d414-144">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7d414-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d414-145">-Title</span><span class="sxs-lookup"><span data-stu-id="7d414-145">-Title</span></span>
<span data-ttu-id="7d414-146">Название внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="7d414-146">Backend Title.</span></span>
<span data-ttu-id="7d414-147">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7d414-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d414-148">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="7d414-148">-Url</span></span>
<span data-ttu-id="7d414-149">URL-адрес среды выполнения для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="7d414-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="7d414-150">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7d414-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="7d414-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d414-151">-Confirm</span></span>
<span data-ttu-id="7d414-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d414-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d414-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d414-153">-WhatIf</span></span>
<span data-ttu-id="7d414-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d414-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d414-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d414-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d414-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d414-156">CommonParameters</span></span>
<span data-ttu-id="7d414-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d414-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d414-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d414-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d414-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d414-159">INPUTS</span></span>

### <span data-ttu-id="7d414-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7d414-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7d414-161">System. String</span><span class="sxs-lookup"><span data-stu-id="7d414-161">System.String</span></span>

### <span data-ttu-id="7d414-162">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7d414-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7d414-163">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7d414-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="7d414-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7d414-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="7d414-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d414-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="7d414-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7d414-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7d414-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d414-167">OUTPUTS</span></span>

### <span data-ttu-id="7d414-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7d414-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="7d414-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d414-169">NOTES</span></span>

## <span data-ttu-id="7d414-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d414-170">RELATED LINKS</span></span>

[<span data-ttu-id="7d414-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7d414-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="7d414-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7d414-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="7d414-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="7d414-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="7d414-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="7d414-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="7d414-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="7d414-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
