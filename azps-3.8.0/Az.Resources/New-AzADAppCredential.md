---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 8290ad3779c91565509833bbf41d7f9b37b07635
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074470"
---
# <span data-ttu-id="37141-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="37141-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="37141-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37141-102">SYNOPSIS</span></span>
<span data-ttu-id="37141-103">Добавляет учетные данные в существующее приложение.</span><span class="sxs-lookup"><span data-stu-id="37141-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="37141-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37141-104">SYNTAX</span></span>

### <span data-ttu-id="37141-105">ApplicationObjectIdWithPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37141-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37141-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="37141-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37141-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="37141-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37141-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="37141-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37141-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="37141-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37141-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="37141-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37141-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="37141-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37141-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="37141-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37141-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37141-113">DESCRIPTION</span></span>
<span data-ttu-id="37141-114">Командлет New-AzADAppCredential можно использовать для добавления новых учетных данных или для их отката для приложения.</span><span class="sxs-lookup"><span data-stu-id="37141-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="37141-115">Приложение определяется путем предоставления либо идентификатора объекта приложения, либо идентификатора приложения.</span><span class="sxs-lookup"><span data-stu-id="37141-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="37141-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37141-116">EXAMPLES</span></span>

### <span data-ttu-id="37141-117">Пример 1: создание новых учетных данных приложения с помощью пароля</span><span class="sxs-lookup"><span data-stu-id="37141-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="37141-118">Новые учетные данные пароля добавляются в существующее приложение с идентификатором объекта "1f89cf81-0146-4f4e-beae-2007d0668416".</span><span class="sxs-lookup"><span data-stu-id="37141-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="37141-119">Пример 2. Создание учетных данных приложения с помощью сертификата</span><span class="sxs-lookup"><span data-stu-id="37141-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="37141-120">Предоставленный общедоступный сертификат X509, закодированный с помощью Base64 ("MyApp. cer"), добавляется к существующему приложению с идентификатором приложения "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="37141-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="37141-121">Пример 3. Создание учетных данных приложения с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="37141-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="37141-122">Возвращает приложение с идентификатором объекта "1f89cf81-0146-4f4e-beae-2007d0668416" и каналами для создания новых учетных данных приложения для этого приложения с заданным паролем в New-AzADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="37141-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="37141-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37141-123">PARAMETERS</span></span>

### <span data-ttu-id="37141-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="37141-124">-ApplicationId</span></span>
<span data-ttu-id="37141-125">Идентификатор приложения, в которое нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="37141-125">The application id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37141-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="37141-126">-ApplicationObject</span></span>
<span data-ttu-id="37141-127">Объект приложения, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="37141-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37141-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="37141-128">-CertValue</span></span>
<span data-ttu-id="37141-129">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="37141-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="37141-130">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="37141-130">It represents the base 64 encoded certificate.</span></span>

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

```yaml
Type: System.String
Parameter Sets: DisplayNameWithCertValueParameterSet, ApplicationObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37141-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37141-131">-DefaultProfile</span></span>
<span data-ttu-id="37141-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="37141-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37141-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="37141-133">-DisplayName</span></span>
<span data-ttu-id="37141-134">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="37141-134">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithPasswordParameterSet, DisplayNameWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37141-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="37141-135">-EndDate</span></span>
<span data-ttu-id="37141-136">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="37141-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="37141-137">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="37141-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="37141-138">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="37141-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="37141-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="37141-139">-ObjectId</span></span>
<span data-ttu-id="37141-140">Идентификатор объекта приложения, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="37141-140">The object id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="37141-141">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="37141-141">-Password</span></span>
<span data-ttu-id="37141-142">Пароль, который должен быть связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="37141-142">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: DisplayNameWithPasswordParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37141-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="37141-143">-StartDate</span></span>
<span data-ttu-id="37141-144">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="37141-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="37141-145">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="37141-145">The default start date value is today.</span></span> <span data-ttu-id="37141-146">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="37141-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="37141-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37141-147">-Confirm</span></span>
<span data-ttu-id="37141-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="37141-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37141-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37141-149">-WhatIf</span></span>
<span data-ttu-id="37141-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="37141-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37141-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="37141-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37141-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37141-152">CommonParameters</span></span>
<span data-ttu-id="37141-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37141-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37141-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37141-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37141-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37141-155">INPUTS</span></span>

### <span data-ttu-id="37141-156">System. String</span><span class="sxs-lookup"><span data-stu-id="37141-156">System.String</span></span>

### <span data-ttu-id="37141-157">System. GUID</span><span class="sxs-lookup"><span data-stu-id="37141-157">System.Guid</span></span>

### <span data-ttu-id="37141-158">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="37141-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="37141-159">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="37141-159">System.Security.SecureString</span></span>

### <span data-ttu-id="37141-160">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="37141-160">System.DateTime</span></span>

## <span data-ttu-id="37141-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37141-161">OUTPUTS</span></span>

### <span data-ttu-id="37141-162">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="37141-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="37141-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="37141-163">NOTES</span></span>

## <span data-ttu-id="37141-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37141-164">RELATED LINKS</span></span>

[<span data-ttu-id="37141-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="37141-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="37141-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="37141-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="37141-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="37141-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

