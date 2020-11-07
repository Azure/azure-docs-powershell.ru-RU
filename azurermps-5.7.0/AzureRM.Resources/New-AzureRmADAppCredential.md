---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: d4d7cb0a188b4c00c4ea0c07140b3360c98805aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733228"
---
# <span data-ttu-id="2658d-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2658d-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="2658d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2658d-102">SYNOPSIS</span></span>
<span data-ttu-id="2658d-103">Добавляет учетные данные в существующее приложение.</span><span class="sxs-lookup"><span data-stu-id="2658d-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2658d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2658d-104">SYNTAX</span></span>

### <span data-ttu-id="2658d-105">ApplicationObjectIdWithPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2658d-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2658d-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="2658d-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2658d-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="2658d-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2658d-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="2658d-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2658d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2658d-109">DESCRIPTION</span></span>
<span data-ttu-id="2658d-110">Командлет New-AzureRmADAppCredential можно использовать для добавления новых учетных данных или для их отката для приложения.</span><span class="sxs-lookup"><span data-stu-id="2658d-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="2658d-111">Приложение определяется путем предоставления либо идентификатора объекта приложения, либо идентификатора приложения.</span><span class="sxs-lookup"><span data-stu-id="2658d-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="2658d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2658d-112">EXAMPLES</span></span>

### <span data-ttu-id="2658d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2658d-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="2658d-114">Новые учетные данные пароля добавляются в существующее приложение.</span><span class="sxs-lookup"><span data-stu-id="2658d-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="2658d-115">В этом примере предоставленное значение пароля добавляется в приложение с помощью идентификатора объекта Application.</span><span class="sxs-lookup"><span data-stu-id="2658d-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="2658d-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2658d-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="2658d-117">Новые учетные данные ключа добавляются в существующее приложение.</span><span class="sxs-lookup"><span data-stu-id="2658d-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="2658d-118">В этом примере предоставленный общедоступный сертификат X.509 с кодировкой base64 ("MyApp. cer") добавляется в приложение с помощью приложения applicationId.</span><span class="sxs-lookup"><span data-stu-id="2658d-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="2658d-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2658d-119">Example 3</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="2658d-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2658d-120">PARAMETERS</span></span>

### <span data-ttu-id="2658d-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2658d-121">-ApplicationId</span></span>
<span data-ttu-id="2658d-122">Идентификатор приложения, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="2658d-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2658d-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="2658d-123">-CertValue</span></span>
<span data-ttu-id="2658d-124">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="2658d-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="2658d-125">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="2658d-125">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2658d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2658d-126">-DefaultProfile</span></span>
<span data-ttu-id="2658d-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2658d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2658d-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2658d-128">-EndDate</span></span>
<span data-ttu-id="2658d-129">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="2658d-129">The effective end date of the credential usage.</span></span>
<span data-ttu-id="2658d-130">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="2658d-130">The default end date value is one year from today.</span></span> <span data-ttu-id="2658d-131">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="2658d-131">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2658d-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2658d-132">-ObjectId</span></span>
<span data-ttu-id="2658d-133">Идентификатор объекта приложения, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="2658d-133">The object id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2658d-134">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="2658d-134">-Password</span></span>
<span data-ttu-id="2658d-135">Пароль, который должен быть связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="2658d-135">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2658d-136">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2658d-136">-StartDate</span></span>
<span data-ttu-id="2658d-137">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="2658d-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="2658d-138">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="2658d-138">The default start date value is today.</span></span>
<span data-ttu-id="2658d-139">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="2658d-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2658d-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2658d-140">-Confirm</span></span>
<span data-ttu-id="2658d-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2658d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2658d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2658d-142">-WhatIf</span></span>
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

### <span data-ttu-id="2658d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2658d-143">CommonParameters</span></span>
<span data-ttu-id="2658d-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2658d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2658d-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2658d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2658d-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2658d-146">INPUTS</span></span>

### <span data-ttu-id="2658d-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="2658d-147">None</span></span>
<span data-ttu-id="2658d-148">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2658d-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2658d-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2658d-149">OUTPUTS</span></span>

### <span data-ttu-id="2658d-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="2658d-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="2658d-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="2658d-151">NOTES</span></span>

## <span data-ttu-id="2658d-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2658d-152">RELATED LINKS</span></span>

[<span data-ttu-id="2658d-153">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2658d-153">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="2658d-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2658d-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="2658d-155">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="2658d-155">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

