---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 144830c2155379683c8568eda6e0d1bc021b38fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565743"
---
# <span data-ttu-id="c47d6-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c47d6-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="c47d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c47d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c47d6-103">Создание новой серверной сущности.</span><span class="sxs-lookup"><span data-stu-id="c47d6-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c47d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c47d6-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c47d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c47d6-105">DESCRIPTION</span></span>
<span data-ttu-id="c47d6-106">Создает новую серверную сущность в управлении API.</span><span class="sxs-lookup"><span data-stu-id="c47d6-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="c47d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c47d6-107">EXAMPLES</span></span>

### <span data-ttu-id="c47d6-108">Создание внутренних 123 с помощью базовой схемы авторизации</span><span class="sxs-lookup"><span data-stu-id="c47d6-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="c47d6-109">Создание новой базы данных</span><span class="sxs-lookup"><span data-stu-id="c47d6-109">Creates a new Backend</span></span>

## <span data-ttu-id="c47d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c47d6-110">PARAMETERS</span></span>

### <span data-ttu-id="c47d6-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="c47d6-111">-BackendId</span></span>
<span data-ttu-id="c47d6-112">Идентификатор нового внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="c47d6-112">Identifier of new backend.</span></span>
<span data-ttu-id="c47d6-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c47d6-113">This parameter is optional.</span></span>
<span data-ttu-id="c47d6-114">Если не указано, будет создано.</span><span class="sxs-lookup"><span data-stu-id="c47d6-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="c47d6-115">-Context</span><span class="sxs-lookup"><span data-stu-id="c47d6-115">-Context</span></span>
<span data-ttu-id="c47d6-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c47d6-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c47d6-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c47d6-117">This parameter is required.</span></span>

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

### <span data-ttu-id="c47d6-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="c47d6-118">-Credential</span></span>
<span data-ttu-id="c47d6-119">Сведения об учетных данных, которые следует использовать при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="c47d6-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="c47d6-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c47d6-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="c47d6-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="c47d6-121">-Description</span></span>
<span data-ttu-id="c47d6-122">Описание внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="c47d6-122">Backend Description.</span></span>
<span data-ttu-id="c47d6-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c47d6-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="c47d6-124">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="c47d6-124">-Protocol</span></span>
<span data-ttu-id="c47d6-125">Внутренний протокол связи.</span><span class="sxs-lookup"><span data-stu-id="c47d6-125">Backend Communication protocol.</span></span>
<span data-ttu-id="c47d6-126">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c47d6-126">This parameter is required.</span></span>
<span data-ttu-id="c47d6-127">Допустимые значения: "http" и "SOAP".</span><span class="sxs-lookup"><span data-stu-id="c47d6-127">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="c47d6-128">-Прокси</span><span class="sxs-lookup"><span data-stu-id="c47d6-128">-Proxy</span></span>
<span data-ttu-id="c47d6-129">Сведения о прокси-сервере, которые необходимо использовать при отправке запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="c47d6-129">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="c47d6-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c47d6-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="c47d6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c47d6-131">-ResourceId</span></span>
<span data-ttu-id="c47d6-132">Универсальный код ресурса (URI) для управления ресурсом во внешней системе.</span><span class="sxs-lookup"><span data-stu-id="c47d6-132">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="c47d6-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c47d6-133">This parameter is optional.</span></span>
<span data-ttu-id="c47d6-134">Этот URL-адрес может представлять собой идентификатор ресурса ARM для логических приложений, приложений-функций или приложений API.</span><span class="sxs-lookup"><span data-stu-id="c47d6-134">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="c47d6-135">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="c47d6-135">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="c47d6-136">Необходимость пропуска проверки цепочки сертификатов при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="c47d6-136">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="c47d6-137">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c47d6-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="c47d6-138">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="c47d6-138">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="c47d6-139">Следует ли пропускать проверку имени сертификата при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="c47d6-139">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="c47d6-140">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c47d6-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="c47d6-141">-Title</span><span class="sxs-lookup"><span data-stu-id="c47d6-141">-Title</span></span>
<span data-ttu-id="c47d6-142">Название внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="c47d6-142">Backend Title.</span></span>
<span data-ttu-id="c47d6-143">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c47d6-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="c47d6-144">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="c47d6-144">-Url</span></span>
<span data-ttu-id="c47d6-145">URL-адрес среды выполнения для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="c47d6-145">Runtime Url for the Backend.</span></span>
<span data-ttu-id="c47d6-146">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c47d6-146">This parameter is required.</span></span>

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

### <span data-ttu-id="c47d6-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c47d6-147">-Confirm</span></span>
<span data-ttu-id="c47d6-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c47d6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c47d6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c47d6-149">-WhatIf</span></span>
<span data-ttu-id="c47d6-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c47d6-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c47d6-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c47d6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c47d6-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c47d6-152">-DefaultProfile</span></span>
<span data-ttu-id="c47d6-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c47d6-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c47d6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c47d6-154">CommonParameters</span></span>
<span data-ttu-id="c47d6-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c47d6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c47d6-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c47d6-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c47d6-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c47d6-157">INPUTS</span></span>

## <span data-ttu-id="c47d6-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c47d6-158">OUTPUTS</span></span>

### <span data-ttu-id="c47d6-159">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c47d6-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="c47d6-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="c47d6-160">NOTES</span></span>

## <span data-ttu-id="c47d6-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c47d6-161">RELATED LINKS</span></span>

[<span data-ttu-id="c47d6-162">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c47d6-162">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="c47d6-163">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="c47d6-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="c47d6-164">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="c47d6-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="c47d6-165">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c47d6-165">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="c47d6-166">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c47d6-166">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

