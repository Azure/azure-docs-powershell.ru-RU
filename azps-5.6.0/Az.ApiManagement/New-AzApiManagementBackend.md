---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: ba528724bebfc6ce3400ead69a223e08f42663ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010947"
---
# <span data-ttu-id="9d807-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9d807-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="9d807-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d807-102">SYNOPSIS</span></span>
<span data-ttu-id="9d807-103">Создается новый объект в качестве backend.</span><span class="sxs-lookup"><span data-stu-id="9d807-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="9d807-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d807-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d807-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d807-105">DESCRIPTION</span></span>
<span data-ttu-id="9d807-106">Создает новую организацию в управлении Api.</span><span class="sxs-lookup"><span data-stu-id="9d807-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="9d807-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d807-107">EXAMPLES</span></span>

### <span data-ttu-id="9d807-108">Пример 1. Создание backend 123 с помощью базовой схемы авторизации</span><span class="sxs-lookup"><span data-stu-id="9d807-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="9d807-109">Создание нового backend</span><span class="sxs-lookup"><span data-stu-id="9d807-109">Creates a new Backend</span></span>

## <span data-ttu-id="9d807-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d807-110">PARAMETERS</span></span>

### <span data-ttu-id="9d807-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="9d807-111">-BackendId</span></span>
<span data-ttu-id="9d807-112">Идентификатор нового backend.</span><span class="sxs-lookup"><span data-stu-id="9d807-112">Identifier of new backend.</span></span>
<span data-ttu-id="9d807-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9d807-113">This parameter is optional.</span></span>
<span data-ttu-id="9d807-114">Если он не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="9d807-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="9d807-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="9d807-115">-Context</span></span>
<span data-ttu-id="9d807-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9d807-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9d807-117">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9d807-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d807-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="9d807-118">-Credential</span></span>
<span data-ttu-id="9d807-119">Учетные данные, которые следует использовать при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="9d807-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="9d807-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9d807-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d807-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d807-121">-DefaultProfile</span></span>
<span data-ttu-id="9d807-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d807-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d807-123">-Description</span><span class="sxs-lookup"><span data-stu-id="9d807-123">-Description</span></span>
<span data-ttu-id="9d807-124">Описание backend.</span><span class="sxs-lookup"><span data-stu-id="9d807-124">Backend Description.</span></span>
<span data-ttu-id="9d807-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9d807-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d807-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9d807-126">-Protocol</span></span>
<span data-ttu-id="9d807-127">Протокол Backend Communication (Протокол backend Communication).</span><span class="sxs-lookup"><span data-stu-id="9d807-127">Backend Communication protocol.</span></span>
<span data-ttu-id="9d807-128">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9d807-128">This parameter is required.</span></span>
<span data-ttu-id="9d807-129">Допустимые значения: http и soap.</span><span class="sxs-lookup"><span data-stu-id="9d807-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="9d807-130">-Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="9d807-130">-Proxy</span></span>
<span data-ttu-id="9d807-131">Сведения прокси-сервера, которые будут использоваться при отправке запроса на сервер серверов.</span><span class="sxs-lookup"><span data-stu-id="9d807-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="9d807-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9d807-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d807-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d807-133">-ResourceId</span></span>
<span data-ttu-id="9d807-134">Uri управления ресурсом внешней системы.</span><span class="sxs-lookup"><span data-stu-id="9d807-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="9d807-135">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9d807-135">This parameter is optional.</span></span>
<span data-ttu-id="9d807-136">Этот URL-адрес может быть ид ресурса Arm приложений Logic, приложений function или API.</span><span class="sxs-lookup"><span data-stu-id="9d807-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="9d807-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="9d807-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="9d807-138">Сведения о структуре кластера "Сервис".</span><span class="sxs-lookup"><span data-stu-id="9d807-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="9d807-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9d807-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d807-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="9d807-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="9d807-141">Следует ли пропустить проверку цепочки сертификатов при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="9d807-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="9d807-142">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9d807-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d807-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="9d807-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="9d807-144">Следует ли пропускать проверку имени сертификата при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="9d807-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="9d807-145">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9d807-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d807-146">-Title</span><span class="sxs-lookup"><span data-stu-id="9d807-146">-Title</span></span>
<span data-ttu-id="9d807-147">Заголовок для backend.</span><span class="sxs-lookup"><span data-stu-id="9d807-147">Backend Title.</span></span>
<span data-ttu-id="9d807-148">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9d807-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="9d807-149">-URL-адрес</span><span class="sxs-lookup"><span data-stu-id="9d807-149">-Url</span></span>
<span data-ttu-id="9d807-150">URL-адрес времени запуска для backend.</span><span class="sxs-lookup"><span data-stu-id="9d807-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="9d807-151">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9d807-151">This parameter is required.</span></span>

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

### <span data-ttu-id="9d807-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d807-152">-Confirm</span></span>
<span data-ttu-id="9d807-153">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d807-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d807-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d807-154">-WhatIf</span></span>
<span data-ttu-id="9d807-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d807-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d807-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9d807-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d807-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d807-157">CommonParameters</span></span>
<span data-ttu-id="9d807-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d807-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d807-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d807-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d807-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d807-160">INPUTS</span></span>

### <span data-ttu-id="9d807-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9d807-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9d807-162">System.String</span><span class="sxs-lookup"><span data-stu-id="9d807-162">System.String</span></span>

### <span data-ttu-id="9d807-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9d807-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9d807-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="9d807-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="9d807-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="9d807-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="9d807-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9d807-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="9d807-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d807-167">OUTPUTS</span></span>

### <span data-ttu-id="9d807-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9d807-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="9d807-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d807-169">NOTES</span></span>

## <span data-ttu-id="9d807-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d807-170">RELATED LINKS</span></span>

[<span data-ttu-id="9d807-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9d807-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="9d807-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="9d807-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="9d807-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="9d807-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="9d807-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9d807-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="9d807-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9d807-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

