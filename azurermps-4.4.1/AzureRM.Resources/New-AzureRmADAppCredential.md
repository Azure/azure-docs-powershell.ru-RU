---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: 15b3e3fd90a7bacf87062bc12269ca2853276370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569231"
---
# <span data-ttu-id="c097f-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c097f-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="c097f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c097f-102">SYNOPSIS</span></span>
<span data-ttu-id="c097f-103">Добавляет учетные данные в существующее приложение.</span><span class="sxs-lookup"><span data-stu-id="c097f-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c097f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c097f-104">SYNTAX</span></span>

### <span data-ttu-id="c097f-105">ApplicationObjectIdWithPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c097f-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c097f-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c097f-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c097f-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="c097f-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c097f-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="c097f-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c097f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c097f-109">DESCRIPTION</span></span>
<span data-ttu-id="c097f-110">Командлет New-AzureRmADAppCredential можно использовать для добавления новых учетных данных или для их отката для приложения.</span><span class="sxs-lookup"><span data-stu-id="c097f-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="c097f-111">Приложение определяется путем предоставления либо идентификатора объекта приложения, либо идентификатора приложения.</span><span class="sxs-lookup"><span data-stu-id="c097f-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="c097f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c097f-112">EXAMPLES</span></span>

### <span data-ttu-id="c097f-113">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c097f-113">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password P@ssw0rd!
```

<span data-ttu-id="c097f-114">Новые учетные данные пароля добавляются в существующее приложение.</span><span class="sxs-lookup"><span data-stu-id="c097f-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="c097f-115">В этом примере предоставленное значение пароля добавляется в приложение с помощью идентификатора объекта Application.</span><span class="sxs-lookup"><span data-stu-id="c097f-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="c097f-116">--------------------------Пример 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c097f-116">--------------------------  Example 2  --------------------------</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="c097f-117">Новые учетные данные ключа добавляются в существующее приложение.</span><span class="sxs-lookup"><span data-stu-id="c097f-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="c097f-118">В этом примере предоставленный общедоступный сертификат X.509 с кодировкой base64 ("MyApp. cer") добавляется в приложение с помощью приложения applicationId.</span><span class="sxs-lookup"><span data-stu-id="c097f-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="c097f-119">--------------------------Пример 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="c097f-119">--------------------------  Example 3  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="c097f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c097f-120">PARAMETERS</span></span>

### <span data-ttu-id="c097f-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c097f-121">-ApplicationId</span></span>
<span data-ttu-id="c097f-122">Идентификатор приложения, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c097f-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c097f-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="c097f-123">-CertValue</span></span>
<span data-ttu-id="c097f-124">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="c097f-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="c097f-125">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="c097f-125">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c097f-126">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c097f-126">-EndDate</span></span>
<span data-ttu-id="c097f-127">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c097f-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="c097f-128">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="c097f-128">The default end date value is one year from today.</span></span> <span data-ttu-id="c097f-129">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="c097f-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="c097f-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c097f-130">-ObjectId</span></span>
<span data-ttu-id="c097f-131">Идентификатор объекта приложения, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c097f-131">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c097f-132">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="c097f-132">-Password</span></span>
<span data-ttu-id="c097f-133">Пароль, который должен быть связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="c097f-133">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c097f-134">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c097f-134">-StartDate</span></span>
<span data-ttu-id="c097f-135">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c097f-135">The effective start date of the credential usage.</span></span>
<span data-ttu-id="c097f-136">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="c097f-136">The default start date value is today.</span></span>
<span data-ttu-id="c097f-137">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="c097f-137">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="c097f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c097f-138">-Confirm</span></span>
<span data-ttu-id="c097f-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c097f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c097f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c097f-140">-WhatIf</span></span>
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

### <span data-ttu-id="c097f-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c097f-141">-DefaultProfile</span></span>
<span data-ttu-id="c097f-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c097f-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c097f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c097f-143">CommonParameters</span></span>
<span data-ttu-id="c097f-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c097f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c097f-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c097f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c097f-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c097f-146">INPUTS</span></span>

## <span data-ttu-id="c097f-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c097f-147">OUTPUTS</span></span>

### <span data-ttu-id="c097f-148">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="c097f-148">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="c097f-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="c097f-149">NOTES</span></span>

## <span data-ttu-id="c097f-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c097f-150">RELATED LINKS</span></span>

[<span data-ttu-id="c097f-151">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c097f-151">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="c097f-152">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c097f-152">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="c097f-153">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c097f-153">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

