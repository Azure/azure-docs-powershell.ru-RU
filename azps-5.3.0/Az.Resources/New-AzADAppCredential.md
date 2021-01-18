---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 8290ad3779c91565509833bbf41d7f9b37b07635
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505238"
---
# <span data-ttu-id="688a4-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="688a4-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="688a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="688a4-102">SYNOPSIS</span></span>
<span data-ttu-id="688a4-103">Добавляет учетные данные в существующее приложение.</span><span class="sxs-lookup"><span data-stu-id="688a4-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="688a4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="688a4-104">SYNTAX</span></span>

### <span data-ttu-id="688a4-105">ApplicationObjectIdWithPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="688a4-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="688a4-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="688a4-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="688a4-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="688a4-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="688a4-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="688a4-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="688a4-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="688a4-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="688a4-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="688a4-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="688a4-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="688a4-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="688a4-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="688a4-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="688a4-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="688a4-113">DESCRIPTION</span></span>
<span data-ttu-id="688a4-114">С New-AzADAppCredential можно добавить новые учетные данные или откатить учетные данные для приложения.</span><span class="sxs-lookup"><span data-stu-id="688a4-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="688a4-115">Приложение можно определить по его ИД или его ИД.</span><span class="sxs-lookup"><span data-stu-id="688a4-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="688a4-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="688a4-116">EXAMPLES</span></span>

### <span data-ttu-id="688a4-117">Пример 1. Создание учетных данных приложения с помощью пароля</span><span class="sxs-lookup"><span data-stu-id="688a4-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="688a4-118">В существующее приложение будет добавлен новый пароль с ид объекта '1f89cf81-0146-4f4e-beae-2007d0668416'.</span><span class="sxs-lookup"><span data-stu-id="688a4-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="688a4-119">Пример 2. Создание учетных данных приложения с помощью сертификата</span><span class="sxs-lookup"><span data-stu-id="688a4-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="688a4-120">Предоставленный общедоступный сертификат X509 (myapp.cer) с кодом приложения "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="688a4-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="688a4-121">Пример 3. Создание учетных данных приложения с помощью piping</span><span class="sxs-lookup"><span data-stu-id="688a4-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="688a4-122">Получает приложение с ид объекта "1f89cf81-0146-4f4e-beae-2007d0668416" и вертет ему New-AzADAppCredential, чтобы создать учетные данные приложения с заданным паролем.</span><span class="sxs-lookup"><span data-stu-id="688a4-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="688a4-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="688a4-123">PARAMETERS</span></span>

### <span data-ttu-id="688a4-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="688a4-124">-ApplicationId</span></span>
<span data-ttu-id="688a4-125">ИД приложения, в которое нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="688a4-125">The application id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="688a4-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="688a4-126">-ApplicationObject</span></span>
<span data-ttu-id="688a4-127">Объект приложения, к который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="688a4-127">The application object to add the credentials to.</span></span>

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

### <span data-ttu-id="688a4-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="688a4-128">-CertValue</span></span>
<span data-ttu-id="688a4-129">Значение асимметричного типа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="688a4-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="688a4-130">Он представляет собой 64-кодированный сертификат.</span><span class="sxs-lookup"><span data-stu-id="688a4-130">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="688a4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="688a4-131">-DefaultProfile</span></span>
<span data-ttu-id="688a4-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="688a4-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="688a4-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="688a4-133">-DisplayName</span></span>
<span data-ttu-id="688a4-134">Отображаемого имени приложения.</span><span class="sxs-lookup"><span data-stu-id="688a4-134">The display name of the application.</span></span>

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

### <span data-ttu-id="688a4-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="688a4-135">-EndDate</span></span>
<span data-ttu-id="688a4-136">Дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="688a4-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="688a4-137">Значение даты окончания по умолчанию составляет один год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="688a4-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="688a4-138">Для учетных данных асимметричного типа необходимо установить этот учетный данные в день, когда допустим сертификат X509, или до нее.</span><span class="sxs-lookup"><span data-stu-id="688a4-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="688a4-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="688a4-139">-ObjectId</span></span>
<span data-ttu-id="688a4-140">ИД объекта приложения, в который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="688a4-140">The object id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="688a4-141">-Password</span><span class="sxs-lookup"><span data-stu-id="688a4-141">-Password</span></span>
<span data-ttu-id="688a4-142">Пароль, который будет связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="688a4-142">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="688a4-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="688a4-143">-StartDate</span></span>
<span data-ttu-id="688a4-144">Начальную дату использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="688a4-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="688a4-145">По умолчанию дата начала является сегодняшним значением.</span><span class="sxs-lookup"><span data-stu-id="688a4-145">The default start date value is today.</span></span> <span data-ttu-id="688a4-146">Для учетных данных "асимметричного" типа это должно быть установлено в дату, начиная с даты действия сертификата X509, или после нее.</span><span class="sxs-lookup"><span data-stu-id="688a4-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="688a4-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="688a4-147">-Confirm</span></span>
<span data-ttu-id="688a4-148">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="688a4-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="688a4-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="688a4-149">-WhatIf</span></span>
<span data-ttu-id="688a4-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="688a4-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="688a4-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="688a4-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="688a4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="688a4-152">CommonParameters</span></span>
<span data-ttu-id="688a4-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="688a4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="688a4-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="688a4-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="688a4-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="688a4-155">INPUTS</span></span>

### <span data-ttu-id="688a4-156">System.String</span><span class="sxs-lookup"><span data-stu-id="688a4-156">System.String</span></span>

### <span data-ttu-id="688a4-157">System.Guid</span><span class="sxs-lookup"><span data-stu-id="688a4-157">System.Guid</span></span>

### <span data-ttu-id="688a4-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="688a4-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="688a4-159">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="688a4-159">System.Security.SecureString</span></span>

### <span data-ttu-id="688a4-160">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="688a4-160">System.DateTime</span></span>

## <span data-ttu-id="688a4-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="688a4-161">OUTPUTS</span></span>

### <span data-ttu-id="688a4-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="688a4-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="688a4-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="688a4-163">NOTES</span></span>

## <span data-ttu-id="688a4-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="688a4-164">RELATED LINKS</span></span>

[<span data-ttu-id="688a4-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="688a4-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="688a4-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="688a4-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="688a4-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="688a4-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

