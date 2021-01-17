---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327574"
---
# <span data-ttu-id="b03c3-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b03c3-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="b03c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b03c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b03c3-103">Обновляет атрибуты секретного секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="b03c3-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="b03c3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b03c3-104">SYNTAX</span></span>

### <span data-ttu-id="b03c3-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b03c3-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b03c3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b03c3-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b03c3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b03c3-107">DESCRIPTION</span></span>
<span data-ttu-id="b03c3-108">С **его** нажатием можно изменять атрибуты секретного сейфа.</span><span class="sxs-lookup"><span data-stu-id="b03c3-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="b03c3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b03c3-109">EXAMPLES</span></span>

### <span data-ttu-id="b03c3-110">Пример 1. Изменение атрибутов секретного</span><span class="sxs-lookup"><span data-stu-id="b03c3-110">Example 1: Modify the attributes of a secret</span></span>
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

<span data-ttu-id="b03c3-111">Первые четыре команды определяют атрибуты для даты окончания срока действия, даты NotBefore, тегов и типа контекста, а также сохраняют атрибуты в переменных.</span><span class="sxs-lookup"><span data-stu-id="b03c3-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="b03c3-112">Итоговая команда изменяет атрибуты секретного отдела кадров в хранилище ключей ContosoVault с использованием хранимых переменных.</span><span class="sxs-lookup"><span data-stu-id="b03c3-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="b03c3-113">Пример 2. Удаление тегов и типа контента для секретного</span><span class="sxs-lookup"><span data-stu-id="b03c3-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="b03c3-114">Эта команда удаляет теги и тип контента для указанной версии секретного отдела кадров в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="b03c3-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="b03c3-115">Пример 3. Отключение текущей версии секретов, имя которых начинается с ИТ</span><span class="sxs-lookup"><span data-stu-id="b03c3-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="b03c3-116">Первая команда сохраняет строковые значения Contoso в $Vault переменной.</span><span class="sxs-lookup"><span data-stu-id="b03c3-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="b03c3-117">Вторая команда сохраняет строковые значения ИТ в $Prefix переменной.</span><span class="sxs-lookup"><span data-stu-id="b03c3-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="b03c3-118">Третья команда использует Get-AzKeyVaultSecret командлет, чтобы получить секрет в указанном хранилище ключей, а затем передает эти секреты **командлету Where-Object.**</span><span class="sxs-lookup"><span data-stu-id="b03c3-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="b03c3-119">С **помощью cmdlet Where-Object** можно отфильтровать секреты имен, которые начинаются с ИТ-символов.</span><span class="sxs-lookup"><span data-stu-id="b03c3-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="b03c3-120">Эта команда передает секрет, который соответствует фильтру Update-AzKeyVaultSecret командлету, который отключает их.</span><span class="sxs-lookup"><span data-stu-id="b03c3-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="b03c3-121">Пример 4. Настройка ContentType для всех версий секретного</span><span class="sxs-lookup"><span data-stu-id="b03c3-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="b03c3-122">Первые три команды определяют строковые переменные, которые нужно использовать для параметров *VaultName,* *Name* и *ContentType.*</span><span class="sxs-lookup"><span data-stu-id="b03c3-122">The first three commands define string variables to use for the *VaultName*, *Name*, and *ContentType* parameters.</span></span> <span data-ttu-id="b03c3-123">Четвертая команда использует Get-AzKeyVaultKey для получения указанных клавиш, а затем передает их Update-AzKeyVaultSecret командлету, чтобы выбрать тип контента XML.</span><span class="sxs-lookup"><span data-stu-id="b03c3-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="b03c3-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b03c3-124">PARAMETERS</span></span>

### <span data-ttu-id="b03c3-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="b03c3-125">-ContentType</span></span>
<span data-ttu-id="b03c3-126">Тип контента секретного.</span><span class="sxs-lookup"><span data-stu-id="b03c3-126">Secret's content type.</span></span>
<span data-ttu-id="b03c3-127">Если он не задан, существующее значение типа контента секретного содержимого не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b03c3-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="b03c3-128">Удалите существующее значение типа контента, указав пустую строку.</span><span class="sxs-lookup"><span data-stu-id="b03c3-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="b03c3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03c3-129">-DefaultProfile</span></span>
<span data-ttu-id="b03c3-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b03c3-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b03c3-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="b03c3-131">-Enable</span></span>
<span data-ttu-id="b03c3-132">При этом в нее можно включить секрет, если значение является истинным.</span><span class="sxs-lookup"><span data-stu-id="b03c3-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="b03c3-133">Отключать секрет, если значение ложно.</span><span class="sxs-lookup"><span data-stu-id="b03c3-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="b03c3-134">Если он не задан, существующее значение состояния секретного состояния (включено или отключено) не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b03c3-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="b03c3-135">-Expires</span><span class="sxs-lookup"><span data-stu-id="b03c3-135">-Expires</span></span>
<span data-ttu-id="b03c3-136">Время окончания срока действия секретного даты в UTC.</span><span class="sxs-lookup"><span data-stu-id="b03c3-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="b03c3-137">Если он не задан, существующее значение срока действия секретного секрета не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b03c3-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="b03c3-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b03c3-138">-InputObject</span></span>
<span data-ttu-id="b03c3-139">Секретный объект</span><span class="sxs-lookup"><span data-stu-id="b03c3-139">Secret object</span></span>

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

### <span data-ttu-id="b03c3-140">-Name</span><span class="sxs-lookup"><span data-stu-id="b03c3-140">-Name</span></span>
<span data-ttu-id="b03c3-141">Секретное имя.</span><span class="sxs-lookup"><span data-stu-id="b03c3-141">Secret name.</span></span>
<span data-ttu-id="b03c3-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span><span class="sxs-lookup"><span data-stu-id="b03c3-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="b03c3-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="b03c3-143">-NotBefore</span></span>
<span data-ttu-id="b03c3-144">Время в UTC, до которого нельзя использовать секрет.</span><span class="sxs-lookup"><span data-stu-id="b03c3-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="b03c3-145">Если не указано, существующее значение атрибута NotBefore секретного не изменяется.</span><span class="sxs-lookup"><span data-stu-id="b03c3-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="b03c3-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b03c3-146">-PassThru</span></span>
<span data-ttu-id="b03c3-147">По умолчанию cmdlet не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="b03c3-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="b03c3-148">Если этот переключатель задан, возвращается секретный объект.</span><span class="sxs-lookup"><span data-stu-id="b03c3-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="b03c3-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="b03c3-149">-Tag</span></span>
<span data-ttu-id="b03c3-150">Hashtable representing secret tags.</span><span class="sxs-lookup"><span data-stu-id="b03c3-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="b03c3-151">Если не указано, существующие теги секретной части остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="b03c3-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="b03c3-152">Удалите тег, указав пустой hashtable.</span><span class="sxs-lookup"><span data-stu-id="b03c3-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="b03c3-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b03c3-153">-VaultName</span></span>
<span data-ttu-id="b03c3-154">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="b03c3-154">Vault name.</span></span>
<span data-ttu-id="b03c3-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="b03c3-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b03c3-156">-Version</span><span class="sxs-lookup"><span data-stu-id="b03c3-156">-Version</span></span>
<span data-ttu-id="b03c3-157">Секретная версия.</span><span class="sxs-lookup"><span data-stu-id="b03c3-157">Secret version.</span></span>
<span data-ttu-id="b03c3-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span><span class="sxs-lookup"><span data-stu-id="b03c3-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

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

### <span data-ttu-id="b03c3-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b03c3-159">-Confirm</span></span>
<span data-ttu-id="b03c3-160">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b03c3-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b03c3-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b03c3-161">-WhatIf</span></span>
<span data-ttu-id="b03c3-162">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b03c3-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b03c3-163">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b03c3-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b03c3-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03c3-164">CommonParameters</span></span>
<span data-ttu-id="b03c3-165">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b03c3-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03c3-166">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b03c3-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03c3-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b03c3-167">INPUTS</span></span>

### <span data-ttu-id="b03c3-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b03c3-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="b03c3-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b03c3-169">OUTPUTS</span></span>

### <span data-ttu-id="b03c3-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b03c3-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="b03c3-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b03c3-171">NOTES</span></span>

## <span data-ttu-id="b03c3-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b03c3-172">RELATED LINKS</span></span>
