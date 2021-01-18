---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: f1d59a0a34072a91242c6595c269ba55c4397e0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516742"
---
# <span data-ttu-id="10afd-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10afd-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="10afd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10afd-102">SYNOPSIS</span></span>
<span data-ttu-id="10afd-103">Добавляет учетную запись, аутентификацию, которая будет применяться к запросам на использование серверов служб Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="10afd-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="10afd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="10afd-104">SYNTAX</span></span>

### <span data-ttu-id="10afd-105">UserParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="10afd-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10afd-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="10afd-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10afd-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="10afd-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10afd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10afd-108">DESCRIPTION</span></span>
<span data-ttu-id="10afd-109">Этот Add-AzAnalysisServicesAccount используется для входа на сервер служб Azure Analysis Services</span><span class="sxs-lookup"><span data-stu-id="10afd-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="10afd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="10afd-110">EXAMPLES</span></span>

### <span data-ttu-id="10afd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="10afd-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="10afd-112">В этом примере учетная запись, заданная переменной $UserCredential, будет добавлена в среду westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="10afd-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="10afd-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="10afd-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="10afd-114">Первая команда получает учетные данные основного приложения, а затем сохраняет их в переменной $ApplicationCredential службы.</span><span class="sxs-lookup"><span data-stu-id="10afd-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="10afd-115">Вторая команда добавляет учетную запись основного обслуживания приложения, заданную переменной $ApplicationCredential TenantId, в среду westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="10afd-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="10afd-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="10afd-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="10afd-117">В этом примере в среду westcentralus.asazure.windows.net Analysis Services добавляется учетная запись основного приложения, заданная в ApplicationId, TenantId и CertificateThumbprint.</span><span class="sxs-lookup"><span data-stu-id="10afd-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="10afd-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10afd-118">PARAMETERS</span></span>

### <span data-ttu-id="10afd-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="10afd-119">-ApplicationId</span></span>
<span data-ttu-id="10afd-120">ИД приложения.</span><span class="sxs-lookup"><span data-stu-id="10afd-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10afd-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="10afd-121">-CertificateThumbprint</span></span>
<span data-ttu-id="10afd-122">Hash certificate (Thumbprint)</span><span class="sxs-lookup"><span data-stu-id="10afd-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10afd-123">-Credential</span><span class="sxs-lookup"><span data-stu-id="10afd-123">-Credential</span></span>
<span data-ttu-id="10afd-124">Учетные данные для входа</span><span class="sxs-lookup"><span data-stu-id="10afd-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10afd-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="10afd-125">-RolloutEnvironment</span></span>
<span data-ttu-id="10afd-126">Имя среды Azure Analysis Services, в которую нужно в нее влиться.</span><span class="sxs-lookup"><span data-stu-id="10afd-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="10afd-127">По полному имени сервера, например asazure://westcentralus.asazure.windows.net/testserver, для этой переменной будет задано правильное значение westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="10afd-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10afd-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="10afd-128">-ServicePrincipal</span></span>
<span data-ttu-id="10afd-129">Указывает на то, что эта учетная запись аутентификация путем предоставления учетных данных для основной службы.</span><span class="sxs-lookup"><span data-stu-id="10afd-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10afd-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="10afd-130">-TenantId</span></span>
<span data-ttu-id="10afd-131">Имя клиента или ИД клиента</span><span class="sxs-lookup"><span data-stu-id="10afd-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10afd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10afd-132">-Confirm</span></span>
<span data-ttu-id="10afd-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10afd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10afd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10afd-134">-WhatIf</span></span>
<span data-ttu-id="10afd-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10afd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10afd-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="10afd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10afd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10afd-137">CommonParameters</span></span>
<span data-ttu-id="10afd-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10afd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10afd-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10afd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10afd-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10afd-140">INPUTS</span></span>

### <span data-ttu-id="10afd-141">Нет</span><span class="sxs-lookup"><span data-stu-id="10afd-141">None</span></span>

## <span data-ttu-id="10afd-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10afd-142">OUTPUTS</span></span>

### <span data-ttu-id="10afd-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="10afd-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="10afd-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="10afd-144">NOTES</span></span>
<span data-ttu-id="10afd-145">Псевдоним: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="10afd-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="10afd-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10afd-146">RELATED LINKS</span></span>
