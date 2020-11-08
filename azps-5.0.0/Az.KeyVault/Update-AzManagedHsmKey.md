---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
ms.openlocfilehash: 79d01f96fe776432f650d827b16ba83f48b84ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249038"
---
# <span data-ttu-id="16400-101">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="16400-101">Update-AzManagedHsmKey</span></span>

## <span data-ttu-id="16400-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16400-102">SYNOPSIS</span></span>
<span data-ttu-id="16400-103">Обновляет атрибуты ключа в управляемом HSM.</span><span class="sxs-lookup"><span data-stu-id="16400-103">Updates the attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="16400-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16400-104">SYNTAX</span></span>

### <span data-ttu-id="16400-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16400-105">Default (Default)</span></span>
```
Update-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16400-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="16400-106">InputObject</span></span>
```
Update-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16400-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16400-107">DESCRIPTION</span></span>
<span data-ttu-id="16400-108">Командлет **Update-AzManagedHsmKey** обновляет редактируемые атрибуты ключа в управляемом HSM.</span><span class="sxs-lookup"><span data-stu-id="16400-108">The **Update-AzManagedHsmKey** cmdlet updates the editable attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="16400-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16400-109">EXAMPLES</span></span>

### <span data-ttu-id="16400-110">Пример 1: изменение ключа для включения и Настройка даты и тегов срока действия</span><span class="sxs-lookup"><span data-stu-id="16400-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzManagedHsmKey -HsmName testmhsm -Name testkey001 -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 49b74a39dab605bd336628dc094dc31b
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/49b74a39dab605bd336628dc094dc31b
Enabled        : True
Expires        : 10/14/2022 9:46:55 AM
Not Before     :
Created        : 10/14/2020 3:39:16 AM
Updated        : 10/14/2020 9:47:06 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="16400-111">Первая команда создает объект **DateTime** с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="16400-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="16400-112">Этот объект указывает на время в будущем на два года.</span><span class="sxs-lookup"><span data-stu-id="16400-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="16400-113">Команда сохраняет эту дату в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="16400-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="16400-114">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="16400-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="16400-115">Вторая команда создает переменную для хранения значений тега High Severity и Accounting.</span><span class="sxs-lookup"><span data-stu-id="16400-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="16400-116">Последняя команда изменяет клавишу с именем testkey001.</span><span class="sxs-lookup"><span data-stu-id="16400-116">The final command modifies a key named testkey001.</span></span> <span data-ttu-id="16400-117">Эта команда включает ключ, задает время истечения срока действия, которое хранится в $Expires, и задает теги, которые хранятся в $Tags.</span><span class="sxs-lookup"><span data-stu-id="16400-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

## <span data-ttu-id="16400-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16400-118">PARAMETERS</span></span>

### <span data-ttu-id="16400-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16400-119">-DefaultProfile</span></span>
<span data-ttu-id="16400-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16400-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16400-121">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="16400-121">-Enable</span></span>
<span data-ttu-id="16400-122">Значение true включает клавишу и значение false, чтобы клавиша была недоступна.</span><span class="sxs-lookup"><span data-stu-id="16400-122">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="16400-123">Если не указано, существующее состояние "включено/отключено" не изменится.</span><span class="sxs-lookup"><span data-stu-id="16400-123">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="16400-124">-Истекает</span><span class="sxs-lookup"><span data-stu-id="16400-124">-Expires</span></span>
<span data-ttu-id="16400-125">Время окончания срока действия клавиши в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="16400-125">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="16400-126">Если этот параметр не указан, существующее время окончания срока действия ключа не меняется.</span><span class="sxs-lookup"><span data-stu-id="16400-126">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="16400-127">-HsmName</span><span class="sxs-lookup"><span data-stu-id="16400-127">-HsmName</span></span>
<span data-ttu-id="16400-128">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="16400-128">HSM name.</span></span> <span data-ttu-id="16400-129">Командлет создает полное доменное имя управляемого HSM-файла на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="16400-129">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="16400-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16400-130">-InputObject</span></span>
<span data-ttu-id="16400-131">Объект Key</span><span class="sxs-lookup"><span data-stu-id="16400-131">Key object</span></span>

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

### <span data-ttu-id="16400-132">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="16400-132">-KeyOps</span></span>
<span data-ttu-id="16400-133">Операции, которые можно выполнить с ключом.</span><span class="sxs-lookup"><span data-stu-id="16400-133">The operations that can be performed with the key.</span></span>
<span data-ttu-id="16400-134">Если не указано, то существующие операции с ключом ключа остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="16400-134">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="16400-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16400-135">-Name</span></span>
<span data-ttu-id="16400-136">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="16400-136">Key name.</span></span>
<span data-ttu-id="16400-137">Командлет конструирует полное доменное имя ключа из управляемого имени HSM, в настоящее время выбранной среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="16400-137">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16400-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="16400-138">-NotBefore</span></span>
<span data-ttu-id="16400-139">Время в формате UTC, после которого клавиша не может быть использована.</span><span class="sxs-lookup"><span data-stu-id="16400-139">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="16400-140">Если этот параметр не указан, существующий атрибут NotBefore для ключа не изменится.</span><span class="sxs-lookup"><span data-stu-id="16400-140">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="16400-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16400-141">-PassThru</span></span>
<span data-ttu-id="16400-142">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="16400-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="16400-143">Если указан этот параметр, возвращает обновленный объект набора ключей.</span><span class="sxs-lookup"><span data-stu-id="16400-143">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="16400-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="16400-144">-Tag</span></span>
<span data-ttu-id="16400-145">Хэш-таблица представляет ключевые теги.</span><span class="sxs-lookup"><span data-stu-id="16400-145">A hashtable represents key tags.</span></span>
<span data-ttu-id="16400-146">Если этот параметр не указан, существующие теги ключа остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="16400-146">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="16400-147">-Version</span><span class="sxs-lookup"><span data-stu-id="16400-147">-Version</span></span>
<span data-ttu-id="16400-148">Версия ключа.</span><span class="sxs-lookup"><span data-stu-id="16400-148">Key version.</span></span>
<span data-ttu-id="16400-149">Командлет создает полное доменное имя ключа из управляемого имени HSM, в выбранной среде, имени ключа и версии ключа.</span><span class="sxs-lookup"><span data-stu-id="16400-149">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="16400-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16400-150">-Confirm</span></span>
<span data-ttu-id="16400-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16400-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16400-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16400-152">-WhatIf</span></span>
<span data-ttu-id="16400-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="16400-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16400-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="16400-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16400-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16400-155">CommonParameters</span></span>
<span data-ttu-id="16400-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16400-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16400-157">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16400-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16400-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16400-158">INPUTS</span></span>

### <span data-ttu-id="16400-159">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="16400-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="16400-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16400-160">OUTPUTS</span></span>

### <span data-ttu-id="16400-161">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="16400-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="16400-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="16400-162">NOTES</span></span>

## <span data-ttu-id="16400-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16400-163">RELATED LINKS</span></span>

[<span data-ttu-id="16400-164">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="16400-164">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="16400-165">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="16400-165">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="16400-166">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="16400-166">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="16400-167">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="16400-167">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="16400-168">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="16400-168">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="16400-169">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="16400-169">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)