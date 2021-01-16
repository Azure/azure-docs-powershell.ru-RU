---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 4ed63d0e3b801572698b123038a2022e89672a88
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409863"
---
# <span data-ttu-id="9a2e9-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9a2e9-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="9a2e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="9a2e9-103">Создание новой объектной структуры.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="9a2e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a2e9-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a2e9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a2e9-105">DESCRIPTION</span></span>
<span data-ttu-id="9a2e9-106">Создает новую организацию в управлении Api.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="9a2e9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a2e9-107">EXAMPLES</span></span>

### <span data-ttu-id="9a2e9-108">Пример 1. Создание backend 123 с помощью базовой схемы авторизации</span><span class="sxs-lookup"><span data-stu-id="9a2e9-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="9a2e9-109">Создание нового backend</span><span class="sxs-lookup"><span data-stu-id="9a2e9-109">Creates a new Backend</span></span>

## <span data-ttu-id="9a2e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a2e9-110">PARAMETERS</span></span>

### <span data-ttu-id="9a2e9-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="9a2e9-111">-BackendId</span></span>
<span data-ttu-id="9a2e9-112">Идентификатор нового backend.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-112">Identifier of new backend.</span></span>
<span data-ttu-id="9a2e9-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-113">This parameter is optional.</span></span>
<span data-ttu-id="9a2e9-114">Если он не указан, будет создан.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="9a2e9-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="9a2e9-115">-Context</span></span>
<span data-ttu-id="9a2e9-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9a2e9-117">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9a2e9-117">This parameter is required.</span></span>

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

### <span data-ttu-id="9a2e9-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="9a2e9-118">-Credential</span></span>
<span data-ttu-id="9a2e9-119">Сведения об учетных данных, которые следует использовать при беседе с backend.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="9a2e9-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="9a2e9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a2e9-121">-DefaultProfile</span></span>
<span data-ttu-id="9a2e9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a2e9-123">-Description</span><span class="sxs-lookup"><span data-stu-id="9a2e9-123">-Description</span></span>
<span data-ttu-id="9a2e9-124">Описание backend.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-124">Backend Description.</span></span>
<span data-ttu-id="9a2e9-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="9a2e9-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9a2e9-126">-Protocol</span></span>
<span data-ttu-id="9a2e9-127">Протокол Backend Communication (Протокол backend Communication).</span><span class="sxs-lookup"><span data-stu-id="9a2e9-127">Backend Communication protocol.</span></span>
<span data-ttu-id="9a2e9-128">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9a2e9-128">This parameter is required.</span></span>
<span data-ttu-id="9a2e9-129">Допустимые значения: http и soap.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="9a2e9-130">-Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="9a2e9-130">-Proxy</span></span>
<span data-ttu-id="9a2e9-131">Сведения прокси-сервера, которые будут использоваться при отправке запроса на сервер серверов.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="9a2e9-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="9a2e9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a2e9-133">-ResourceId</span></span>
<span data-ttu-id="9a2e9-134">Uri управления ресурсом внешней системы.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="9a2e9-135">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-135">This parameter is optional.</span></span>
<span data-ttu-id="9a2e9-136">Этот URL-адрес может быть ид ресурса Arm приложений Logic, приложений для функций и приложений API.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="9a2e9-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="9a2e9-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="9a2e9-138">Сведения о структуре кластера "Сервис".</span><span class="sxs-lookup"><span data-stu-id="9a2e9-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="9a2e9-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="9a2e9-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="9a2e9-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="9a2e9-141">Следует ли пропустить проверку цепочки сертификатов при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="9a2e9-142">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="9a2e9-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="9a2e9-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="9a2e9-144">Следует ли пропускать проверку имени сертификата при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="9a2e9-145">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="9a2e9-146">-Title</span><span class="sxs-lookup"><span data-stu-id="9a2e9-146">-Title</span></span>
<span data-ttu-id="9a2e9-147">Заголовок для backend.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-147">Backend Title.</span></span>
<span data-ttu-id="9a2e9-148">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="9a2e9-149">-URL-адрес</span><span class="sxs-lookup"><span data-stu-id="9a2e9-149">-Url</span></span>
<span data-ttu-id="9a2e9-150">URL-адрес времени запуска для backend.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="9a2e9-151">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="9a2e9-151">This parameter is required.</span></span>

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

### <span data-ttu-id="9a2e9-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a2e9-152">-Confirm</span></span>
<span data-ttu-id="9a2e9-153">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a2e9-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a2e9-154">-WhatIf</span></span>
<span data-ttu-id="9a2e9-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a2e9-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a2e9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a2e9-157">CommonParameters</span></span>
<span data-ttu-id="9a2e9-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a2e9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a2e9-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a2e9-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a2e9-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a2e9-160">INPUTS</span></span>

### <span data-ttu-id="9a2e9-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9a2e9-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9a2e9-162">System.String</span><span class="sxs-lookup"><span data-stu-id="9a2e9-162">System.String</span></span>

### <span data-ttu-id="9a2e9-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9a2e9-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9a2e9-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="9a2e9-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="9a2e9-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="9a2e9-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="9a2e9-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="9a2e9-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="9a2e9-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a2e9-167">OUTPUTS</span></span>

### <span data-ttu-id="9a2e9-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9a2e9-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="9a2e9-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a2e9-169">NOTES</span></span>

## <span data-ttu-id="9a2e9-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a2e9-170">RELATED LINKS</span></span>

[<span data-ttu-id="9a2e9-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9a2e9-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="9a2e9-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="9a2e9-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="9a2e9-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="9a2e9-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="9a2e9-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9a2e9-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="9a2e9-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9a2e9-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

