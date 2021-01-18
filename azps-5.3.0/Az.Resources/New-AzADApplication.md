---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 7ab7c679bc623a9eaa0f99bcdba1ab8281bd7d8f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505235"
---
# <span data-ttu-id="e3f9a-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e3f9a-101">New-AzADApplication</span></span>

## <span data-ttu-id="e3f9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f9a-103">Создает приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="e3f9a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e3f9a-104">SYNTAX</span></span>

### <span data-ttu-id="e3f9a-105">ApplicationWithoutCredentialParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3f9a-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f9a-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f9a-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f9a-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f9a-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f9a-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f9a-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3f9a-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3f9a-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3f9a-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3f9a-110">DESCRIPTION</span></span>
<span data-ttu-id="e3f9a-111">Создает приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="e3f9a-112">Ниже приведены разрешения, необходимые для создания приложения.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="e3f9a-113">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="e3f9a-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="e3f9a-114">Application.ReadWrite.OwnedBy</span><span class="sxs-lookup"><span data-stu-id="e3f9a-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="e3f9a-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e3f9a-115">Microsoft Graph</span></span>
  - <span data-ttu-id="e3f9a-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e3f9a-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="e3f9a-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e3f9a-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="e3f9a-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e3f9a-118">EXAMPLES</span></span>

### <span data-ttu-id="e3f9a-119">Пример 1. Создание приложения AAD.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="e3f9a-120">Создает приложение Azure Active Directory без учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="e3f9a-121">Пример 2. Создание нового приложения AAD с паролем.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="e3f9a-122">Создает приложение Azure Active Directory и связывает с ним учетные данные паролей.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="e3f9a-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3f9a-123">PARAMETERS</span></span>

### <span data-ttu-id="e3f9a-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="e3f9a-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="e3f9a-125">Значение, которое указывает, является ли приложение клиентом или нескольким клиентом.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f9a-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="e3f9a-126">-CertValue</span></span>
<span data-ttu-id="e3f9a-127">Значение асимметричного типа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="e3f9a-128">Он представляет собой 64-кодированный сертификат.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-128">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f9a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f9a-129">-DefaultProfile</span></span>
<span data-ttu-id="e3f9a-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e3f9a-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3f9a-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e3f9a-131">-DisplayName</span></span>
<span data-ttu-id="e3f9a-132">Отображает имя нового приложения.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="e3f9a-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e3f9a-133">-EndDate</span></span>
<span data-ttu-id="e3f9a-134">Дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="e3f9a-135">Значение даты окончания по умолчанию составляет один год с сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-135">The default end date value is one year from today.</span></span> <span data-ttu-id="e3f9a-136">Для учетных данных асимметричного типа необходимо установить этот учетный данные в день, когда допустим сертификат X509, или до нее.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f9a-137">-HomePage</span><span class="sxs-lookup"><span data-stu-id="e3f9a-137">-HomePage</span></span>
<span data-ttu-id="e3f9a-138">URL-адрес домашней страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="e3f9a-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="e3f9a-139">-IdentifierUris</span></span>
<span data-ttu-id="e3f9a-140">ЮРИС, определяют приложение.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-140">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f9a-141">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="e3f9a-141">-KeyCredentials</span></span>
<span data-ttu-id="e3f9a-142">Список учетных данных сертификата, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-142">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f9a-143">-Password</span><span class="sxs-lookup"><span data-stu-id="e3f9a-143">-Password</span></span>
<span data-ttu-id="e3f9a-144">Пароль, который будет связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-144">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f9a-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="e3f9a-145">-PasswordCredentials</span></span>
<span data-ttu-id="e3f9a-146">Список учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-146">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f9a-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="e3f9a-147">-ReplyUrls</span></span>
<span data-ttu-id="e3f9a-148">URL-адреса ответов приложений.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-148">The application reply urls.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f9a-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e3f9a-149">-StartDate</span></span>
<span data-ttu-id="e3f9a-150">Начальную дату использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="e3f9a-151">По умолчанию дата начала является сегодняшним значением.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-151">The default start date value is today.</span></span> <span data-ttu-id="e3f9a-152">Для учетных данных "асимметричного" типа это должно быть установлено в дату, начиная с даты действия сертификата X509, или после нее.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f9a-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3f9a-153">-Confirm</span></span>
<span data-ttu-id="e3f9a-154">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3f9a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3f9a-155">-WhatIf</span></span>
<span data-ttu-id="e3f9a-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3f9a-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3f9a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f9a-158">CommonParameters</span></span>
<span data-ttu-id="e3f9a-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f9a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f9a-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3f9a-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f9a-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3f9a-161">INPUTS</span></span>

### <span data-ttu-id="e3f9a-162">System.String</span><span class="sxs-lookup"><span data-stu-id="e3f9a-162">System.String</span></span>

### <span data-ttu-id="e3f9a-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e3f9a-163">System.String[]</span></span>

### <span data-ttu-id="e3f9a-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3f9a-164">System.Boolean</span></span>

### <span data-ttu-id="e3f9a-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="e3f9a-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="e3f9a-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="e3f9a-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="e3f9a-167">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="e3f9a-167">System.Security.SecureString</span></span>

### <span data-ttu-id="e3f9a-168">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="e3f9a-168">System.DateTime</span></span>

## <span data-ttu-id="e3f9a-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3f9a-169">OUTPUTS</span></span>

### <span data-ttu-id="e3f9a-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e3f9a-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e3f9a-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e3f9a-171">NOTES</span></span>
<span data-ttu-id="e3f9a-172">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="e3f9a-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e3f9a-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3f9a-173">RELATED LINKS</span></span>

[<span data-ttu-id="e3f9a-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e3f9a-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="e3f9a-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e3f9a-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="e3f9a-176">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e3f9a-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="e3f9a-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e3f9a-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="e3f9a-178">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e3f9a-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="e3f9a-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e3f9a-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

