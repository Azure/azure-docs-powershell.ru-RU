---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: 323e7dd08c2ec18598f089a8001b6d06970b5600
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720211"
---
# <span data-ttu-id="25cbe-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="25cbe-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="25cbe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25cbe-102">SYNOPSIS</span></span>
<span data-ttu-id="25cbe-103">Добавляет учетную запись с проверкой подлинности для использования в запросах командлетов служб аналитики Azure.</span><span class="sxs-lookup"><span data-stu-id="25cbe-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="25cbe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25cbe-104">SYNTAX</span></span>

### <span data-ttu-id="25cbe-105">UserParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="25cbe-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25cbe-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="25cbe-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25cbe-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="25cbe-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25cbe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25cbe-108">DESCRIPTION</span></span>
<span data-ttu-id="25cbe-109">Командлет Add-AzAnalysisServicesAccount используется для входа в экземпляр сервера служб аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="25cbe-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="25cbe-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25cbe-110">EXAMPLES</span></span>

### <span data-ttu-id="25cbe-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="25cbe-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="25cbe-112">Этот пример добавит учетную запись, заданную переменной $UserCredential, в среду служб аналитики westcentralus.asazure.windows.net.</span><span class="sxs-lookup"><span data-stu-id="25cbe-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="25cbe-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="25cbe-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="25cbe-114">Первая команда получает учетные данные субъекта-службы приложения, а затем сохраняет их в переменной $ApplicationCredential.</span><span class="sxs-lookup"><span data-stu-id="25cbe-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="25cbe-115">Вторая команда добавляет учетную запись субъекта-службы приложения, заданную переменной $ApplicationCredential, и TenantId в среде служб аналитики westcentralus.asazure.windows.net.</span><span class="sxs-lookup"><span data-stu-id="25cbe-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="25cbe-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="25cbe-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="25cbe-117">В этом примере добавляется учетная запись субъекта-службы приложения, указанная в "ApplicationId", "TenantId" и "CertificateThumbprint" в среде служб Analysis Services westcentralus.asazure.windows.net.</span><span class="sxs-lookup"><span data-stu-id="25cbe-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="25cbe-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25cbe-118">PARAMETERS</span></span>

### <span data-ttu-id="25cbe-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="25cbe-119">-ApplicationId</span></span>
<span data-ttu-id="25cbe-120">Идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="25cbe-120">The application ID.</span></span>

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

### <span data-ttu-id="25cbe-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="25cbe-121">-CertificateThumbprint</span></span>
<span data-ttu-id="25cbe-122">Хэш сертификата (отпечаток)</span><span class="sxs-lookup"><span data-stu-id="25cbe-122">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="25cbe-123">-Credential</span><span class="sxs-lookup"><span data-stu-id="25cbe-123">-Credential</span></span>
<span data-ttu-id="25cbe-124">Учетные данные для входа</span><span class="sxs-lookup"><span data-stu-id="25cbe-124">Login credentials</span></span>

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

### <span data-ttu-id="25cbe-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="25cbe-125">-RolloutEnvironment</span></span>
<span data-ttu-id="25cbe-126">Имя среды служб Analysis Services Azure, к которой необходимо выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="25cbe-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="25cbe-127">С учетом полного имени сервера например asazure://westcentralus.asazure.windows.net/testserver, правильным значением для этой переменной будет westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="25cbe-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

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

### <span data-ttu-id="25cbe-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="25cbe-128">-ServicePrincipal</span></span>
<span data-ttu-id="25cbe-129">Указывает, что учетная запись проходит проверку подлинности путем предоставления учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="25cbe-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="25cbe-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="25cbe-130">-TenantId</span></span>
<span data-ttu-id="25cbe-131">Имя или идентификатор клиента</span><span class="sxs-lookup"><span data-stu-id="25cbe-131">Tenant name or ID</span></span>

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

### <span data-ttu-id="25cbe-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25cbe-132">-Confirm</span></span>
<span data-ttu-id="25cbe-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25cbe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25cbe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25cbe-134">-WhatIf</span></span>
<span data-ttu-id="25cbe-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25cbe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25cbe-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25cbe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25cbe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25cbe-137">CommonParameters</span></span>
<span data-ttu-id="25cbe-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25cbe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25cbe-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25cbe-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25cbe-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25cbe-140">INPUTS</span></span>

### <span data-ttu-id="25cbe-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="25cbe-141">None</span></span>

## <span data-ttu-id="25cbe-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25cbe-142">OUTPUTS</span></span>

### <span data-ttu-id="25cbe-143">Microsoft. Azure. Commands. AnalysisServices. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="25cbe-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="25cbe-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="25cbe-144">NOTES</span></span>
<span data-ttu-id="25cbe-145">Alias (псевдоним): Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="25cbe-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="25cbe-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25cbe-146">RELATED LINKS</span></span>
