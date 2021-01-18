---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: de8e542079cdeebdb6513c8e0febf8cfe0952889
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507182"
---
# <span data-ttu-id="4ef6e-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ef6e-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="4ef6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ef6e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef6e-103">Обновляет атрибуты ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="4ef6e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ef6e-104">SYNTAX</span></span>

### <span data-ttu-id="4ef6e-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ef6e-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ef6e-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="4ef6e-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ef6e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4ef6e-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ef6e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ef6e-108">DESCRIPTION</span></span>
<span data-ttu-id="4ef6e-109">При нажатии на **клавиши Update-AzKeyVaultKey** редактируемые атрибуты ключа обновляются в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="4ef6e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ef6e-110">EXAMPLES</span></span>

### <span data-ttu-id="4ef6e-111">Пример 1. Изменение ключа, чтобы включить его, и настройка даты окончания срока действия и тегов</span><span class="sxs-lookup"><span data-stu-id="4ef6e-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="4ef6e-112">Первая команда создает объект **даты и времени** с помощью командлета **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="4ef6e-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="4ef6e-113">Этот объект определяет время на два года в будущем.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="4ef6e-114">Эта команда сохраняет эту дату в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="4ef6e-115">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4ef6e-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="4ef6e-116">Вторая команда создает переменную для хранения значений тегов высокой важности и бухгалтерии.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="4ef6e-117">Конечная команда изменяет ключ с именем ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="4ef6e-118">Эта команда включает ключ, задает время окончания срока его действия, сохраненное в $Expires, и устанавливает теги, которые хранятся в $Tags.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="4ef6e-119">Пример 2. Изменение ключа для удаления всех тегов</span><span class="sxs-lookup"><span data-stu-id="4ef6e-119">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="4ef6e-120">Эта команда удаляет все теги для определенной версии ключа ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="4ef6e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ef6e-121">PARAMETERS</span></span>

### <span data-ttu-id="4ef6e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef6e-122">-DefaultProfile</span></span>
<span data-ttu-id="4ef6e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ef6e-124">-Enable</span><span class="sxs-lookup"><span data-stu-id="4ef6e-124">-Enable</span></span>
<span data-ttu-id="4ef6e-125">Значение true включает ключ, а ложь отключает ключ.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="4ef6e-126">Если он не задан, существующее состояние (включено или отключено) не изменяется.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="4ef6e-127">-Expires</span><span class="sxs-lookup"><span data-stu-id="4ef6e-127">-Expires</span></span>
<span data-ttu-id="4ef6e-128">Время окончания срока действия ключа в UTC.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="4ef6e-129">Если он не задан, срок действия ключа не изменяется.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="4ef6e-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="4ef6e-130">-HsmName</span></span>
<span data-ttu-id="4ef6e-131">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-131">HSM name.</span></span> <span data-ttu-id="4ef6e-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef6e-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ef6e-133">-InputObject</span></span>
<span data-ttu-id="4ef6e-134">Ключевой объект</span><span class="sxs-lookup"><span data-stu-id="4ef6e-134">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef6e-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="4ef6e-135">-KeyOps</span></span>
<span data-ttu-id="4ef6e-136">Операции, которые можно выполнять с помощью клавиши.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="4ef6e-137">Если он не задан, существующие операции ключа остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef6e-138">-Name</span><span class="sxs-lookup"><span data-stu-id="4ef6e-138">-Name</span></span>
<span data-ttu-id="4ef6e-139">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-139">Key name.</span></span>
<span data-ttu-id="4ef6e-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef6e-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="4ef6e-141">-NotBefore</span></span>
<span data-ttu-id="4ef6e-142">Время в UTC, до которого нельзя использовать ключ.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="4ef6e-143">Если он не задан, существующий атрибут NotBefore ключа не изменяется.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="4ef6e-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ef6e-144">-PassThru</span></span>
<span data-ttu-id="4ef6e-145">По умолчанию cmdlet не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4ef6e-146">Если этот ключ задан, возвращает обновленный объект пакета ключей.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="4ef6e-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ef6e-147">-Tag</span></span>
<span data-ttu-id="4ef6e-148">В этом элементе есть теги ключа.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="4ef6e-149">Если он не задан, существующие теги ключа остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-149">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="4ef6e-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4ef6e-150">-VaultName</span></span>
<span data-ttu-id="4ef6e-151">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-151">Vault name.</span></span>
<span data-ttu-id="4ef6e-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4ef6e-153">-Версия</span><span class="sxs-lookup"><span data-stu-id="4ef6e-153">-Version</span></span>
<span data-ttu-id="4ef6e-154">Основная версия.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-154">Key version.</span></span>
<span data-ttu-id="4ef6e-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef6e-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ef6e-156">-Confirm</span></span>
<span data-ttu-id="4ef6e-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ef6e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ef6e-158">-WhatIf</span></span>
<span data-ttu-id="4ef6e-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ef6e-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ef6e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef6e-161">CommonParameters</span></span>
<span data-ttu-id="4ef6e-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ef6e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef6e-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ef6e-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef6e-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ef6e-164">INPUTS</span></span>

### <span data-ttu-id="4ef6e-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4ef6e-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="4ef6e-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ef6e-166">OUTPUTS</span></span>

### <span data-ttu-id="4ef6e-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4ef6e-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="4ef6e-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ef6e-168">NOTES</span></span>

## <span data-ttu-id="4ef6e-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ef6e-169">RELATED LINKS</span></span>
