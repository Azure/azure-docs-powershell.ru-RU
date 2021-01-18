---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507176"
---
# <span data-ttu-id="80a31-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="80a31-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="80a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80a31-102">SYNOPSIS</span></span>
<span data-ttu-id="80a31-103">Обновляет атрибуты секретного секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="80a31-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="80a31-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="80a31-104">SYNTAX</span></span>

### <span data-ttu-id="80a31-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80a31-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a31-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="80a31-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80a31-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80a31-107">DESCRIPTION</span></span>
<span data-ttu-id="80a31-108">С **его** нажатием можно изменять атрибуты секретного сейфа.</span><span class="sxs-lookup"><span data-stu-id="80a31-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="80a31-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="80a31-109">EXAMPLES</span></span>

### <span data-ttu-id="80a31-110">Пример 1. Изменение атрибутов секретного</span><span class="sxs-lookup"><span data-stu-id="80a31-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

<span data-ttu-id="80a31-111">Первые четыре команды определяют атрибуты для даты окончания срока действия, даты NotBefore, тегов и типа контекста, а также сохраняют атрибуты в переменных.</span><span class="sxs-lookup"><span data-stu-id="80a31-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="80a31-112">Итоговая команда изменяет атрибуты секретного отдела кадров в хранилище ключей ContosoVault с использованием хранимых переменных.</span><span class="sxs-lookup"><span data-stu-id="80a31-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="80a31-113">Пример 2. Удаление тегов и типа контента для секретного</span><span class="sxs-lookup"><span data-stu-id="80a31-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="80a31-114">Эта команда удаляет теги и тип контента для указанной версии секретного отдела кадров в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="80a31-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="80a31-115">Пример 3. Отключение текущей версии секретов, имя которых начинается с ИТ</span><span class="sxs-lookup"><span data-stu-id="80a31-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="80a31-116">Первая команда сохраняет строковые значения Contoso в $Vault переменной.</span><span class="sxs-lookup"><span data-stu-id="80a31-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="80a31-117">Вторая команда сохраняет строковые значения ИТ в $Prefix переменной.</span><span class="sxs-lookup"><span data-stu-id="80a31-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="80a31-118">Третья команда использует Get-AzKeyVaultSecret командлет, чтобы получить секрет в указанном хранилище ключей, а затем передает эти секреты **командлету Where-Object.**</span><span class="sxs-lookup"><span data-stu-id="80a31-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="80a31-119">С **помощью cmdlet Where-Object** можно отфильтровать секреты имен, которые начинаются с ИТ-символов.</span><span class="sxs-lookup"><span data-stu-id="80a31-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="80a31-120">Эта команда передает секрет, который соответствует фильтру Update-AzKeyVaultSecret командлету, который отключает их.</span><span class="sxs-lookup"><span data-stu-id="80a31-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="80a31-121">Пример 4. Настройка ContentType для всех версий секретного</span><span class="sxs-lookup"><span data-stu-id="80a31-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="80a31-122">Первые три команды определяют строковые переменные, которые нужно использовать для параметров *VaultName,* *Name* и *ContentType.*</span><span class="sxs-lookup"><span data-stu-id="80a31-122">The first three commands define string variables to use for the *VaultName*, *Name*, and *ContentType* parameters.</span></span> <span data-ttu-id="80a31-123">Четвертая команда использует Get-AzKeyVaultKey для получения указанных клавиш, а затем передает их Update-AzKeyVaultSecret командлету, чтобы выбрать тип контента XML.</span><span class="sxs-lookup"><span data-stu-id="80a31-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="80a31-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80a31-124">PARAMETERS</span></span>

### <span data-ttu-id="80a31-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="80a31-125">-ContentType</span></span>
<span data-ttu-id="80a31-126">Тип контента секретного.</span><span class="sxs-lookup"><span data-stu-id="80a31-126">Secret's content type.</span></span>
<span data-ttu-id="80a31-127">Если не указано, существующее значение типа контента секретного содержимого не изменяется.</span><span class="sxs-lookup"><span data-stu-id="80a31-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="80a31-128">Удалите существующее значение типа контента, указав пустую строку.</span><span class="sxs-lookup"><span data-stu-id="80a31-128">Remove the existing content type value by specifying an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a31-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a31-129">-DefaultProfile</span></span>
<span data-ttu-id="80a31-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80a31-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80a31-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="80a31-131">-Enable</span></span>
<span data-ttu-id="80a31-132">При этом в нее можно включить секрет, если значение является истинным.</span><span class="sxs-lookup"><span data-stu-id="80a31-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="80a31-133">Отключать секрет, если значение ложно.</span><span class="sxs-lookup"><span data-stu-id="80a31-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="80a31-134">Если он не задан, существующее значение состояния секретного состояния (включено или отключено) не изменяется.</span><span class="sxs-lookup"><span data-stu-id="80a31-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a31-135">-Expires</span><span class="sxs-lookup"><span data-stu-id="80a31-135">-Expires</span></span>
<span data-ttu-id="80a31-136">Время окончания срока действия секретного даты в UTC.</span><span class="sxs-lookup"><span data-stu-id="80a31-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="80a31-137">Если он не задан, существующее значение срока действия секретного секрета не изменяется.</span><span class="sxs-lookup"><span data-stu-id="80a31-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a31-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80a31-138">-InputObject</span></span>
<span data-ttu-id="80a31-139">Секретный объект</span><span class="sxs-lookup"><span data-stu-id="80a31-139">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80a31-140">-Name</span><span class="sxs-lookup"><span data-stu-id="80a31-140">-Name</span></span>
<span data-ttu-id="80a31-141">Секретное имя.</span><span class="sxs-lookup"><span data-stu-id="80a31-141">Secret name.</span></span>
<span data-ttu-id="80a31-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span><span class="sxs-lookup"><span data-stu-id="80a31-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a31-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="80a31-143">-NotBefore</span></span>
<span data-ttu-id="80a31-144">Время в UTC, до которого нельзя использовать секрет.</span><span class="sxs-lookup"><span data-stu-id="80a31-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="80a31-145">Если не указано, существующее значение атрибута NotBefore секретного не изменяется.</span><span class="sxs-lookup"><span data-stu-id="80a31-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a31-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80a31-146">-PassThru</span></span>
<span data-ttu-id="80a31-147">По умолчанию cmdlet не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="80a31-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="80a31-148">Если этот переключатель задан, возвращается секретный объект.</span><span class="sxs-lookup"><span data-stu-id="80a31-148">If this switch is specified, return Secret object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a31-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="80a31-149">-Tag</span></span>
<span data-ttu-id="80a31-150">Hashtable representing secret tags.</span><span class="sxs-lookup"><span data-stu-id="80a31-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="80a31-151">Если не указано, существующие теги секретной части остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="80a31-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="80a31-152">Удалите тег, указав пустой hashtable.</span><span class="sxs-lookup"><span data-stu-id="80a31-152">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a31-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="80a31-153">-VaultName</span></span>
<span data-ttu-id="80a31-154">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="80a31-154">Vault name.</span></span>
<span data-ttu-id="80a31-155">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="80a31-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a31-156">-Version</span><span class="sxs-lookup"><span data-stu-id="80a31-156">-Version</span></span>
<span data-ttu-id="80a31-157">Секретная версия.</span><span class="sxs-lookup"><span data-stu-id="80a31-157">Secret version.</span></span>
<span data-ttu-id="80a31-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span><span class="sxs-lookup"><span data-stu-id="80a31-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a31-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80a31-159">-Confirm</span></span>
<span data-ttu-id="80a31-160">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="80a31-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80a31-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a31-161">-WhatIf</span></span>
<span data-ttu-id="80a31-162">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80a31-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80a31-163">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="80a31-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80a31-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a31-164">CommonParameters</span></span>
<span data-ttu-id="80a31-165">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80a31-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a31-166">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80a31-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a31-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80a31-167">INPUTS</span></span>

### <span data-ttu-id="80a31-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="80a31-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="80a31-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80a31-169">OUTPUTS</span></span>

### <span data-ttu-id="80a31-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="80a31-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="80a31-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="80a31-171">NOTES</span></span>

## <span data-ttu-id="80a31-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80a31-172">RELATED LINKS</span></span>
