---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
ms.openlocfilehash: e9e2401ab96da63c3fe6b5978916b96f98db9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564375"
---
# <span data-ttu-id="9a52c-101">Update-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9a52c-101">Update-AzureKeyVaultKey</span></span>

## <span data-ttu-id="9a52c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a52c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a52c-103">Обновляет атрибуты ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="9a52c-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a52c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a52c-104">SYNTAX</span></span>

### <span data-ttu-id="9a52c-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a52c-105">Default (Default)</span></span>
```
Update-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a52c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9a52c-106">InputObject</span></span>
```
Update-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a52c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a52c-107">DESCRIPTION</span></span>
<span data-ttu-id="9a52c-108">Командлет **Update-AzureKeyVaultKey** обновляет редактируемые атрибуты ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="9a52c-108">The **Update-AzureKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="9a52c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a52c-109">EXAMPLES</span></span>

### <span data-ttu-id="9a52c-110">Пример 1: изменение ключа для включения и Настройка даты и тегов срока действия</span><span class="sxs-lookup"><span data-stu-id="9a52c-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

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

<span data-ttu-id="9a52c-111">Первая команда создает объект **DateTime** с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="9a52c-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="9a52c-112">Этот объект указывает на время в будущем на два года.</span><span class="sxs-lookup"><span data-stu-id="9a52c-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="9a52c-113">Команда сохраняет эту дату в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="9a52c-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="9a52c-114">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9a52c-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="9a52c-115">Вторая команда создает переменную для хранения значений тега High Severity и Accounting.</span><span class="sxs-lookup"><span data-stu-id="9a52c-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="9a52c-116">Последняя команда изменяет клавишу с именем ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="9a52c-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="9a52c-117">Эта команда включает ключ, задает время истечения срока действия, которое хранится в $Expires, и задает теги, которые хранятся в $Tags.</span><span class="sxs-lookup"><span data-stu-id="9a52c-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="9a52c-118">Пример 2: изменение ключа для удаления всех тегов</span><span class="sxs-lookup"><span data-stu-id="9a52c-118">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

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

<span data-ttu-id="9a52c-119">Эта команда удаляет все теги для определенной версии ключа с именем ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="9a52c-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="9a52c-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a52c-120">PARAMETERS</span></span>

### <span data-ttu-id="9a52c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a52c-121">-DefaultProfile</span></span>
<span data-ttu-id="9a52c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a52c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a52c-123">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="9a52c-123">-Enable</span></span>
<span data-ttu-id="9a52c-124">Значение true включает клавишу и значение false, чтобы клавиша была недоступна.</span><span class="sxs-lookup"><span data-stu-id="9a52c-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="9a52c-125">Если не указано, существующее состояние "включено/отключено" не изменится.</span><span class="sxs-lookup"><span data-stu-id="9a52c-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="9a52c-126">-Истекает</span><span class="sxs-lookup"><span data-stu-id="9a52c-126">-Expires</span></span>
<span data-ttu-id="9a52c-127">Время окончания срока действия клавиши в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="9a52c-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="9a52c-128">Если этот параметр не указан, существующее время окончания срока действия ключа не меняется.</span><span class="sxs-lookup"><span data-stu-id="9a52c-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="9a52c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a52c-129">-InputObject</span></span>
<span data-ttu-id="9a52c-130">Объект Key</span><span class="sxs-lookup"><span data-stu-id="9a52c-130">Key object</span></span>

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

### <span data-ttu-id="9a52c-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="9a52c-131">-KeyOps</span></span>
<span data-ttu-id="9a52c-132">Операции, которые можно выполнить с ключом.</span><span class="sxs-lookup"><span data-stu-id="9a52c-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="9a52c-133">Если не указано, то существующие операции с ключом ключа остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="9a52c-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="9a52c-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a52c-134">-Name</span></span>
<span data-ttu-id="9a52c-135">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="9a52c-135">Key name.</span></span>
<span data-ttu-id="9a52c-136">Командлет создает полное доменное имя ключа из имени хранилища, выбранной в данный момент среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="9a52c-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="9a52c-137">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="9a52c-137">-NotBefore</span></span>
<span data-ttu-id="9a52c-138">Время в формате UTC, после которого клавиша не может быть использована.</span><span class="sxs-lookup"><span data-stu-id="9a52c-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="9a52c-139">Если этот параметр не указан, существующий атрибут NotBefore для ключа не изменится.</span><span class="sxs-lookup"><span data-stu-id="9a52c-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="9a52c-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a52c-140">-PassThru</span></span>
<span data-ttu-id="9a52c-141">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="9a52c-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9a52c-142">Если указан этот параметр, возвращает обновленный объект набора ключей.</span><span class="sxs-lookup"><span data-stu-id="9a52c-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="9a52c-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="9a52c-143">-Tag</span></span>
<span data-ttu-id="9a52c-144">Хэш-таблица представляет ключевые теги.</span><span class="sxs-lookup"><span data-stu-id="9a52c-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="9a52c-145">Если этот параметр не указан, существующие теги ключа остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="9a52c-145">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="9a52c-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9a52c-146">-VaultName</span></span>
<span data-ttu-id="9a52c-147">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="9a52c-147">Vault name.</span></span>
<span data-ttu-id="9a52c-148">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="9a52c-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9a52c-149">-Version</span><span class="sxs-lookup"><span data-stu-id="9a52c-149">-Version</span></span>
<span data-ttu-id="9a52c-150">Версия ключа.</span><span class="sxs-lookup"><span data-stu-id="9a52c-150">Key version.</span></span>
<span data-ttu-id="9a52c-151">Командлет создает полное доменное имя ключа из имени хранилища, выбранной в данный момент среды, имени ключа и версии ключа.</span><span class="sxs-lookup"><span data-stu-id="9a52c-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="9a52c-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a52c-152">-Confirm</span></span>
<span data-ttu-id="9a52c-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a52c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a52c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a52c-154">-WhatIf</span></span>
<span data-ttu-id="9a52c-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a52c-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a52c-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a52c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a52c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a52c-157">CommonParameters</span></span>
<span data-ttu-id="9a52c-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a52c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a52c-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a52c-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a52c-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a52c-160">INPUTS</span></span>

### <span data-ttu-id="9a52c-161">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9a52c-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="9a52c-162">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9a52c-162">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9a52c-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a52c-163">OUTPUTS</span></span>

### <span data-ttu-id="9a52c-164">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9a52c-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="9a52c-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a52c-165">NOTES</span></span>

## <span data-ttu-id="9a52c-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a52c-166">RELATED LINKS</span></span>
