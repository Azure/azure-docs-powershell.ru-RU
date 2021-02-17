---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 1f78630f195fca7e08ed755dbaeb48e413c8f8d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401017"
---
# <span data-ttu-id="d882a-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d882a-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="d882a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d882a-102">SYNOPSIS</span></span>
<span data-ttu-id="d882a-103">Создается новый объект в качестве backend.</span><span class="sxs-lookup"><span data-stu-id="d882a-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="d882a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d882a-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d882a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d882a-105">DESCRIPTION</span></span>
<span data-ttu-id="d882a-106">Создает новую организацию в управлении Api.</span><span class="sxs-lookup"><span data-stu-id="d882a-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="d882a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d882a-107">EXAMPLES</span></span>

### <span data-ttu-id="d882a-108">Создание backend 123 с помощью базовой схемы авторизации</span><span class="sxs-lookup"><span data-stu-id="d882a-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="d882a-109">Создание нового backend</span><span class="sxs-lookup"><span data-stu-id="d882a-109">Creates a new Backend</span></span>

## <span data-ttu-id="d882a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d882a-110">PARAMETERS</span></span>

### <span data-ttu-id="d882a-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="d882a-111">-BackendId</span></span>
<span data-ttu-id="d882a-112">Идентификатор нового backend.</span><span class="sxs-lookup"><span data-stu-id="d882a-112">Identifier of new backend.</span></span>
<span data-ttu-id="d882a-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d882a-113">This parameter is optional.</span></span>
<span data-ttu-id="d882a-114">Если он не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="d882a-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="d882a-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="d882a-115">-Context</span></span>
<span data-ttu-id="d882a-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d882a-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d882a-117">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="d882a-117">This parameter is required.</span></span>

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

### <span data-ttu-id="d882a-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="d882a-118">-Credential</span></span>
<span data-ttu-id="d882a-119">Учетные данные, которые следует использовать при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="d882a-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="d882a-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d882a-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="d882a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d882a-121">-DefaultProfile</span></span>
<span data-ttu-id="d882a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d882a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d882a-123">-Description</span><span class="sxs-lookup"><span data-stu-id="d882a-123">-Description</span></span>
<span data-ttu-id="d882a-124">Описание backend.</span><span class="sxs-lookup"><span data-stu-id="d882a-124">Backend Description.</span></span>
<span data-ttu-id="d882a-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d882a-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="d882a-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d882a-126">-Protocol</span></span>
<span data-ttu-id="d882a-127">Протокол Backend Communication (Протокол backend Communication).</span><span class="sxs-lookup"><span data-stu-id="d882a-127">Backend Communication protocol.</span></span>
<span data-ttu-id="d882a-128">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="d882a-128">This parameter is required.</span></span>
<span data-ttu-id="d882a-129">Допустимые значения: http и soap.</span><span class="sxs-lookup"><span data-stu-id="d882a-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="d882a-130">-Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="d882a-130">-Proxy</span></span>
<span data-ttu-id="d882a-131">Сведения прокси-сервера, которые будут использоваться при отправке запроса на сервер серверов.</span><span class="sxs-lookup"><span data-stu-id="d882a-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="d882a-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d882a-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="d882a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d882a-133">-ResourceId</span></span>
<span data-ttu-id="d882a-134">Uri управления ресурсом внешней системы.</span><span class="sxs-lookup"><span data-stu-id="d882a-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="d882a-135">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d882a-135">This parameter is optional.</span></span>
<span data-ttu-id="d882a-136">Этот URL-адрес может быть ид ресурса Arm приложений Logic, приложений для функций и приложений API.</span><span class="sxs-lookup"><span data-stu-id="d882a-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="d882a-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d882a-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="d882a-138">Сведения о структуре кластера "Сервис".</span><span class="sxs-lookup"><span data-stu-id="d882a-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="d882a-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d882a-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="d882a-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="d882a-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="d882a-141">Следует ли пропустить проверку цепочки сертификатов при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="d882a-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="d882a-142">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d882a-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="d882a-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="d882a-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="d882a-144">Следует ли пропускать проверку имени сертификата при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="d882a-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="d882a-145">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d882a-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="d882a-146">-Title</span><span class="sxs-lookup"><span data-stu-id="d882a-146">-Title</span></span>
<span data-ttu-id="d882a-147">Заголовок для backend.</span><span class="sxs-lookup"><span data-stu-id="d882a-147">Backend Title.</span></span>
<span data-ttu-id="d882a-148">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d882a-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="d882a-149">-URL-адрес</span><span class="sxs-lookup"><span data-stu-id="d882a-149">-Url</span></span>
<span data-ttu-id="d882a-150">URL-адрес времени запуска для backend.</span><span class="sxs-lookup"><span data-stu-id="d882a-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="d882a-151">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="d882a-151">This parameter is required.</span></span>

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

### <span data-ttu-id="d882a-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d882a-152">-Confirm</span></span>
<span data-ttu-id="d882a-153">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d882a-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d882a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d882a-154">-WhatIf</span></span>
<span data-ttu-id="d882a-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d882a-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d882a-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d882a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d882a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d882a-157">CommonParameters</span></span>
<span data-ttu-id="d882a-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d882a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d882a-159">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d882a-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d882a-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d882a-160">INPUTS</span></span>

### <span data-ttu-id="d882a-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d882a-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d882a-162">System.String</span><span class="sxs-lookup"><span data-stu-id="d882a-162">System.String</span></span>

### <span data-ttu-id="d882a-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d882a-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d882a-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d882a-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="d882a-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d882a-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="d882a-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d882a-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="d882a-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d882a-167">OUTPUTS</span></span>

### <span data-ttu-id="d882a-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d882a-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="d882a-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d882a-169">NOTES</span></span>

## <span data-ttu-id="d882a-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d882a-170">RELATED LINKS</span></span>

[<span data-ttu-id="d882a-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d882a-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="d882a-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d882a-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="d882a-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d882a-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="d882a-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d882a-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="d882a-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d882a-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

