---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: 814da56d9b925e19deac81dad886604d562e05e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734782"
---
# <span data-ttu-id="f4484-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f4484-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="f4484-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4484-102">SYNOPSIS</span></span>
<span data-ttu-id="f4484-103">Добавление учетных данных к существующему субъекту-службе.</span><span class="sxs-lookup"><span data-stu-id="f4484-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4484-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4484-104">SYNTAX</span></span>

### <span data-ttu-id="f4484-105">SpObjectIdWithPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4484-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4484-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4484-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4484-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4484-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4484-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4484-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4484-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4484-109">DESCRIPTION</span></span>
<span data-ttu-id="f4484-110">Командлет New-AzureRmADSpCredential можно использовать для добавления новых учетных данных или для вызаписи учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="f4484-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="f4484-111">Субъект-служба определяется указанием либо идентификатора объекта, либо имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="f4484-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="f4484-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4484-112">EXAMPLES</span></span>

### <span data-ttu-id="f4484-113">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f4484-113">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password "P@ssw0rd!"
```

<span data-ttu-id="f4484-114">Новые учетные данные пароля добавляются к существующему субъекту-службе.</span><span class="sxs-lookup"><span data-stu-id="f4484-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="f4484-115">В этом примере предоставленное значение пароля добавляется к субъекту-службы с помощью objectId.</span><span class="sxs-lookup"><span data-stu-id="f4484-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="f4484-116">--------------------------Пример 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f4484-116">--------------------------  Example 2  --------------------------</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="f4484-117">Новые учетные данные ключа добавляются к существующему субъекту-службе.</span><span class="sxs-lookup"><span data-stu-id="f4484-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="f4484-118">В этом примере предоставленный общедоступный сертификат X.509, закодированный с помощью Base64 ("MyApp. cer"), добавляется для субъекта-службы с использованием его SPN.</span><span class="sxs-lookup"><span data-stu-id="f4484-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="f4484-119">--------------------------Пример 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="f4484-119">--------------------------  Example 3  --------------------------</span></span>
<span data-ttu-id="f4484-120">@ {абзац = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="f4484-120">@{paragraph=PS C:\\\>}</span></span>







```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="f4484-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4484-121">PARAMETERS</span></span>

### <span data-ttu-id="f4484-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="f4484-122">-CertValue</span></span>
<span data-ttu-id="f4484-123">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="f4484-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="f4484-124">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="f4484-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="f4484-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="f4484-125">-EndDate</span></span>
<span data-ttu-id="f4484-126">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="f4484-126">The effective end date of the credential usage.</span></span>
<span data-ttu-id="f4484-127">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="f4484-127">The default end date value is one year from today.</span></span> <span data-ttu-id="f4484-128">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="f4484-128">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="f4484-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f4484-129">-ObjectId</span></span>
<span data-ttu-id="f4484-130">Идентификатор объекта субъекта-службы, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="f4484-130">The object id of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="f4484-131">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="f4484-131">-Password</span></span>
<span data-ttu-id="f4484-132">Пароль, который должен быть связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="f4484-132">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4484-133">-Намерено</span><span class="sxs-lookup"><span data-stu-id="f4484-133">-ServicePrincipalName</span></span>
<span data-ttu-id="f4484-134">Имя субъекта-службы, в которую нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="f4484-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="f4484-135">-StartDate</span><span class="sxs-lookup"><span data-stu-id="f4484-135">-StartDate</span></span>
<span data-ttu-id="f4484-136">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="f4484-136">The effective start date of the credential usage.</span></span>
<span data-ttu-id="f4484-137">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="f4484-137">The default start date value is today.</span></span> <span data-ttu-id="f4484-138">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="f4484-138">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="f4484-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4484-139">-Confirm</span></span>
<span data-ttu-id="f4484-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4484-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4484-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4484-141">-WhatIf</span></span>
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

### <span data-ttu-id="f4484-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4484-142">-DefaultProfile</span></span>
<span data-ttu-id="f4484-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4484-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4484-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4484-144">CommonParameters</span></span>
<span data-ttu-id="f4484-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4484-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4484-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4484-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4484-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4484-147">INPUTS</span></span>

## <span data-ttu-id="f4484-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4484-148">OUTPUTS</span></span>

### <span data-ttu-id="f4484-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="f4484-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="f4484-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4484-150">NOTES</span></span>

## <span data-ttu-id="f4484-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4484-151">RELATED LINKS</span></span>

[<span data-ttu-id="f4484-152">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f4484-152">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="f4484-153">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f4484-153">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="f4484-154">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f4484-154">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



