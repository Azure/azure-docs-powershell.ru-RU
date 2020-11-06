---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: 4b9799a0d2433b513b801a95ffd5c408bf8bdbf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564863"
---
# <span data-ttu-id="cdedf-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="cdedf-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="cdedf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cdedf-102">SYNOPSIS</span></span>
<span data-ttu-id="cdedf-103">Обновляет атрибуты ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="cdedf-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdedf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cdedf-104">SYNTAX</span></span>

### <span data-ttu-id="cdedf-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cdedf-105">Default (Default)</span></span>
```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdedf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cdedf-106">InputObject</span></span>
```
Set-AzureKeyVaultKeyAttribute [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdedf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdedf-107">DESCRIPTION</span></span>
<span data-ttu-id="cdedf-108">Командлет **Set-AzureKeyVaultKeyAttribute** обновляет редактируемые атрибуты ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="cdedf-108">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="cdedf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cdedf-109">EXAMPLES</span></span>

### <span data-ttu-id="cdedf-110">Пример 1: изменение ключа для включения и Настройка даты и тегов срока действия</span><span class="sxs-lookup"><span data-stu-id="cdedf-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="cdedf-111">Первая команда создает объект **DateTime** с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="cdedf-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="cdedf-112">Этот объект указывает на время в будущем на два года.</span><span class="sxs-lookup"><span data-stu-id="cdedf-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="cdedf-113">Команда сохраняет эту дату в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="cdedf-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="cdedf-114">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="cdedf-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="cdedf-115">Вторая команда создает переменную для хранения значений тега High Severity и Accounting.</span><span class="sxs-lookup"><span data-stu-id="cdedf-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="cdedf-116">Последняя команда изменяет клавишу с именем ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="cdedf-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="cdedf-117">Эта команда включает ключ, задает время истечения срока действия, которое хранится в $Expires, и задает теги, которые хранятся в $Tags.</span><span class="sxs-lookup"><span data-stu-id="cdedf-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="cdedf-118">Пример 2: изменение ключа для удаления всех тегов</span><span class="sxs-lookup"><span data-stu-id="cdedf-118">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="cdedf-119">Эта команда удаляет все теги для определенной версии ключа с именем ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="cdedf-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="cdedf-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cdedf-120">PARAMETERS</span></span>

### <span data-ttu-id="cdedf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdedf-121">-DefaultProfile</span></span>
<span data-ttu-id="cdedf-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cdedf-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-123">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="cdedf-123">-Enable</span></span>
<span data-ttu-id="cdedf-124">Указывает, нужно ли включать или отключать ключ.</span><span class="sxs-lookup"><span data-stu-id="cdedf-124">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="cdedf-125">Значение $True включает ключ.</span><span class="sxs-lookup"><span data-stu-id="cdedf-125">A value of $True enables the key.</span></span> <span data-ttu-id="cdedf-126">Значение $False отключает ключ.</span><span class="sxs-lookup"><span data-stu-id="cdedf-126">A value of $False disables the key.</span></span> <span data-ttu-id="cdedf-127">Если этот параметр не указан, этот командлет не изменяет состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="cdedf-127">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-128">-Истекает</span><span class="sxs-lookup"><span data-stu-id="cdedf-128">-Expires</span></span>
<span data-ttu-id="cdedf-129">Задает время истечения срока действия в виде объекта **DateTime** для ключа, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="cdedf-129">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="cdedf-130">Этот параметр использует координированное координированное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="cdedf-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="cdedf-131">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="cdedf-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="cdedf-132">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="cdedf-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdedf-133">-InputObject</span></span>
<span data-ttu-id="cdedf-134">Объект Key</span><span class="sxs-lookup"><span data-stu-id="cdedf-134">Key object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="cdedf-135">-KeyOps</span></span>
<span data-ttu-id="cdedf-136">Задает массив операций, которые можно выполнить с помощью ключа, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cdedf-136">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="cdedf-137">Если этот параметр не указан, может выполняться выполнение всех операций.</span><span class="sxs-lookup"><span data-stu-id="cdedf-137">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="cdedf-138">Допустимые значения этого параметра — разделенный запятыми список ключевых операций, определяемый спецификацией веб-ключа JSON.</span><span class="sxs-lookup"><span data-stu-id="cdedf-138">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="cdedf-139">Эти значения (с учетом регистра):</span><span class="sxs-lookup"><span data-stu-id="cdedf-139">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="cdedf-140">EFS</span><span class="sxs-lookup"><span data-stu-id="cdedf-140">encrypt</span></span>
- <span data-ttu-id="cdedf-141">расшифровки</span><span class="sxs-lookup"><span data-stu-id="cdedf-141">decrypt</span></span>
- <span data-ttu-id="cdedf-142">Инкапсулирует</span><span class="sxs-lookup"><span data-stu-id="cdedf-142">wrap</span></span>
- <span data-ttu-id="cdedf-143">разтекание</span><span class="sxs-lookup"><span data-stu-id="cdedf-143">unwrap</span></span>
- <span data-ttu-id="cdedf-144">рядом</span><span class="sxs-lookup"><span data-stu-id="cdedf-144">sign</span></span>
- <span data-ttu-id="cdedf-145">подтвержда</span><span class="sxs-lookup"><span data-stu-id="cdedf-145">verify</span></span>
- <span data-ttu-id="cdedf-146">копирование</span><span class="sxs-lookup"><span data-stu-id="cdedf-146">backup</span></span>
- <span data-ttu-id="cdedf-147">восстановление</span><span class="sxs-lookup"><span data-stu-id="cdedf-147">restore</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cdedf-148">-Name</span></span>
<span data-ttu-id="cdedf-149">Задает имя обновляемого ключа.</span><span class="sxs-lookup"><span data-stu-id="cdedf-149">Specifies the name of the key to update.</span></span> <span data-ttu-id="cdedf-150">Этот командлет создает полное доменное имя (FQDN) ключа на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="cdedf-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-151">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="cdedf-151">-NotBefore</span></span>
<span data-ttu-id="cdedf-152">Указывает время в виде объекта **DateTime** , до которого невозможно использовать клавишу.</span><span class="sxs-lookup"><span data-stu-id="cdedf-152">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="cdedf-153">Этот параметр использует время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="cdedf-153">This parameter uses UTC.</span></span>
<span data-ttu-id="cdedf-154">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="cdedf-154">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdedf-155">-PassThru</span></span>
<span data-ttu-id="cdedf-156">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="cdedf-156">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cdedf-157">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cdedf-157">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-158">-Тег</span><span class="sxs-lookup"><span data-stu-id="cdedf-158">-Tag</span></span>
<span data-ttu-id="cdedf-159">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="cdedf-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cdedf-160">Например:</span><span class="sxs-lookup"><span data-stu-id="cdedf-160">For example:</span></span>

<span data-ttu-id="cdedf-161">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="cdedf-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-162">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cdedf-162">-VaultName</span></span>
<span data-ttu-id="cdedf-163">Указывает имя хранилища ключей, в котором этот командлет изменяет ключ.</span><span class="sxs-lookup"><span data-stu-id="cdedf-163">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="cdedf-164">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="cdedf-164">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-165">-Version</span><span class="sxs-lookup"><span data-stu-id="cdedf-165">-Version</span></span>
<span data-ttu-id="cdedf-166">Указывает версию ключа.</span><span class="sxs-lookup"><span data-stu-id="cdedf-166">Specifies the key version.</span></span>
<span data-ttu-id="cdedf-167">Этот командлет создает полное доменное имя ключа на основе имени хранилища ключей, текущей выбранной среды, имени ключа и версии ключа.</span><span class="sxs-lookup"><span data-stu-id="cdedf-167">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdedf-168">-Confirm</span></span>
<span data-ttu-id="cdedf-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cdedf-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdedf-170">-WhatIf</span></span>
<span data-ttu-id="cdedf-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cdedf-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdedf-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cdedf-172">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdedf-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdedf-173">CommonParameters</span></span>
<span data-ttu-id="cdedf-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cdedf-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdedf-175">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdedf-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdedf-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cdedf-176">INPUTS</span></span>

### <span data-ttu-id="cdedf-177">Ничего</span><span class="sxs-lookup"><span data-stu-id="cdedf-177">None</span></span>
<span data-ttu-id="cdedf-178">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="cdedf-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cdedf-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cdedf-179">OUTPUTS</span></span>

### <span data-ttu-id="cdedf-180">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cdedf-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="cdedf-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="cdedf-181">NOTES</span></span>

## <span data-ttu-id="cdedf-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cdedf-182">RELATED LINKS</span></span>

[<span data-ttu-id="cdedf-183">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cdedf-183">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="cdedf-184">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cdedf-184">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="cdedf-185">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cdedf-185">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
