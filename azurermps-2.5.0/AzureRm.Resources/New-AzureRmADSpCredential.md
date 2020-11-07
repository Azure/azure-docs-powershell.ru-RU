---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: 2f4a5e19f9b563361b526fab386c068fe65ce6ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914749"
---
# <span data-ttu-id="a5f61-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a5f61-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="a5f61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5f61-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f61-103">Добавление учетных данных к существующему субъекту-службе.</span><span class="sxs-lookup"><span data-stu-id="a5f61-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5f61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5f61-104">SYNTAX</span></span>

### <span data-ttu-id="a5f61-105">SpObjectIdWithPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5f61-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <Guid> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5f61-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5f61-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5f61-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5f61-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5f61-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5f61-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5f61-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5f61-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5f61-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5f61-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5f61-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5f61-111">DESCRIPTION</span></span>
<span data-ttu-id="a5f61-112">Командлет New-AzureRmADSpCredential можно использовать для добавления новых учетных данных или для вызаписи учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="a5f61-112">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="a5f61-113">Субъект-служба определяется указанием либо идентификатора объекта, либо имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="a5f61-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="a5f61-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5f61-114">EXAMPLES</span></span>

### <span data-ttu-id="a5f61-115">Пример 1. Создание учетных данных субъектов-служб с помощью сгенерированного пароля</span><span class="sxs-lookup"><span data-stu-id="a5f61-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="a5f61-116">Новые учетные данные пароля добавляются к существующему субъекту-службе с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="a5f61-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="a5f61-117">Пример 2. Создание учетных данных субъектов-служб с помощью сертификата</span><span class="sxs-lookup"><span data-stu-id="a5f61-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="a5f61-118">Предоставленный общедоступный сертификат X509, закодированный с помощью Base64 ("MyApp. cer"), добавляется к существующему субъекту-службе, используя его SPN.</span><span class="sxs-lookup"><span data-stu-id="a5f61-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="a5f61-119">Пример 3: создание учетных данных субъекта-службы с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="a5f61-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzureRmADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="a5f61-120">Возвращает субъекта-службы с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476" и каналами, которые нужно использовать в New-AzureRmADSpCredential для создания учетных данных субъекта-службы для этого субъекта-службы с созданным паролем.</span><span class="sxs-lookup"><span data-stu-id="a5f61-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzureRmADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="a5f61-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5f61-121">PARAMETERS</span></span>

### <span data-ttu-id="a5f61-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="a5f61-122">-CertValue</span></span>
<span data-ttu-id="a5f61-123">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="a5f61-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="a5f61-124">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="a5f61-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="a5f61-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f61-125">-DefaultProfile</span></span>
<span data-ttu-id="a5f61-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a5f61-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f61-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a5f61-127">-EndDate</span></span>
<span data-ttu-id="a5f61-128">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a5f61-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="a5f61-129">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="a5f61-129">The default end date value is one year from today.</span></span> <span data-ttu-id="a5f61-130">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="a5f61-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="a5f61-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a5f61-131">-ObjectId</span></span>
<span data-ttu-id="a5f61-132">Идентификатор объекта субъекта-службы, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="a5f61-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f61-133">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="a5f61-133">-Password</span></span>
<span data-ttu-id="a5f61-134">Пароль, который должен быть связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="a5f61-134">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f61-135">-Намерено</span><span class="sxs-lookup"><span data-stu-id="a5f61-135">-ServicePrincipalName</span></span>
<span data-ttu-id="a5f61-136">Имя субъекта-службы, в которую нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="a5f61-136">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="a5f61-137">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="a5f61-137">-ServicePrincipalObject</span></span>
<span data-ttu-id="a5f61-138">Объект субъекта-службы, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="a5f61-138">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f61-139">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a5f61-139">-StartDate</span></span>
<span data-ttu-id="a5f61-140">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a5f61-140">The effective start date of the credential usage.</span></span>
<span data-ttu-id="a5f61-141">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="a5f61-141">The default start date value is today.</span></span> <span data-ttu-id="a5f61-142">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="a5f61-142">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="a5f61-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5f61-143">-Confirm</span></span>
<span data-ttu-id="a5f61-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a5f61-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5f61-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5f61-145">-WhatIf</span></span>
<span data-ttu-id="a5f61-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a5f61-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5f61-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a5f61-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5f61-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f61-148">CommonParameters</span></span>
<span data-ttu-id="a5f61-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5f61-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f61-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5f61-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f61-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5f61-151">INPUTS</span></span>

### <span data-ttu-id="a5f61-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a5f61-152">System.Guid</span></span>

### <span data-ttu-id="a5f61-153">System. String</span><span class="sxs-lookup"><span data-stu-id="a5f61-153">System.String</span></span>

### <span data-ttu-id="a5f61-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a5f61-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="a5f61-155">Параметры: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5f61-155">Parameters: ServicePrincipalObject (ByValue)</span></span>

### <span data-ttu-id="a5f61-156">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a5f61-156">System.Security.SecureString</span></span>

### <span data-ttu-id="a5f61-157">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="a5f61-157">System.DateTime</span></span>

## <span data-ttu-id="a5f61-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5f61-158">OUTPUTS</span></span>

### <span data-ttu-id="a5f61-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="a5f61-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="a5f61-160">Microsoft. Azure. Commands. Resources. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="a5f61-160">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="a5f61-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5f61-161">NOTES</span></span>

## <span data-ttu-id="a5f61-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5f61-162">RELATED LINKS</span></span>

[<span data-ttu-id="a5f61-163">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a5f61-163">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="a5f61-164">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a5f61-164">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="a5f61-165">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a5f61-165">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



