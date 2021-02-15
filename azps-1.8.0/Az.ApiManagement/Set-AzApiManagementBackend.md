---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 0ac89ed099029fbbabe90e07da7ba9c204449db9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400745"
---
# <span data-ttu-id="c780b-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c780b-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="c780b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c780b-102">SYNOPSIS</span></span>
<span data-ttu-id="c780b-103">Обновляет backend.</span><span class="sxs-lookup"><span data-stu-id="c780b-103">Updates a Backend.</span></span>

## <span data-ttu-id="c780b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c780b-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c780b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c780b-105">DESCRIPTION</span></span>
<span data-ttu-id="c780b-106">Обновляет существующий backend in the Api Management (Управление Api).</span><span class="sxs-lookup"><span data-stu-id="c780b-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="c780b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c780b-107">EXAMPLES</span></span>

### <span data-ttu-id="c780b-108">Обновляет описание backend 123.</span><span class="sxs-lookup"><span data-stu-id="c780b-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="c780b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c780b-109">PARAMETERS</span></span>

### <span data-ttu-id="c780b-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="c780b-110">-BackendId</span></span>
<span data-ttu-id="c780b-111">Идентификатор нового backend.</span><span class="sxs-lookup"><span data-stu-id="c780b-111">Identifier of new backend.</span></span>
<span data-ttu-id="c780b-112">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c780b-112">This parameter is required.</span></span>

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

### <span data-ttu-id="c780b-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="c780b-113">-Context</span></span>
<span data-ttu-id="c780b-114">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c780b-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c780b-115">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="c780b-115">This parameter is required.</span></span>

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

### <span data-ttu-id="c780b-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="c780b-116">-Credential</span></span>
<span data-ttu-id="c780b-117">Учетные данные, которые следует использовать при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="c780b-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="c780b-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c780b-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="c780b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c780b-119">-DefaultProfile</span></span>
<span data-ttu-id="c780b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c780b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c780b-121">-Description</span><span class="sxs-lookup"><span data-stu-id="c780b-121">-Description</span></span>
<span data-ttu-id="c780b-122">Описание backend.</span><span class="sxs-lookup"><span data-stu-id="c780b-122">Backend Description.</span></span>
<span data-ttu-id="c780b-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c780b-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="c780b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c780b-124">-PassThru</span></span>
<span data-ttu-id="c780b-125">Указывает на то, что этот cmdlet возвращает  **psApiManagementBackend,** который изменяет этот.</span><span class="sxs-lookup"><span data-stu-id="c780b-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c780b-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c780b-126">-Protocol</span></span>
<span data-ttu-id="c780b-127">Протокол backend Communication (http или soap).</span><span class="sxs-lookup"><span data-stu-id="c780b-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="c780b-128">Этот параметр необязателен.</span><span class="sxs-lookup"><span data-stu-id="c780b-128">This parameter is optional</span></span>

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

### <span data-ttu-id="c780b-129">-Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="c780b-129">-Proxy</span></span>
<span data-ttu-id="c780b-130">Сведения прокси-сервера, которые будут использоваться при отправке запроса на сервер серверов.</span><span class="sxs-lookup"><span data-stu-id="c780b-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="c780b-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c780b-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="c780b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c780b-132">-ResourceId</span></span>
<span data-ttu-id="c780b-133">Uri управления ресурсом внешней системы.</span><span class="sxs-lookup"><span data-stu-id="c780b-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="c780b-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c780b-134">This parameter is optional.</span></span>
<span data-ttu-id="c780b-135">Этот URL-адрес может быть ид ресурса Arm приложений Logic, приложений для функций и приложений API.</span><span class="sxs-lookup"><span data-stu-id="c780b-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="c780b-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c780b-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="c780b-137">Сведения о структуре кластера "Сервис".</span><span class="sxs-lookup"><span data-stu-id="c780b-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="c780b-138">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c780b-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="c780b-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="c780b-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="c780b-140">Следует ли пропустить проверку цепочки сертификатов при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="c780b-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="c780b-141">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c780b-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="c780b-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="c780b-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="c780b-143">Следует ли пропускать проверку имени сертификата при разговоре с backend.</span><span class="sxs-lookup"><span data-stu-id="c780b-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="c780b-144">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c780b-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="c780b-145">-Title</span><span class="sxs-lookup"><span data-stu-id="c780b-145">-Title</span></span>
<span data-ttu-id="c780b-146">Заголовок для backend.</span><span class="sxs-lookup"><span data-stu-id="c780b-146">Backend Title.</span></span>
<span data-ttu-id="c780b-147">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c780b-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="c780b-148">-URL-адрес</span><span class="sxs-lookup"><span data-stu-id="c780b-148">-Url</span></span>
<span data-ttu-id="c780b-149">URL-адрес времени запуска для backend.</span><span class="sxs-lookup"><span data-stu-id="c780b-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="c780b-150">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c780b-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="c780b-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c780b-151">-Confirm</span></span>
<span data-ttu-id="c780b-152">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c780b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c780b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c780b-153">-WhatIf</span></span>
<span data-ttu-id="c780b-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c780b-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c780b-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c780b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c780b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c780b-156">CommonParameters</span></span>
<span data-ttu-id="c780b-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c780b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c780b-158">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c780b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c780b-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c780b-159">INPUTS</span></span>

### <span data-ttu-id="c780b-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c780b-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c780b-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c780b-161">System.String</span></span>

### <span data-ttu-id="c780b-162">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c780b-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c780b-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="c780b-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="c780b-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="c780b-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="c780b-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c780b-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="c780b-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c780b-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c780b-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c780b-167">OUTPUTS</span></span>

### <span data-ttu-id="c780b-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c780b-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="c780b-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c780b-169">NOTES</span></span>

## <span data-ttu-id="c780b-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c780b-170">RELATED LINKS</span></span>

[<span data-ttu-id="c780b-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c780b-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="c780b-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c780b-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="c780b-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="c780b-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="c780b-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="c780b-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="c780b-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c780b-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
