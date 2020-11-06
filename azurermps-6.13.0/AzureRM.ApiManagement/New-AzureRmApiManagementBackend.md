---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 46e0a864bcedd8ac0c23761545f5480eaa4a093a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561239"
---
# <span data-ttu-id="d4afc-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d4afc-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="d4afc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4afc-102">SYNOPSIS</span></span>
<span data-ttu-id="d4afc-103">Создание новой серверной сущности.</span><span class="sxs-lookup"><span data-stu-id="d4afc-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4afc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4afc-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4afc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4afc-105">DESCRIPTION</span></span>
<span data-ttu-id="d4afc-106">Создает новую серверную сущность в управлении API.</span><span class="sxs-lookup"><span data-stu-id="d4afc-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="d4afc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4afc-107">EXAMPLES</span></span>

### <span data-ttu-id="d4afc-108">Создание внутренних 123 с помощью базовой схемы авторизации</span><span class="sxs-lookup"><span data-stu-id="d4afc-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="d4afc-109">Создание новой базы данных</span><span class="sxs-lookup"><span data-stu-id="d4afc-109">Creates a new Backend</span></span>

## <span data-ttu-id="d4afc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4afc-110">PARAMETERS</span></span>

### <span data-ttu-id="d4afc-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="d4afc-111">-BackendId</span></span>
<span data-ttu-id="d4afc-112">Идентификатор нового внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="d4afc-112">Identifier of new backend.</span></span>
<span data-ttu-id="d4afc-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-113">This parameter is optional.</span></span>
<span data-ttu-id="d4afc-114">Если не указано, будет создано.</span><span class="sxs-lookup"><span data-stu-id="d4afc-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="d4afc-115">-Context</span><span class="sxs-lookup"><span data-stu-id="d4afc-115">-Context</span></span>
<span data-ttu-id="d4afc-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d4afc-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d4afc-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-117">This parameter is required.</span></span>

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

### <span data-ttu-id="d4afc-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="d4afc-118">-Credential</span></span>
<span data-ttu-id="d4afc-119">Сведения об учетных данных, которые следует использовать при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="d4afc-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="d4afc-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="d4afc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4afc-121">-DefaultProfile</span></span>
<span data-ttu-id="d4afc-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4afc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4afc-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="d4afc-123">-Description</span></span>
<span data-ttu-id="d4afc-124">Описание внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="d4afc-124">Backend Description.</span></span>
<span data-ttu-id="d4afc-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="d4afc-126">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="d4afc-126">-Protocol</span></span>
<span data-ttu-id="d4afc-127">Внутренний протокол связи.</span><span class="sxs-lookup"><span data-stu-id="d4afc-127">Backend Communication protocol.</span></span>
<span data-ttu-id="d4afc-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-128">This parameter is required.</span></span>
<span data-ttu-id="d4afc-129">Допустимые значения: "http" и "SOAP".</span><span class="sxs-lookup"><span data-stu-id="d4afc-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="d4afc-130">-Прокси</span><span class="sxs-lookup"><span data-stu-id="d4afc-130">-Proxy</span></span>
<span data-ttu-id="d4afc-131">Сведения о прокси-сервере, которые необходимо использовать при отправке запроса на сервер.</span><span class="sxs-lookup"><span data-stu-id="d4afc-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="d4afc-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="d4afc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4afc-133">-ResourceId</span></span>
<span data-ttu-id="d4afc-134">Универсальный код ресурса (URI) для управления ресурсом во внешней системе.</span><span class="sxs-lookup"><span data-stu-id="d4afc-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="d4afc-135">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-135">This parameter is optional.</span></span>
<span data-ttu-id="d4afc-136">Этот URL-адрес может представлять собой идентификатор ресурса ARM для логических приложений, приложений-функций или приложений API.</span><span class="sxs-lookup"><span data-stu-id="d4afc-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="d4afc-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d4afc-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="d4afc-138">Сведения о внутреннем кластере кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="d4afc-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="d4afc-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="d4afc-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="d4afc-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="d4afc-141">Необходимость пропуска проверки цепочки сертификатов при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="d4afc-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="d4afc-142">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="d4afc-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="d4afc-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="d4afc-144">Следует ли пропускать проверку имени сертификата при общении с серверным сервером.</span><span class="sxs-lookup"><span data-stu-id="d4afc-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="d4afc-145">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="d4afc-146">-Title</span><span class="sxs-lookup"><span data-stu-id="d4afc-146">-Title</span></span>
<span data-ttu-id="d4afc-147">Название внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="d4afc-147">Backend Title.</span></span>
<span data-ttu-id="d4afc-148">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="d4afc-149">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="d4afc-149">-Url</span></span>
<span data-ttu-id="d4afc-150">URL-адрес среды выполнения для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="d4afc-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="d4afc-151">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d4afc-151">This parameter is required.</span></span>

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

### <span data-ttu-id="d4afc-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4afc-152">-Confirm</span></span>
<span data-ttu-id="d4afc-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d4afc-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4afc-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4afc-154">-WhatIf</span></span>
<span data-ttu-id="d4afc-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d4afc-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4afc-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4afc-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4afc-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4afc-157">CommonParameters</span></span>
<span data-ttu-id="d4afc-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4afc-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4afc-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4afc-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4afc-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4afc-160">INPUTS</span></span>

### <span data-ttu-id="d4afc-161">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d4afc-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d4afc-162">System. String</span><span class="sxs-lookup"><span data-stu-id="d4afc-162">System.String</span></span>

### <span data-ttu-id="d4afc-163">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d4afc-163">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d4afc-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d4afc-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="d4afc-165">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d4afc-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="d4afc-166">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d4afc-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="d4afc-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4afc-167">OUTPUTS</span></span>

### <span data-ttu-id="d4afc-168">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d4afc-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="d4afc-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4afc-169">NOTES</span></span>

## <span data-ttu-id="d4afc-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4afc-170">RELATED LINKS</span></span>

[<span data-ttu-id="d4afc-171">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d4afc-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="d4afc-172">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d4afc-172">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="d4afc-173">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d4afc-173">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="d4afc-174">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d4afc-174">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d4afc-175">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d4afc-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

