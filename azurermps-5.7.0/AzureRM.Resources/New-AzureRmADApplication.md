---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: 171f09e2d9a9e6e646731817526451b311f94482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566913"
---
# <span data-ttu-id="0a65f-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0a65f-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="0a65f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a65f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a65f-103">Создание нового приложения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0a65f-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a65f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a65f-104">SYNTAX</span></span>

### <span data-ttu-id="0a65f-105">ApplicationWithoutCredentialParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a65f-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a65f-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a65f-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a65f-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a65f-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a65f-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a65f-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a65f-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a65f-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a65f-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a65f-110">DESCRIPTION</span></span>
<span data-ttu-id="0a65f-111">Создание нового приложения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0a65f-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="0a65f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a65f-112">EXAMPLES</span></span>

### <span data-ttu-id="0a65f-113">Создайте новое приложение AAD.</span><span class="sxs-lookup"><span data-stu-id="0a65f-113">Create new AAD application.</span></span>
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="0a65f-114">Создание нового приложения Azure Active Directory без каких-либо учетных данных.</span><span class="sxs-lookup"><span data-stu-id="0a65f-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="0a65f-115">Создайте новое приложение AAD с паролем.</span><span class="sxs-lookup"><span data-stu-id="0a65f-115">Create new AAD application with password.</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="0a65f-116">Создание нового приложения Azure Active Directory и связывание с ним учетных данных пароля.</span><span class="sxs-lookup"><span data-stu-id="0a65f-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="0a65f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a65f-117">PARAMETERS</span></span>

### <span data-ttu-id="0a65f-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="0a65f-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="0a65f-119">Значение, определяющее, является ли приложение единственным клиентом или несколькими клиентами.</span><span class="sxs-lookup"><span data-stu-id="0a65f-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="0a65f-120">-CertValue</span></span>
<span data-ttu-id="0a65f-121">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="0a65f-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="0a65f-122">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="0a65f-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a65f-123">-DefaultProfile</span></span>
<span data-ttu-id="0a65f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0a65f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0a65f-125">-DisplayName</span></span>
<span data-ttu-id="0a65f-126">Отображаемое имя нового приложения.</span><span class="sxs-lookup"><span data-stu-id="0a65f-126">Display name of the new application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0a65f-127">-EndDate</span></span>
<span data-ttu-id="0a65f-128">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="0a65f-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="0a65f-129">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="0a65f-129">The default end date value is one year from today.</span></span> <span data-ttu-id="0a65f-130">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="0a65f-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-131">-Главная страница</span><span class="sxs-lookup"><span data-stu-id="0a65f-131">-HomePage</span></span>
<span data-ttu-id="0a65f-132">URL-адрес домашней страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="0a65f-132">The URL to the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="0a65f-133">-IdentifierUris</span></span>
<span data-ttu-id="0a65f-134">Универсальные коды ресурсов (URI), обозначающие приложение.</span><span class="sxs-lookup"><span data-stu-id="0a65f-134">The URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-135">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="0a65f-135">-KeyCredentials</span></span>
<span data-ttu-id="0a65f-136">Список учетных данных сертификата, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="0a65f-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-137">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="0a65f-137">-Password</span></span>
<span data-ttu-id="0a65f-138">Пароль, который должен быть связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="0a65f-138">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="0a65f-139">-PasswordCredentials</span></span>
<span data-ttu-id="0a65f-140">Список учетных данных пароля, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="0a65f-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="0a65f-141">-ReplyUrls</span></span>
<span data-ttu-id="0a65f-142">URL-адреса ответа приложения.</span><span class="sxs-lookup"><span data-stu-id="0a65f-142">The application reply urls.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="0a65f-143">-StartDate</span></span>
<span data-ttu-id="0a65f-144">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="0a65f-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="0a65f-145">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="0a65f-145">The default start date value is today.</span></span> <span data-ttu-id="0a65f-146">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="0a65f-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a65f-147">-Confirm</span></span>
<span data-ttu-id="0a65f-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a65f-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a65f-149">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a65f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a65f-150">CommonParameters</span></span>
<span data-ttu-id="0a65f-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a65f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a65f-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a65f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a65f-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a65f-153">INPUTS</span></span>

### <span data-ttu-id="0a65f-154">Ничего</span><span class="sxs-lookup"><span data-stu-id="0a65f-154">None</span></span>
<span data-ttu-id="0a65f-155">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0a65f-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a65f-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a65f-156">OUTPUTS</span></span>

### <span data-ttu-id="0a65f-157">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="0a65f-157">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="0a65f-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a65f-158">NOTES</span></span>
<span data-ttu-id="0a65f-159">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="0a65f-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0a65f-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a65f-160">RELATED LINKS</span></span>

[<span data-ttu-id="0a65f-161">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0a65f-161">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="0a65f-162">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0a65f-162">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="0a65f-163">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0a65f-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="0a65f-164">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0a65f-164">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="0a65f-165">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0a65f-165">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="0a65f-166">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0a65f-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

