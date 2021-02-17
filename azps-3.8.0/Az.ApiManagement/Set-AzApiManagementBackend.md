---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 8631120178a256aa1ec5b817727f9362f6d8f076
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407290"
---
# <span data-ttu-id="89cb3-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="89cb3-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="89cb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="89cb3-103">Обновляет backend.</span><span class="sxs-lookup"><span data-stu-id="89cb3-103">Updates a Backend.</span></span>

## <span data-ttu-id="89cb3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89cb3-104">SYNTAX</span></span>

### <span data-ttu-id="89cb3-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89cb3-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89cb3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="89cb3-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89cb3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89cb3-107">DESCRIPTION</span></span>
<span data-ttu-id="89cb3-108">Обновляет существующий backend in the Api Management (Управление Api).</span><span class="sxs-lookup"><span data-stu-id="89cb3-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="89cb3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89cb3-109">EXAMPLES</span></span>

### <span data-ttu-id="89cb3-110">Обновляет описание backend 123.</span><span class="sxs-lookup"><span data-stu-id="89cb3-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="89cb3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89cb3-111">PARAMETERS</span></span>

### <span data-ttu-id="89cb3-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="89cb3-112">-BackendId</span></span>
<span data-ttu-id="89cb3-113">Идентификатор нового backend.</span><span class="sxs-lookup"><span data-stu-id="89cb3-113">Identifier of new backend.</span></span>
<span data-ttu-id="89cb3-114">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="89cb3-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89cb3-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="89cb3-115">-Context</span></span>
<span data-ttu-id="89cb3-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="89cb3-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="89cb3-117">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="89cb3-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89cb3-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="89cb3-118">-Credential</span></span>
<span data-ttu-id="89cb3-119">Учетные данные, которые следует использовать при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="89cb3-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="89cb3-120">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="89cb3-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="89cb3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89cb3-121">-DefaultProfile</span></span>
<span data-ttu-id="89cb3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89cb3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89cb3-123">-Description</span><span class="sxs-lookup"><span data-stu-id="89cb3-123">-Description</span></span>
<span data-ttu-id="89cb3-124">Описание backend.</span><span class="sxs-lookup"><span data-stu-id="89cb3-124">Backend Description.</span></span>
<span data-ttu-id="89cb3-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="89cb3-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="89cb3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89cb3-126">-InputObject</span></span>
<span data-ttu-id="89cb3-127">Экземпляр PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="89cb3-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="89cb3-128">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="89cb3-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89cb3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89cb3-129">-PassThru</span></span>
<span data-ttu-id="89cb3-130">Указывает на то, что этот cmdlet возвращает  **psApiManagementBackend,** который изменяет этот.</span><span class="sxs-lookup"><span data-stu-id="89cb3-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="89cb3-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="89cb3-131">-Protocol</span></span>
<span data-ttu-id="89cb3-132">Протокол backend Communication (http или soap).</span><span class="sxs-lookup"><span data-stu-id="89cb3-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="89cb3-133">Этот параметр необязателен.</span><span class="sxs-lookup"><span data-stu-id="89cb3-133">This parameter is optional</span></span>

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

### <span data-ttu-id="89cb3-134">-Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="89cb3-134">-Proxy</span></span>
<span data-ttu-id="89cb3-135">Сведения прокси-сервера, которые будут использоваться при отправке запроса на сервер серверов.</span><span class="sxs-lookup"><span data-stu-id="89cb3-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="89cb3-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="89cb3-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="89cb3-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89cb3-137">-ResourceId</span></span>
<span data-ttu-id="89cb3-138">Uri управления ресурсом внешней системы.</span><span class="sxs-lookup"><span data-stu-id="89cb3-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="89cb3-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="89cb3-139">This parameter is optional.</span></span>
<span data-ttu-id="89cb3-140">Этот URL-адрес может быть ид ресурса Arm приложений Logic, приложений для функций и приложений API.</span><span class="sxs-lookup"><span data-stu-id="89cb3-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="89cb3-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="89cb3-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="89cb3-142">Сведения о структуре кластера "Сервис".</span><span class="sxs-lookup"><span data-stu-id="89cb3-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="89cb3-143">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="89cb3-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="89cb3-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="89cb3-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="89cb3-145">Следует ли пропустить проверку цепочки сертификатов при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="89cb3-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="89cb3-146">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="89cb3-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="89cb3-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="89cb3-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="89cb3-148">Следует ли пропускать проверку имени сертификата при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="89cb3-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="89cb3-149">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="89cb3-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="89cb3-150">-Title</span><span class="sxs-lookup"><span data-stu-id="89cb3-150">-Title</span></span>
<span data-ttu-id="89cb3-151">Заголовок для backend.</span><span class="sxs-lookup"><span data-stu-id="89cb3-151">Backend Title.</span></span>
<span data-ttu-id="89cb3-152">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="89cb3-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="89cb3-153">-URL-адрес</span><span class="sxs-lookup"><span data-stu-id="89cb3-153">-Url</span></span>
<span data-ttu-id="89cb3-154">URL-адрес времени запуска для backend.</span><span class="sxs-lookup"><span data-stu-id="89cb3-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="89cb3-155">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="89cb3-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="89cb3-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89cb3-156">-Confirm</span></span>
<span data-ttu-id="89cb3-157">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="89cb3-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89cb3-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89cb3-158">-WhatIf</span></span>
<span data-ttu-id="89cb3-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89cb3-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89cb3-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="89cb3-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89cb3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89cb3-161">CommonParameters</span></span>
<span data-ttu-id="89cb3-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89cb3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89cb3-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89cb3-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89cb3-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89cb3-164">INPUTS</span></span>

### <span data-ttu-id="89cb3-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="89cb3-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="89cb3-166">System.String</span><span class="sxs-lookup"><span data-stu-id="89cb3-166">System.String</span></span>

### <span data-ttu-id="89cb3-167">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="89cb3-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="89cb3-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="89cb3-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="89cb3-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="89cb3-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="89cb3-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="89cb3-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="89cb3-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89cb3-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89cb3-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89cb3-172">OUTPUTS</span></span>

### <span data-ttu-id="89cb3-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="89cb3-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="89cb3-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89cb3-174">NOTES</span></span>

## <span data-ttu-id="89cb3-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89cb3-175">RELATED LINKS</span></span>

[<span data-ttu-id="89cb3-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="89cb3-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="89cb3-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="89cb3-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="89cb3-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="89cb3-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="89cb3-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="89cb3-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="89cb3-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="89cb3-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
