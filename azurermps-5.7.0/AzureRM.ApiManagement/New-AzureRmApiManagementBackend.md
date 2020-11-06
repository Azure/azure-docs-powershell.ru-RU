---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: c337e82c88c7fdbbc1f8a3663249126c9d92b19f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569103"
---
# <span data-ttu-id="5796b-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5796b-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="5796b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5796b-102">SYNOPSIS</span></span>
<span data-ttu-id="5796b-103">Создание новой серверной сущности.</span><span class="sxs-lookup"><span data-stu-id="5796b-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5796b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5796b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5796b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5796b-105">DESCRIPTION</span></span>
<span data-ttu-id="5796b-106">Создает новую серверную сущность в управлении API.</span><span class="sxs-lookup"><span data-stu-id="5796b-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="5796b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5796b-107">EXAMPLES</span></span>

### <span data-ttu-id="5796b-108">Создание внутренних 123 с помощью базовой схемы авторизации</span><span class="sxs-lookup"><span data-stu-id="5796b-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="5796b-109">Создание новой базы данных</span><span class="sxs-lookup"><span data-stu-id="5796b-109">Creates a new Backend</span></span>

## <span data-ttu-id="5796b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5796b-110">PARAMETERS</span></span>

### <span data-ttu-id="5796b-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="5796b-111">-BackendId</span></span>
<span data-ttu-id="5796b-112">Идентификатор нового внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="5796b-112">Identifier of new backend.</span></span>
<span data-ttu-id="5796b-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5796b-113">This parameter is optional.</span></span>
<span data-ttu-id="5796b-114">Если не указано, будет создано.</span><span class="sxs-lookup"><span data-stu-id="5796b-114">If not specified will be generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-115">-Context</span><span class="sxs-lookup"><span data-stu-id="5796b-115">-Context</span></span>
<span data-ttu-id="5796b-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5796b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5796b-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="5796b-117">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="5796b-118">-Credential</span></span>
<span data-ttu-id="5796b-119">Сведения об учетных данных, которые следует использовать при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="5796b-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="5796b-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5796b-120">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5796b-121">-DefaultProfile</span></span>
<span data-ttu-id="5796b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5796b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="5796b-123">-Description</span></span>
<span data-ttu-id="5796b-124">Описание внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="5796b-124">Backend Description.</span></span>
<span data-ttu-id="5796b-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5796b-125">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-126">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="5796b-126">-Protocol</span></span>
<span data-ttu-id="5796b-127">Внутренний протокол связи.</span><span class="sxs-lookup"><span data-stu-id="5796b-127">Backend Communication protocol.</span></span>
<span data-ttu-id="5796b-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="5796b-128">This parameter is required.</span></span>
<span data-ttu-id="5796b-129">Допустимые значения: "http" и "SOAP".</span><span class="sxs-lookup"><span data-stu-id="5796b-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-130">-Прокси</span><span class="sxs-lookup"><span data-stu-id="5796b-130">-Proxy</span></span>
<span data-ttu-id="5796b-131">Сведения о прокси-сервере, которые необходимо использовать при отправке запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="5796b-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="5796b-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5796b-132">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5796b-133">-ResourceId</span></span>
<span data-ttu-id="5796b-134">Универсальный код ресурса (URI) для управления ресурсом во внешней системе.</span><span class="sxs-lookup"><span data-stu-id="5796b-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="5796b-135">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5796b-135">This parameter is optional.</span></span>
<span data-ttu-id="5796b-136">Этот URL-адрес может представлять собой идентификатор ресурса ARM для логических приложений, приложений-функций или приложений API.</span><span class="sxs-lookup"><span data-stu-id="5796b-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-137">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="5796b-137">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="5796b-138">Необходимость пропуска проверки цепочки сертификатов при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="5796b-138">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="5796b-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5796b-139">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-140">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="5796b-140">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="5796b-141">Следует ли пропускать проверку имени сертификата при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="5796b-141">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="5796b-142">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5796b-142">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-143">-Title</span><span class="sxs-lookup"><span data-stu-id="5796b-143">-Title</span></span>
<span data-ttu-id="5796b-144">Название внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="5796b-144">Backend Title.</span></span>
<span data-ttu-id="5796b-145">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5796b-145">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-146">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="5796b-146">-Url</span></span>
<span data-ttu-id="5796b-147">URL-адрес среды выполнения для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="5796b-147">Runtime Url for the Backend.</span></span>
<span data-ttu-id="5796b-148">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="5796b-148">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5796b-149">-Confirm</span></span>
<span data-ttu-id="5796b-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5796b-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5796b-151">-WhatIf</span></span>
<span data-ttu-id="5796b-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5796b-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5796b-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5796b-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5796b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5796b-154">CommonParameters</span></span>
<span data-ttu-id="5796b-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5796b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5796b-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5796b-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5796b-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5796b-157">INPUTS</span></span>

### <span data-ttu-id="5796b-158">Ничего</span><span class="sxs-lookup"><span data-stu-id="5796b-158">None</span></span>
<span data-ttu-id="5796b-159">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5796b-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5796b-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5796b-160">OUTPUTS</span></span>

### <span data-ttu-id="5796b-161">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5796b-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="5796b-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="5796b-162">NOTES</span></span>

## <span data-ttu-id="5796b-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5796b-163">RELATED LINKS</span></span>

[<span data-ttu-id="5796b-164">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5796b-164">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="5796b-165">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="5796b-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="5796b-166">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="5796b-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="5796b-167">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5796b-167">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="5796b-168">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5796b-168">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

