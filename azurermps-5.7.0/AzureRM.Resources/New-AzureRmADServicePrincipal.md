---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: ca338fd648010b9158a6bc308bb4dcb2f1c48317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566911"
---
# <span data-ttu-id="60c42-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="60c42-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="60c42-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60c42-102">SYNOPSIS</span></span>
<span data-ttu-id="60c42-103">Создание нового субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="60c42-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60c42-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60c42-104">SYNTAX</span></span>

### <span data-ttu-id="60c42-105">ApplicationWithoutCredentialParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60c42-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60c42-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="60c42-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60c42-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="60c42-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60c42-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="60c42-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60c42-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="60c42-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60c42-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="60c42-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60c42-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="60c42-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60c42-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="60c42-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60c42-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="60c42-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60c42-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="60c42-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60c42-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60c42-115">DESCRIPTION</span></span>
<span data-ttu-id="60c42-116">Создание нового субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="60c42-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="60c42-117">Примечание. командлет также неявно создает приложение и задает его свойства (если не задано значение ApplicationId).</span><span class="sxs-lookup"><span data-stu-id="60c42-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="60c42-118">Чтобы обновить параметры, зависящие от приложения, используйте командлет Set-AzureRmADApplication.</span><span class="sxs-lookup"><span data-stu-id="60c42-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="60c42-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60c42-119">EXAMPLES</span></span>

### <span data-ttu-id="60c42-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="60c42-120">Example 1</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="60c42-121">Создание нового субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="60c42-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="60c42-122">Тип DisplayName (ИД)</span><span class="sxs-lookup"><span data-stu-id="60c42-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="60c42-123">DemoApp ServicePrincipal f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="60c42-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="60c42-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="60c42-124">Example 2</span></span>
```
$SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp -Password $SecureStringPassword
```

<span data-ttu-id="60c42-125">Создание нового субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="60c42-125">Creates a new service principal.</span></span>
<span data-ttu-id="60c42-126">Командлет также неявно создает приложение, поскольку оно не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="60c42-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="60c42-127">Тип DisplayName (ИД)</span><span class="sxs-lookup"><span data-stu-id="60c42-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="60c42-128">SPForNoExistingApp ServicePrincipal 784136ca-3ae2-4fdd-a388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="60c42-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="60c42-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60c42-129">PARAMETERS</span></span>

### <span data-ttu-id="60c42-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="60c42-130">-ApplicationId</span></span>
<span data-ttu-id="60c42-131">Уникальный идентификатор приложения для субъекта-службы в клиенте.</span><span class="sxs-lookup"><span data-stu-id="60c42-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="60c42-132">После создания это свойство невозможно изменить.</span><span class="sxs-lookup"><span data-stu-id="60c42-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="60c42-133">Если идентификатор приложения не указан, будет создан один из них.</span><span class="sxs-lookup"><span data-stu-id="60c42-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c42-134">-CertValue</span><span class="sxs-lookup"><span data-stu-id="60c42-134">-CertValue</span></span>
<span data-ttu-id="60c42-135">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="60c42-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="60c42-136">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="60c42-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c42-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c42-137">-DefaultProfile</span></span>
<span data-ttu-id="60c42-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="60c42-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60c42-139">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="60c42-139">-DisplayName</span></span>
<span data-ttu-id="60c42-140">Понятное имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="60c42-140">The friendly name of the service principal.</span></span>

```yaml
Type: String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c42-141">-EndDate</span><span class="sxs-lookup"><span data-stu-id="60c42-141">-EndDate</span></span>
<span data-ttu-id="60c42-142">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="60c42-142">The effective end date of the credential usage.</span></span>
<span data-ttu-id="60c42-143">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="60c42-143">The default end date value is one year from today.</span></span> <span data-ttu-id="60c42-144">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="60c42-144">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c42-145">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="60c42-145">-KeyCredentials</span></span>
<span data-ttu-id="60c42-146">Список учетных данных сертификата, связанных с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="60c42-146">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c42-147">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="60c42-147">-Password</span></span>
<span data-ttu-id="60c42-148">Пароль, который должен быть связан с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="60c42-148">The password to be associated with the service principal.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c42-149">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="60c42-149">-PasswordCredentials</span></span>
<span data-ttu-id="60c42-150">Список учетных данных, связанных с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="60c42-150">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c42-151">-StartDate</span><span class="sxs-lookup"><span data-stu-id="60c42-151">-StartDate</span></span>
<span data-ttu-id="60c42-152">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="60c42-152">The effective start date of the credential usage.</span></span>
<span data-ttu-id="60c42-153">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="60c42-153">The default start date value is today.</span></span> <span data-ttu-id="60c42-154">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="60c42-154">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c42-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60c42-155">-Confirm</span></span>
<span data-ttu-id="60c42-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="60c42-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60c42-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60c42-157">-WhatIf</span></span>
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

### <span data-ttu-id="60c42-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c42-158">CommonParameters</span></span>
<span data-ttu-id="60c42-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60c42-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c42-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c42-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c42-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60c42-161">INPUTS</span></span>

### <span data-ttu-id="60c42-162">Ничего</span><span class="sxs-lookup"><span data-stu-id="60c42-162">None</span></span>
<span data-ttu-id="60c42-163">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="60c42-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60c42-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60c42-164">OUTPUTS</span></span>

### <span data-ttu-id="60c42-165">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="60c42-165">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="60c42-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="60c42-166">NOTES</span></span>
<span data-ttu-id="60c42-167">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="60c42-167">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="60c42-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60c42-168">RELATED LINKS</span></span>

[<span data-ttu-id="60c42-169">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="60c42-169">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="60c42-170">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="60c42-170">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="60c42-171">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="60c42-171">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="60c42-172">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="60c42-172">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="60c42-173">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="60c42-173">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="60c42-174">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="60c42-174">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="60c42-175">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="60c42-175">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

