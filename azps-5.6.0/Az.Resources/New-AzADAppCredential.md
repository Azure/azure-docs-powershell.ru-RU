---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 1a80a5a2b6bb5e7af4d6467414feb3936377ea8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985606"
---
# <span data-ttu-id="dc48d-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="dc48d-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="dc48d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc48d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc48d-103">Добавляет учетные данные в существующее приложение.</span><span class="sxs-lookup"><span data-stu-id="dc48d-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="dc48d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc48d-104">SYNTAX</span></span>

### <span data-ttu-id="dc48d-105">ApplicationObjectIdWithPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc48d-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc48d-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc48d-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc48d-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc48d-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc48d-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc48d-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc48d-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc48d-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc48d-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc48d-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc48d-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc48d-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc48d-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc48d-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc48d-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc48d-113">DESCRIPTION</span></span>
<span data-ttu-id="dc48d-114">С New-AzADAppCredential можно добавить новые учетные данные или свести учетные данные для приложения.</span><span class="sxs-lookup"><span data-stu-id="dc48d-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="dc48d-115">Приложение можно определить по его ИД или его ИД.</span><span class="sxs-lookup"><span data-stu-id="dc48d-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="dc48d-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc48d-116">EXAMPLES</span></span>

### <span data-ttu-id="dc48d-117">Пример 1. Создание учетных данных приложения с помощью пароля</span><span class="sxs-lookup"><span data-stu-id="dc48d-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="dc48d-118">В существующее приложение будет добавлен новый пароль с ид объекта '1f89cf81-0146-4f4e-beae-2007d0668416'.</span><span class="sxs-lookup"><span data-stu-id="dc48d-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="dc48d-119">Пример 2. Создание учетных данных приложения с помощью сертификата</span><span class="sxs-lookup"><span data-stu-id="dc48d-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="dc48d-120">Предоставленный общедоступный сертификат X509 (myapp.cer) с кодом приложения "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="dc48d-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="dc48d-121">Пример 3. Создание учетных данных приложения с помощью piping</span><span class="sxs-lookup"><span data-stu-id="dc48d-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="dc48d-122">Получает приложение с ид объекта "1f89cf81-0146-4f4e-beae-2007d0668416" и вертет ему New-AzADAppCredential, чтобы создать учетные данные приложения с заданным паролем.</span><span class="sxs-lookup"><span data-stu-id="dc48d-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="dc48d-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc48d-123">PARAMETERS</span></span>

### <span data-ttu-id="dc48d-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dc48d-124">-ApplicationId</span></span>
<span data-ttu-id="dc48d-125">ИД приложения, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="dc48d-125">The application id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="dc48d-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="dc48d-126">-ApplicationObject</span></span>
<span data-ttu-id="dc48d-127">Объект приложения, к который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="dc48d-127">The application object to add the credentials to.</span></span>

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

### <span data-ttu-id="dc48d-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="dc48d-128">-CertValue</span></span>
<span data-ttu-id="dc48d-129">Значение асимметричного типа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="dc48d-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="dc48d-130">Он представляет собой 64-кодированный сертификат.</span><span class="sxs-lookup"><span data-stu-id="dc48d-130">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="dc48d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc48d-131">-DefaultProfile</span></span>
<span data-ttu-id="dc48d-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dc48d-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc48d-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dc48d-133">-DisplayName</span></span>
<span data-ttu-id="dc48d-134">Отображаемого имени приложения.</span><span class="sxs-lookup"><span data-stu-id="dc48d-134">The display name of the application.</span></span>

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

### <span data-ttu-id="dc48d-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="dc48d-135">-EndDate</span></span>
<span data-ttu-id="dc48d-136">Дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="dc48d-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="dc48d-137">Значение даты окончания по умолчанию составляет один год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="dc48d-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="dc48d-138">Для учетных данных "асимметричного" типа это должно быть задано в день, когда допустим сертификат X509 или раньше нее.</span><span class="sxs-lookup"><span data-stu-id="dc48d-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="dc48d-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dc48d-139">-ObjectId</span></span>
<span data-ttu-id="dc48d-140">ИД объекта приложения, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="dc48d-140">The object id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="dc48d-141">-Password</span><span class="sxs-lookup"><span data-stu-id="dc48d-141">-Password</span></span>
<span data-ttu-id="dc48d-142">Пароль, который будет связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="dc48d-142">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="dc48d-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="dc48d-143">-StartDate</span></span>
<span data-ttu-id="dc48d-144">Начальную дату использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="dc48d-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="dc48d-145">По умолчанию дата начала является сегодняшним значением.</span><span class="sxs-lookup"><span data-stu-id="dc48d-145">The default start date value is today.</span></span> <span data-ttu-id="dc48d-146">Для учетных данных "асимметричного" типа это должно быть установлено в дату, начиная с даты действия сертификата X509, или после нее.</span><span class="sxs-lookup"><span data-stu-id="dc48d-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="dc48d-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc48d-147">-Confirm</span></span>
<span data-ttu-id="dc48d-148">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dc48d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc48d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc48d-149">-WhatIf</span></span>
<span data-ttu-id="dc48d-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc48d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc48d-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc48d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc48d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc48d-152">CommonParameters</span></span>
<span data-ttu-id="dc48d-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc48d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc48d-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc48d-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc48d-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc48d-155">INPUTS</span></span>

### <span data-ttu-id="dc48d-156">System.String</span><span class="sxs-lookup"><span data-stu-id="dc48d-156">System.String</span></span>

### <span data-ttu-id="dc48d-157">System.Guid</span><span class="sxs-lookup"><span data-stu-id="dc48d-157">System.Guid</span></span>

### <span data-ttu-id="dc48d-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="dc48d-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="dc48d-159">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="dc48d-159">System.Security.SecureString</span></span>

### <span data-ttu-id="dc48d-160">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="dc48d-160">System.DateTime</span></span>

## <span data-ttu-id="dc48d-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc48d-161">OUTPUTS</span></span>

### <span data-ttu-id="dc48d-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="dc48d-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="dc48d-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc48d-163">NOTES</span></span>

## <span data-ttu-id="dc48d-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc48d-164">RELATED LINKS</span></span>

[<span data-ttu-id="dc48d-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="dc48d-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="dc48d-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="dc48d-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="dc48d-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="dc48d-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

