---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: bf2a42df42a343d9745cb55f4d72463513b44dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566132"
---
# <span data-ttu-id="e4232-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e4232-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="e4232-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4232-102">SYNOPSIS</span></span>
<span data-ttu-id="e4232-103">Добавление учетных данных к существующему субъекту-службе.</span><span class="sxs-lookup"><span data-stu-id="e4232-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4232-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4232-104">SYNTAX</span></span>

### <span data-ttu-id="e4232-105">SpObjectIdWithPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e4232-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4232-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4232-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4232-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4232-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4232-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4232-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4232-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4232-109">DESCRIPTION</span></span>
<span data-ttu-id="e4232-110">Командлет New-AzureRmADSpCredential можно использовать для добавления новых учетных данных или для вызаписи учетных данных субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e4232-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="e4232-111">Субъект-служба определяется указанием либо идентификатора объекта, либо имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e4232-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="e4232-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4232-112">EXAMPLES</span></span>

### <span data-ttu-id="e4232-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e4232-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $SecureStringPassword
```

<span data-ttu-id="e4232-114">Новые учетные данные пароля добавляются к существующему субъекту-службе.</span><span class="sxs-lookup"><span data-stu-id="e4232-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="e4232-115">В этом примере предоставленное значение пароля добавляется к субъекту-службы с помощью objectId.</span><span class="sxs-lookup"><span data-stu-id="e4232-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="e4232-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e4232-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="e4232-117">Новые учетные данные ключа добавляются к существующему субъекту-службе.</span><span class="sxs-lookup"><span data-stu-id="e4232-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="e4232-118">В этом примере предоставленный общедоступный сертификат X.509, закодированный с помощью Base64 ("MyApp. cer"), добавляется для субъекта-службы с использованием его SPN.</span><span class="sxs-lookup"><span data-stu-id="e4232-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="e4232-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e4232-119">Example 3</span></span>

```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="e4232-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4232-120">PARAMETERS</span></span>

### <span data-ttu-id="e4232-121">-CertValue</span><span class="sxs-lookup"><span data-stu-id="e4232-121">-CertValue</span></span>
<span data-ttu-id="e4232-122">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="e4232-122">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="e4232-123">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="e4232-123">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4232-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4232-124">-DefaultProfile</span></span>
<span data-ttu-id="e4232-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e4232-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4232-126">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e4232-126">-EndDate</span></span>
<span data-ttu-id="e4232-127">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e4232-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="e4232-128">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="e4232-128">The default end date value is one year from today.</span></span> <span data-ttu-id="e4232-129">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="e4232-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="e4232-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e4232-130">-ObjectId</span></span>
<span data-ttu-id="e4232-131">Идентификатор объекта субъекта-службы, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e4232-131">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4232-132">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="e4232-132">-Password</span></span>
<span data-ttu-id="e4232-133">Пароль, который должен быть связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="e4232-133">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4232-134">-Намерено</span><span class="sxs-lookup"><span data-stu-id="e4232-134">-ServicePrincipalName</span></span>
<span data-ttu-id="e4232-135">Имя субъекта-службы, в которую нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e4232-135">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4232-136">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e4232-136">-StartDate</span></span>
<span data-ttu-id="e4232-137">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="e4232-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="e4232-138">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="e4232-138">The default start date value is today.</span></span> <span data-ttu-id="e4232-139">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="e4232-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="e4232-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4232-140">-Confirm</span></span>
<span data-ttu-id="e4232-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e4232-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4232-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4232-142">-WhatIf</span></span>
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

### <span data-ttu-id="e4232-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4232-143">CommonParameters</span></span>
<span data-ttu-id="e4232-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4232-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4232-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4232-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4232-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4232-146">INPUTS</span></span>

### <span data-ttu-id="e4232-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="e4232-147">None</span></span>
<span data-ttu-id="e4232-148">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e4232-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4232-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4232-149">OUTPUTS</span></span>

### <span data-ttu-id="e4232-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="e4232-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="e4232-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4232-151">NOTES</span></span>

## <span data-ttu-id="e4232-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4232-152">RELATED LINKS</span></span>

[<span data-ttu-id="e4232-153">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e4232-153">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="e4232-154">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e4232-154">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="e4232-155">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e4232-155">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



