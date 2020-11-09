---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 7ab7c679bc623a9eaa0f99bcdba1ab8281bd7d8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316364"
---
# <span data-ttu-id="e8b47-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e8b47-101">New-AzADApplication</span></span>

## <span data-ttu-id="e8b47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8b47-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b47-103">Создание нового приложения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e8b47-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="e8b47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8b47-104">SYNTAX</span></span>

### <span data-ttu-id="e8b47-105">ApplicationWithoutCredentialParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8b47-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b47-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8b47-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b47-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8b47-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b47-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8b47-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b47-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8b47-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8b47-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8b47-110">DESCRIPTION</span></span>
<span data-ttu-id="e8b47-111">Создание нового приложения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e8b47-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="e8b47-112">Ниже приводятся разрешения, необходимые для создания приложения.</span><span class="sxs-lookup"><span data-stu-id="e8b47-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="e8b47-113">Graph Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e8b47-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="e8b47-114">Application. ReadWrite. OwnedBy</span><span class="sxs-lookup"><span data-stu-id="e8b47-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="e8b47-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e8b47-115">Microsoft Graph</span></span>
  - <span data-ttu-id="e8b47-116">Directory. AccessAsUser. ALL</span><span class="sxs-lookup"><span data-stu-id="e8b47-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="e8b47-117">Directory. ReadWrite. ALL</span><span class="sxs-lookup"><span data-stu-id="e8b47-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="e8b47-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8b47-118">EXAMPLES</span></span>

### <span data-ttu-id="e8b47-119">Пример 1: создание нового приложения AAD.</span><span class="sxs-lookup"><span data-stu-id="e8b47-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="e8b47-120">Создание нового приложения Azure Active Directory без каких-либо учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e8b47-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="e8b47-121">Пример 2: создание нового приложения AAD с паролем.</span><span class="sxs-lookup"><span data-stu-id="e8b47-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="e8b47-122">Создание нового приложения Azure Active Directory и связывание с ним учетных данных пароля.</span><span class="sxs-lookup"><span data-stu-id="e8b47-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="e8b47-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8b47-123">PARAMETERS</span></span>

### <span data-ttu-id="e8b47-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="e8b47-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="e8b47-125">Значение, определяющее, является ли приложение единственным клиентом или несколькими клиентами.</span><span class="sxs-lookup"><span data-stu-id="e8b47-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="e8b47-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="e8b47-126">-CertValue</span></span>
<span data-ttu-id="e8b47-127">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="e8b47-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="e8b47-128">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="e8b47-128">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="e8b47-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b47-129">-DefaultProfile</span></span>
<span data-ttu-id="e8b47-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e8b47-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8b47-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e8b47-131">-DisplayName</span></span>
<span data-ttu-id="e8b47-132">Отображаемое имя нового приложения.</span><span class="sxs-lookup"><span data-stu-id="e8b47-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="e8b47-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e8b47-133">-EndDate</span></span>
<span data-ttu-id="e8b47-134">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e8b47-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="e8b47-135">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="e8b47-135">The default end date value is one year from today.</span></span> <span data-ttu-id="e8b47-136">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="e8b47-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="e8b47-137">-Главная страница</span><span class="sxs-lookup"><span data-stu-id="e8b47-137">-HomePage</span></span>
<span data-ttu-id="e8b47-138">URL-адрес домашней страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="e8b47-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="e8b47-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="e8b47-139">-IdentifierUris</span></span>
<span data-ttu-id="e8b47-140">Универсальные коды ресурсов (URI), обозначающие приложение.</span><span class="sxs-lookup"><span data-stu-id="e8b47-140">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="e8b47-141">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="e8b47-141">-KeyCredentials</span></span>
<span data-ttu-id="e8b47-142">Список учетных данных сертификата, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="e8b47-142">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="e8b47-143">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="e8b47-143">-Password</span></span>
<span data-ttu-id="e8b47-144">Пароль, который должен быть связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="e8b47-144">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="e8b47-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="e8b47-145">-PasswordCredentials</span></span>
<span data-ttu-id="e8b47-146">Список учетных данных пароля, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="e8b47-146">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="e8b47-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="e8b47-147">-ReplyUrls</span></span>
<span data-ttu-id="e8b47-148">URL-адреса ответа приложения.</span><span class="sxs-lookup"><span data-stu-id="e8b47-148">The application reply urls.</span></span>

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

### <span data-ttu-id="e8b47-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e8b47-149">-StartDate</span></span>
<span data-ttu-id="e8b47-150">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e8b47-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="e8b47-151">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="e8b47-151">The default start date value is today.</span></span> <span data-ttu-id="e8b47-152">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="e8b47-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="e8b47-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8b47-153">-Confirm</span></span>
<span data-ttu-id="e8b47-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8b47-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8b47-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8b47-155">-WhatIf</span></span>
<span data-ttu-id="e8b47-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8b47-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8b47-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8b47-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8b47-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b47-158">CommonParameters</span></span>
<span data-ttu-id="e8b47-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8b47-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b47-160">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8b47-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b47-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8b47-161">INPUTS</span></span>

### <span data-ttu-id="e8b47-162">System. String</span><span class="sxs-lookup"><span data-stu-id="e8b47-162">System.String</span></span>

### <span data-ttu-id="e8b47-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="e8b47-163">System.String[]</span></span>

### <span data-ttu-id="e8b47-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8b47-164">System.Boolean</span></span>

### <span data-ttu-id="e8b47-165">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="e8b47-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="e8b47-166">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="e8b47-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="e8b47-167">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e8b47-167">System.Security.SecureString</span></span>

### <span data-ttu-id="e8b47-168">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="e8b47-168">System.DateTime</span></span>

## <span data-ttu-id="e8b47-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8b47-169">OUTPUTS</span></span>

### <span data-ttu-id="e8b47-170">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e8b47-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e8b47-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8b47-171">NOTES</span></span>
<span data-ttu-id="e8b47-172">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="e8b47-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e8b47-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8b47-173">RELATED LINKS</span></span>

[<span data-ttu-id="e8b47-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e8b47-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="e8b47-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e8b47-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="e8b47-176">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e8b47-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="e8b47-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e8b47-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="e8b47-178">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e8b47-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="e8b47-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e8b47-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

