---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 85545777f5a76f3f75e81648a009ffcdcad8ab30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734279"
---
# <span data-ttu-id="3869f-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3869f-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="3869f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3869f-102">SYNOPSIS</span></span>
<span data-ttu-id="3869f-103">Обновляет сервер.</span><span class="sxs-lookup"><span data-stu-id="3869f-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3869f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3869f-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3869f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3869f-105">DESCRIPTION</span></span>
<span data-ttu-id="3869f-106">Обновляет существующую базу данных в управлении API.</span><span class="sxs-lookup"><span data-stu-id="3869f-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="3869f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3869f-107">EXAMPLES</span></span>

### <span data-ttu-id="3869f-108">Обновляет описание внутреннего сервера 123</span><span class="sxs-lookup"><span data-stu-id="3869f-108">Updates the Description of the Backend 123</span></span>
```
Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="3869f-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3869f-109">PARAMETERS</span></span>

### <span data-ttu-id="3869f-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="3869f-110">-BackendId</span></span>
<span data-ttu-id="3869f-111">Идентификатор нового внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="3869f-111">Identifier of new backend.</span></span>
<span data-ttu-id="3869f-112">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3869f-112">This parameter is required.</span></span>

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

### <span data-ttu-id="3869f-113">-Context</span><span class="sxs-lookup"><span data-stu-id="3869f-113">-Context</span></span>
<span data-ttu-id="3869f-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3869f-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3869f-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3869f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="3869f-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="3869f-116">-Credential</span></span>
<span data-ttu-id="3869f-117">Сведения об учетных данных, которые следует использовать при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="3869f-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="3869f-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3869f-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="3869f-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="3869f-119">-Description</span></span>
<span data-ttu-id="3869f-120">Описание внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="3869f-120">Backend Description.</span></span>
<span data-ttu-id="3869f-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3869f-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="3869f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3869f-122">-PassThru</span></span>
<span data-ttu-id="3869f-123">Указывает на то, что этот командлет возвращает  **PsApiManagementBackend** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3869f-123">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3869f-124">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="3869f-124">-Protocol</span></span>
<span data-ttu-id="3869f-125">Внутренний протокол передачи данных (HTTP или SOAP).</span><span class="sxs-lookup"><span data-stu-id="3869f-125">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="3869f-126">Это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="3869f-126">This parameter is optional</span></span>

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

### <span data-ttu-id="3869f-127">-Прокси</span><span class="sxs-lookup"><span data-stu-id="3869f-127">-Proxy</span></span>
<span data-ttu-id="3869f-128">Сведения о прокси-сервере, которые необходимо использовать при отправке запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="3869f-128">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="3869f-129">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3869f-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="3869f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3869f-130">-ResourceId</span></span>
<span data-ttu-id="3869f-131">Универсальный код ресурса (URI) для управления ресурсом во внешней системе.</span><span class="sxs-lookup"><span data-stu-id="3869f-131">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="3869f-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3869f-132">This parameter is optional.</span></span>
<span data-ttu-id="3869f-133">Этот URL-адрес может представлять собой идентификатор ресурса ARM для логических приложений, приложений-функций или приложений API.</span><span class="sxs-lookup"><span data-stu-id="3869f-133">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="3869f-134">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="3869f-134">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="3869f-135">Необходимость пропуска проверки цепочки сертификатов при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="3869f-135">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="3869f-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3869f-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="3869f-137">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="3869f-137">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="3869f-138">Следует ли пропускать проверку имени сертификата при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="3869f-138">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="3869f-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3869f-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="3869f-140">-Title</span><span class="sxs-lookup"><span data-stu-id="3869f-140">-Title</span></span>
<span data-ttu-id="3869f-141">Название внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="3869f-141">Backend Title.</span></span>
<span data-ttu-id="3869f-142">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3869f-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="3869f-143">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="3869f-143">-Url</span></span>
<span data-ttu-id="3869f-144">URL-адрес среды выполнения для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="3869f-144">Runtime Url for the Backend.</span></span>
<span data-ttu-id="3869f-145">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3869f-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="3869f-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3869f-146">-Confirm</span></span>
<span data-ttu-id="3869f-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3869f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3869f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3869f-148">-WhatIf</span></span>
<span data-ttu-id="3869f-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3869f-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3869f-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3869f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3869f-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3869f-151">-DefaultProfile</span></span>
<span data-ttu-id="3869f-152">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3869f-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3869f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3869f-153">CommonParameters</span></span>
<span data-ttu-id="3869f-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3869f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3869f-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3869f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3869f-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3869f-156">INPUTS</span></span>

## <span data-ttu-id="3869f-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3869f-157">OUTPUTS</span></span>

### <span data-ttu-id="3869f-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3869f-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="3869f-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="3869f-159">NOTES</span></span>

## <span data-ttu-id="3869f-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3869f-160">RELATED LINKS</span></span>

[<span data-ttu-id="3869f-161">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3869f-161">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="3869f-162">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3869f-162">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="3869f-163">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="3869f-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="3869f-164">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="3869f-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="3869f-165">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3869f-165">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
