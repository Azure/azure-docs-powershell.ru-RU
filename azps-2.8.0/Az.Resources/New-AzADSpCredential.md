---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: af2eb05e627af1b88948b2c1be0229eb6680254c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904046"
---
# <span data-ttu-id="078fe-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="078fe-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="078fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="078fe-102">SYNOPSIS</span></span>
<span data-ttu-id="078fe-103">Добавление учетных данных к существующему субъекту-службе.</span><span class="sxs-lookup"><span data-stu-id="078fe-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="078fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="078fe-104">SYNTAX</span></span>

### <span data-ttu-id="078fe-105">SpObjectIdWithPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="078fe-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="078fe-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="078fe-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="078fe-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="078fe-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="078fe-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="078fe-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="078fe-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="078fe-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="078fe-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="078fe-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="078fe-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="078fe-111">DESCRIPTION</span></span>
<span data-ttu-id="078fe-112">Командлет New-AzADSpCredential можно использовать для добавления новых учетных данных или для вызаписи учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="078fe-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="078fe-113">Субъект-служба определяется указанием либо идентификатора объекта, либо имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="078fe-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="078fe-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="078fe-114">EXAMPLES</span></span>

### <span data-ttu-id="078fe-115">Пример 1. Создание учетных данных субъектов-служб с помощью сгенерированного пароля</span><span class="sxs-lookup"><span data-stu-id="078fe-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="078fe-116">Новые учетные данные пароля добавляются к существующему субъекту-службе с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="078fe-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="078fe-117">Пример 2. Создание учетных данных субъектов-служб с помощью сертификата</span><span class="sxs-lookup"><span data-stu-id="078fe-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="078fe-118">Предоставленный общедоступный сертификат X509, закодированный с помощью Base64 ("MyApp. cer"), добавляется к существующему субъекту-службе, используя его SPN.</span><span class="sxs-lookup"><span data-stu-id="078fe-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="078fe-119">Пример 3: создание учетных данных субъекта-службы с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="078fe-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="078fe-120">Возвращает субъекта-службы с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476" и каналами, которые нужно использовать в New-AzADSpCredential для создания учетных данных субъекта-службы для этого субъекта-службы с созданным паролем.</span><span class="sxs-lookup"><span data-stu-id="078fe-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="078fe-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="078fe-121">PARAMETERS</span></span>

### <span data-ttu-id="078fe-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="078fe-122">-CertValue</span></span>
<span data-ttu-id="078fe-123">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="078fe-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="078fe-124">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="078fe-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fe-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="078fe-125">-DefaultProfile</span></span>
<span data-ttu-id="078fe-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="078fe-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="078fe-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="078fe-127">-EndDate</span></span>
<span data-ttu-id="078fe-128">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="078fe-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="078fe-129">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="078fe-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="078fe-130">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="078fe-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fe-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="078fe-131">-ObjectId</span></span>
<span data-ttu-id="078fe-132">Идентификатор объекта субъекта-службы, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="078fe-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fe-133">-Намерено</span><span class="sxs-lookup"><span data-stu-id="078fe-133">-ServicePrincipalName</span></span>
<span data-ttu-id="078fe-134">Имя субъекта-службы, в которую нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="078fe-134">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fe-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="078fe-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="078fe-136">Объект субъекта-службы, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="078fe-136">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="078fe-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="078fe-137">-StartDate</span></span>
<span data-ttu-id="078fe-138">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="078fe-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="078fe-139">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="078fe-139">The default start date value is today.</span></span>
<span data-ttu-id="078fe-140">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="078fe-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078fe-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="078fe-141">-Confirm</span></span>
<span data-ttu-id="078fe-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="078fe-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="078fe-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="078fe-143">-WhatIf</span></span>
<span data-ttu-id="078fe-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="078fe-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="078fe-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="078fe-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="078fe-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="078fe-146">CommonParameters</span></span>
<span data-ttu-id="078fe-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="078fe-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="078fe-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="078fe-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="078fe-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="078fe-149">INPUTS</span></span>

### <span data-ttu-id="078fe-150">System. String</span><span class="sxs-lookup"><span data-stu-id="078fe-150">System.String</span></span>

### <span data-ttu-id="078fe-151">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="078fe-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="078fe-152">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="078fe-152">System.DateTime</span></span>

## <span data-ttu-id="078fe-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="078fe-153">OUTPUTS</span></span>

### <span data-ttu-id="078fe-154">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="078fe-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="078fe-155">Microsoft. Azure. Commands. Resources. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="078fe-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="078fe-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="078fe-156">NOTES</span></span>

## <span data-ttu-id="078fe-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="078fe-157">RELATED LINKS</span></span>

[<span data-ttu-id="078fe-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="078fe-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="078fe-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="078fe-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="078fe-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="078fe-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



