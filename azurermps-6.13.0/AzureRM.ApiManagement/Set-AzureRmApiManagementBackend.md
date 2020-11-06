---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 52e159ae0f9d1b94b316394ddefe04f0bd8aa1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556923"
---
# <span data-ttu-id="1ef79-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1ef79-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="1ef79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ef79-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef79-103">Обновляет сервер.</span><span class="sxs-lookup"><span data-stu-id="1ef79-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ef79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ef79-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ef79-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ef79-105">DESCRIPTION</span></span>
<span data-ttu-id="1ef79-106">Обновляет существующую базу данных в управлении API.</span><span class="sxs-lookup"><span data-stu-id="1ef79-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="1ef79-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ef79-107">EXAMPLES</span></span>

### <span data-ttu-id="1ef79-108">Обновляет описание внутреннего сервера 123</span><span class="sxs-lookup"><span data-stu-id="1ef79-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="1ef79-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ef79-109">PARAMETERS</span></span>

### <span data-ttu-id="1ef79-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="1ef79-110">-BackendId</span></span>
<span data-ttu-id="1ef79-111">Идентификатор нового внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1ef79-111">Identifier of new backend.</span></span>
<span data-ttu-id="1ef79-112">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1ef79-112">This parameter is required.</span></span>

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

### <span data-ttu-id="1ef79-113">-Context</span><span class="sxs-lookup"><span data-stu-id="1ef79-113">-Context</span></span>
<span data-ttu-id="1ef79-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1ef79-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1ef79-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1ef79-115">This parameter is required.</span></span>

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

### <span data-ttu-id="1ef79-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="1ef79-116">-Credential</span></span>
<span data-ttu-id="1ef79-117">Сведения об учетных данных, которые следует использовать при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="1ef79-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="1ef79-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1ef79-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="1ef79-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef79-119">-DefaultProfile</span></span>
<span data-ttu-id="1ef79-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef79-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ef79-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="1ef79-121">-Description</span></span>
<span data-ttu-id="1ef79-122">Описание внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1ef79-122">Backend Description.</span></span>
<span data-ttu-id="1ef79-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1ef79-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="1ef79-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ef79-124">-PassThru</span></span>
<span data-ttu-id="1ef79-125">Указывает на то, что этот командлет возвращает  **PsApiManagementBackend** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="1ef79-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1ef79-126">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="1ef79-126">-Protocol</span></span>
<span data-ttu-id="1ef79-127">Внутренний протокол передачи данных (HTTP или SOAP).</span><span class="sxs-lookup"><span data-stu-id="1ef79-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="1ef79-128">Это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="1ef79-128">This parameter is optional</span></span>

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

### <span data-ttu-id="1ef79-129">-Прокси</span><span class="sxs-lookup"><span data-stu-id="1ef79-129">-Proxy</span></span>
<span data-ttu-id="1ef79-130">Сведения о прокси-сервере, которые необходимо использовать при отправке запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="1ef79-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="1ef79-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1ef79-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="1ef79-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ef79-132">-ResourceId</span></span>
<span data-ttu-id="1ef79-133">Универсальный код ресурса (URI) для управления ресурсом во внешней системе.</span><span class="sxs-lookup"><span data-stu-id="1ef79-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="1ef79-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1ef79-134">This parameter is optional.</span></span>
<span data-ttu-id="1ef79-135">Этот URL-адрес может представлять собой идентификатор ресурса ARM для логических приложений, приложений-функций или приложений API.</span><span class="sxs-lookup"><span data-stu-id="1ef79-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="1ef79-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="1ef79-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="1ef79-137">Сведения о внутреннем кластере кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="1ef79-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="1ef79-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1ef79-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="1ef79-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="1ef79-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="1ef79-140">Необходимость пропуска проверки цепочки сертификатов при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="1ef79-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="1ef79-141">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1ef79-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="1ef79-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="1ef79-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="1ef79-143">Следует ли пропускать проверку имени сертификата при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="1ef79-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="1ef79-144">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1ef79-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="1ef79-145">-Title</span><span class="sxs-lookup"><span data-stu-id="1ef79-145">-Title</span></span>
<span data-ttu-id="1ef79-146">Название внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1ef79-146">Backend Title.</span></span>
<span data-ttu-id="1ef79-147">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1ef79-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="1ef79-148">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="1ef79-148">-Url</span></span>
<span data-ttu-id="1ef79-149">URL-адрес среды выполнения для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1ef79-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="1ef79-150">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1ef79-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="1ef79-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ef79-151">-Confirm</span></span>
<span data-ttu-id="1ef79-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1ef79-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ef79-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ef79-153">-WhatIf</span></span>
<span data-ttu-id="1ef79-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1ef79-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ef79-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1ef79-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ef79-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef79-156">CommonParameters</span></span>
<span data-ttu-id="1ef79-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ef79-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef79-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef79-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef79-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ef79-159">INPUTS</span></span>

### <span data-ttu-id="1ef79-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1ef79-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1ef79-161">System. String</span><span class="sxs-lookup"><span data-stu-id="1ef79-161">System.String</span></span>

### <span data-ttu-id="1ef79-162">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1ef79-162">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1ef79-163">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1ef79-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="1ef79-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1ef79-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="1ef79-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1ef79-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="1ef79-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ef79-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1ef79-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ef79-167">OUTPUTS</span></span>

### <span data-ttu-id="1ef79-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1ef79-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="1ef79-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ef79-169">NOTES</span></span>

## <span data-ttu-id="1ef79-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ef79-170">RELATED LINKS</span></span>

[<span data-ttu-id="1ef79-171">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1ef79-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="1ef79-172">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1ef79-172">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="1ef79-173">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1ef79-173">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="1ef79-174">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1ef79-174">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="1ef79-175">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1ef79-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
