---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/add-azureanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
ms.openlocfilehash: 39d15940b85e7da19cf4f8f23abee5db6223235f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558696"
---
# <span data-ttu-id="38751-101">Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="38751-101">Add-AzureAnalysisServicesAccount</span></span>

## <span data-ttu-id="38751-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38751-102">SYNOPSIS</span></span>
<span data-ttu-id="38751-103">Добавляет учетную запись с проверкой подлинности для использования в запросах командлетов служб аналитики Azure.</span><span class="sxs-lookup"><span data-stu-id="38751-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38751-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38751-104">SYNTAX</span></span>

### <span data-ttu-id="38751-105">UserParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38751-105">UserParameterSetName (Default)</span></span>
```
Add-AzureAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38751-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="38751-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential>
 [-ServicePrincipal] -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38751-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="38751-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38751-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38751-108">DESCRIPTION</span></span>
<span data-ttu-id="38751-109">Командлет Add-AzureAnalysisServicesAccount используется для входа в экземпляр сервера служб аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="38751-109">The Add-AzureAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="38751-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38751-110">EXAMPLES</span></span>

### <span data-ttu-id="38751-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="38751-111">Example 1</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="38751-112">Этот пример добавит учетную запись, заданную переменной $UserCredential, в среду служб аналитики westcentralus.asazure.windows.net.</span><span class="sxs-lookup"><span data-stu-id="38751-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="38751-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="38751-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="38751-114">Первая команда получает учетные данные субъекта-службы приложения, а затем сохраняет их в переменной $ApplicationCredential.</span><span class="sxs-lookup"><span data-stu-id="38751-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="38751-115">Вторая команда добавляет учетную запись субъекта-службы приложения, заданную переменной $ApplicationCredential, и TenantId в среде служб аналитики westcentralus.asazure.windows.net.</span><span class="sxs-lookup"><span data-stu-id="38751-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="38751-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="38751-116">Example 3</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="38751-117">В этом примере добавляется учетная запись субъекта-службы приложения, указанная в "ApplicationId", "TenantId" и "CertificateThumbprint" в среде служб Analysis Services westcentralus.asazure.windows.net.</span><span class="sxs-lookup"><span data-stu-id="38751-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="38751-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38751-118">PARAMETERS</span></span>

### <span data-ttu-id="38751-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="38751-119">-ApplicationId</span></span>
<span data-ttu-id="38751-120">Идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="38751-120">The application ID.</span></span>

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

### <span data-ttu-id="38751-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="38751-121">-CertificateThumbprint</span></span>
<span data-ttu-id="38751-122">Хэш сертификата (отпечаток)</span><span class="sxs-lookup"><span data-stu-id="38751-122">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="38751-123">-Credential</span><span class="sxs-lookup"><span data-stu-id="38751-123">-Credential</span></span>
<span data-ttu-id="38751-124">Учетные данные для входа</span><span class="sxs-lookup"><span data-stu-id="38751-124">Login credentials</span></span>

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

### <span data-ttu-id="38751-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="38751-125">-RolloutEnvironment</span></span>
<span data-ttu-id="38751-126">Имя среды служб Analysis Services Azure, к которой необходимо выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="38751-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="38751-127">С учетом полного имени сервера например asazure://westcentralus.asazure.windows.net/testserver, правильным значением для этой переменной будет westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="38751-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

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

### <span data-ttu-id="38751-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="38751-128">-ServicePrincipal</span></span>
<span data-ttu-id="38751-129">Указывает, что учетная запись проходит проверку подлинности путем предоставления учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="38751-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="38751-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="38751-130">-TenantId</span></span>
<span data-ttu-id="38751-131">Имя или идентификатор клиента</span><span class="sxs-lookup"><span data-stu-id="38751-131">Tenant name or ID</span></span>

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

### <span data-ttu-id="38751-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38751-132">-Confirm</span></span>
<span data-ttu-id="38751-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38751-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38751-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38751-134">-WhatIf</span></span>
<span data-ttu-id="38751-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38751-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38751-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38751-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38751-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38751-137">CommonParameters</span></span>
<span data-ttu-id="38751-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38751-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38751-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38751-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38751-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38751-140">INPUTS</span></span>

### <span data-ttu-id="38751-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="38751-141">None</span></span>

## <span data-ttu-id="38751-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38751-142">OUTPUTS</span></span>

### <span data-ttu-id="38751-143">Microsoft. Azure. Commands. AnalysisServices. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="38751-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="38751-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="38751-144">NOTES</span></span>
<span data-ttu-id="38751-145">Alias (псевдоним): Login-AzureAsAccount</span><span class="sxs-lookup"><span data-stu-id="38751-145">Alias: Login-AzureAsAccount</span></span>

## <span data-ttu-id="38751-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38751-146">RELATED LINKS</span></span>
