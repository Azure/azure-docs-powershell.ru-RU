---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 46977fe6b2e6cf3c3811c7d9bbd49262b06cec54
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505231"
---
# <span data-ttu-id="a8573-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a8573-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="a8573-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8573-102">SYNOPSIS</span></span>
<span data-ttu-id="a8573-103">Добавляет учетные данные к существующей основной службе.</span><span class="sxs-lookup"><span data-stu-id="a8573-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="a8573-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8573-104">SYNTAX</span></span>

### <span data-ttu-id="a8573-105">SpObjectIdWithPasswordParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8573-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8573-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8573-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8573-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8573-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8573-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8573-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8573-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8573-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8573-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8573-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8573-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8573-111">DESCRIPTION</span></span>
<span data-ttu-id="a8573-112">Этот New-AzADSpCredential можно использовать для добавления новых учетных данных или для ската для основного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a8573-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="a8573-113">Это имя можно определить по имени объекта или основные службы.</span><span class="sxs-lookup"><span data-stu-id="a8573-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="a8573-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8573-114">EXAMPLES</span></span>

### <span data-ttu-id="a8573-115">Пример 1. Создание учетных данных для основной службы с помощью сгенерированного пароля</span><span class="sxs-lookup"><span data-stu-id="a8573-115">Example 1: Create a new service principal credential using a generated password</span></span>

```powershell
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="a8573-116">К существующей основной службе добавляется новый пароль с ид объекта '1f99cf81-0146-4f4e-beae-2007d0668476'.</span><span class="sxs-lookup"><span data-stu-id="a8573-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="a8573-117">Пример 2. Создание учетных данных для основной службы с помощью сертификата</span><span class="sxs-lookup"><span data-stu-id="a8573-117">Example 2: Create a new service principal credential using a certificate</span></span>

```powershell
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="a8573-118">Предоставленный общедоступный сертификат X509 в кодированном коде X509 (myapp.cer) добавляется к существующему основному службе с использованием его spN.</span><span class="sxs-lookup"><span data-stu-id="a8573-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="a8573-119">Пример 3. Создание учетных данных для основной службы с помощью piping</span><span class="sxs-lookup"><span data-stu-id="a8573-119">Example 3: Create a new service principal credential using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="a8573-120">Получает главную службу с ид объекта "1f99cf81-0146-4f4e-beae-2007d0668476" и вертет в New-AzADSpCredential, чтобы создать для этого директора-службы новые учетные данные с созданным паролем.</span><span class="sxs-lookup"><span data-stu-id="a8573-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="a8573-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8573-121">PARAMETERS</span></span>

### <span data-ttu-id="a8573-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="a8573-122">-CertValue</span></span>
<span data-ttu-id="a8573-123">Значение асимметричного типа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a8573-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="a8573-124">Он представляет собой 64-кодированный сертификат.</span><span class="sxs-lookup"><span data-stu-id="a8573-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="a8573-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8573-125">-DefaultProfile</span></span>
<span data-ttu-id="a8573-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a8573-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8573-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a8573-127">-EndDate</span></span>
<span data-ttu-id="a8573-128">Дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a8573-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="a8573-129">Значение даты окончания по умолчанию составляет один год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="a8573-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="a8573-130">Для учетных данных асимметричного типа необходимо установить этот учетный данные в день, когда допустим сертификат X509, или до нее.</span><span class="sxs-lookup"><span data-stu-id="a8573-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="a8573-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a8573-131">-ObjectId</span></span>
<span data-ttu-id="a8573-132">Object id of the service principal to add the credentials to.</span><span class="sxs-lookup"><span data-stu-id="a8573-132">The object id of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="a8573-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a8573-133">-ServicePrincipalName</span></span>
<span data-ttu-id="a8573-134">Имя (SPN) директора-службы, для которого нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="a8573-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="a8573-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="a8573-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="a8573-136">Объект-основной службы, к который нужно добавить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="a8573-136">The service principal object to add the credentials to.</span></span>

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

### <span data-ttu-id="a8573-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a8573-137">-StartDate</span></span>
<span data-ttu-id="a8573-138">Начальную дату использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="a8573-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="a8573-139">По умолчанию дата начала является сегодняшним значением.</span><span class="sxs-lookup"><span data-stu-id="a8573-139">The default start date value is today.</span></span>
<span data-ttu-id="a8573-140">Для учетных данных "асимметричного" типа это должно быть установлено в дату, начиная с даты действия сертификата X509, или после нее.</span><span class="sxs-lookup"><span data-stu-id="a8573-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="a8573-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8573-141">-Confirm</span></span>
<span data-ttu-id="a8573-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8573-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8573-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8573-143">-WhatIf</span></span>
<span data-ttu-id="a8573-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8573-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8573-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a8573-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8573-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8573-146">CommonParameters</span></span>
<span data-ttu-id="a8573-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8573-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8573-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8573-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8573-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8573-149">INPUTS</span></span>

### <span data-ttu-id="a8573-150">System.String</span><span class="sxs-lookup"><span data-stu-id="a8573-150">System.String</span></span>

### <span data-ttu-id="a8573-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a8573-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="a8573-152">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="a8573-152">System.DateTime</span></span>

## <span data-ttu-id="a8573-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8573-153">OUTPUTS</span></span>

### <span data-ttu-id="a8573-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="a8573-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="a8573-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="a8573-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="a8573-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8573-156">NOTES</span></span>

## <span data-ttu-id="a8573-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8573-157">RELATED LINKS</span></span>

[<span data-ttu-id="a8573-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a8573-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="a8573-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a8573-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="a8573-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a8573-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



