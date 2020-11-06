---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: b5e51891f82b2a12f42fac3a1535f974912ca1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565035"
---
# <span data-ttu-id="a4742-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4742-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="a4742-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4742-102">SYNOPSIS</span></span>
<span data-ttu-id="a4742-103">Обновляет сервер.</span><span class="sxs-lookup"><span data-stu-id="a4742-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4742-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4742-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4742-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4742-105">DESCRIPTION</span></span>
<span data-ttu-id="a4742-106">Обновляет существующую базу данных в управлении API.</span><span class="sxs-lookup"><span data-stu-id="a4742-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="a4742-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4742-107">EXAMPLES</span></span>

### <span data-ttu-id="a4742-108">Обновляет описание внутреннего сервера 123</span><span class="sxs-lookup"><span data-stu-id="a4742-108">Updates the Description of the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="a4742-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4742-109">PARAMETERS</span></span>

### <span data-ttu-id="a4742-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="a4742-110">-BackendId</span></span>
<span data-ttu-id="a4742-111">Идентификатор нового внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="a4742-111">Identifier of new backend.</span></span>
<span data-ttu-id="a4742-112">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a4742-112">This parameter is required.</span></span>

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

### <span data-ttu-id="a4742-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a4742-113">-Context</span></span>
<span data-ttu-id="a4742-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a4742-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a4742-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a4742-115">This parameter is required.</span></span>

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

### <span data-ttu-id="a4742-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="a4742-116">-Credential</span></span>
<span data-ttu-id="a4742-117">Сведения об учетных данных, которые следует использовать при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="a4742-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="a4742-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a4742-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4742-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4742-119">-DefaultProfile</span></span>
<span data-ttu-id="a4742-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4742-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a4742-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="a4742-121">-Description</span></span>
<span data-ttu-id="a4742-122">Описание внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="a4742-122">Backend Description.</span></span>
<span data-ttu-id="a4742-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a4742-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4742-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4742-124">-PassThru</span></span>
<span data-ttu-id="a4742-125">Указывает на то, что этот командлет возвращает  **PsApiManagementBackend** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a4742-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4742-126">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="a4742-126">-Protocol</span></span>
<span data-ttu-id="a4742-127">Внутренний протокол передачи данных (HTTP или SOAP).</span><span class="sxs-lookup"><span data-stu-id="a4742-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="a4742-128">Это необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="a4742-128">This parameter is optional</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4742-129">-Прокси</span><span class="sxs-lookup"><span data-stu-id="a4742-129">-Proxy</span></span>
<span data-ttu-id="a4742-130">Сведения о прокси-сервере, которые необходимо использовать при отправке запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="a4742-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="a4742-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a4742-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4742-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4742-132">-ResourceId</span></span>
<span data-ttu-id="a4742-133">Универсальный код ресурса (URI) для управления ресурсом во внешней системе.</span><span class="sxs-lookup"><span data-stu-id="a4742-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="a4742-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a4742-134">This parameter is optional.</span></span>
<span data-ttu-id="a4742-135">Этот URL-адрес может представлять собой идентификатор ресурса ARM для логических приложений, приложений-функций или приложений API.</span><span class="sxs-lookup"><span data-stu-id="a4742-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="a4742-136">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="a4742-136">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="a4742-137">Необходимость пропуска проверки цепочки сертификатов при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="a4742-137">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="a4742-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a4742-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4742-139">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="a4742-139">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="a4742-140">Следует ли пропускать проверку имени сертификата при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="a4742-140">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="a4742-141">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a4742-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4742-142">-Title</span><span class="sxs-lookup"><span data-stu-id="a4742-142">-Title</span></span>
<span data-ttu-id="a4742-143">Название внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="a4742-143">Backend Title.</span></span>
<span data-ttu-id="a4742-144">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a4742-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4742-145">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="a4742-145">-Url</span></span>
<span data-ttu-id="a4742-146">URL-адрес среды выполнения для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="a4742-146">Runtime Url for the Backend.</span></span>
<span data-ttu-id="a4742-147">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a4742-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="a4742-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4742-148">-Confirm</span></span>
<span data-ttu-id="a4742-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4742-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4742-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4742-150">-WhatIf</span></span>
<span data-ttu-id="a4742-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4742-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4742-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4742-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4742-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4742-153">CommonParameters</span></span>
<span data-ttu-id="a4742-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4742-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4742-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4742-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4742-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4742-156">INPUTS</span></span>

### <span data-ttu-id="a4742-157">Ничего</span><span class="sxs-lookup"><span data-stu-id="a4742-157">None</span></span>
<span data-ttu-id="a4742-158">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a4742-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4742-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4742-159">OUTPUTS</span></span>

### <span data-ttu-id="a4742-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4742-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="a4742-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4742-161">NOTES</span></span>

## <span data-ttu-id="a4742-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4742-162">RELATED LINKS</span></span>

[<span data-ttu-id="a4742-163">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4742-163">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="a4742-164">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4742-164">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="a4742-165">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a4742-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="a4742-166">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a4742-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="a4742-167">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a4742-167">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
