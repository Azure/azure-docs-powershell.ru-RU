---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://go.microsoft.com/fwlink/?LinkId=690302
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: fbc2c4cd56da23bef29716800316f479159af148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568758"
---
# <span data-ttu-id="465e1-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="465e1-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="465e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="465e1-102">SYNOPSIS</span></span>
<span data-ttu-id="465e1-103">Обновляет атрибуты ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="465e1-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="465e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="465e1-104">SYNTAX</span></span>

```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="465e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="465e1-105">DESCRIPTION</span></span>
<span data-ttu-id="465e1-106">Командлет **Set-AzureKeyVaultKeyAttribute** обновляет редактируемые атрибуты ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="465e1-106">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="465e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="465e1-107">EXAMPLES</span></span>

### <span data-ttu-id="465e1-108">Пример 1: изменение ключа для включения и Настройка даты и тегов срока действия</span><span class="sxs-lookup"><span data-stu-id="465e1-108">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="465e1-109">Первая команда создает объект **DateTime** с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="465e1-109">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="465e1-110">Этот объект указывает на время в будущем на два года.</span><span class="sxs-lookup"><span data-stu-id="465e1-110">That object specifies a time two years in the future.</span></span> <span data-ttu-id="465e1-111">Команда сохраняет эту дату в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="465e1-111">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="465e1-112">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="465e1-112">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="465e1-113">Вторая команда создает переменную для хранения значений тега High Severity и Accounting.</span><span class="sxs-lookup"><span data-stu-id="465e1-113">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="465e1-114">Последняя команда изменяет клавишу с именем ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="465e1-114">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="465e1-115">Эта команда включает ключ, задает время истечения срока действия, которое хранится в $Expires, и задает теги, которые хранятся в $Tags.</span><span class="sxs-lookup"><span data-stu-id="465e1-115">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="465e1-116">Пример 2: изменение ключа для удаления всех тегов</span><span class="sxs-lookup"><span data-stu-id="465e1-116">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="465e1-117">Эта команда удаляет все теги для определенной версии ключа с именем ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="465e1-117">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="465e1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="465e1-118">PARAMETERS</span></span>

### <span data-ttu-id="465e1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="465e1-119">-Confirm</span></span>
<span data-ttu-id="465e1-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="465e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="465e1-121">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="465e1-121">-Enable</span></span>
<span data-ttu-id="465e1-122">Указывает, нужно ли включать или отключать ключ.</span><span class="sxs-lookup"><span data-stu-id="465e1-122">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="465e1-123">Значение $True включает ключ.</span><span class="sxs-lookup"><span data-stu-id="465e1-123">A value of $True enables the key.</span></span> <span data-ttu-id="465e1-124">Значение $False отключает ключ.</span><span class="sxs-lookup"><span data-stu-id="465e1-124">A value of $False disables the key.</span></span> <span data-ttu-id="465e1-125">Если этот параметр не указан, этот командлет не изменяет состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="465e1-125">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="465e1-126">-Истекает</span><span class="sxs-lookup"><span data-stu-id="465e1-126">-Expires</span></span>
<span data-ttu-id="465e1-127">Задает время истечения срока действия в виде объекта **DateTime** для ключа, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="465e1-127">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="465e1-128">Этот параметр использует координированное координированное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="465e1-128">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="465e1-129">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="465e1-129">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="465e1-130">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="465e1-130">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="465e1-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="465e1-131">-KeyOps</span></span>
<span data-ttu-id="465e1-132">Задает массив операций, которые можно выполнить с помощью ключа, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="465e1-132">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="465e1-133">Если этот параметр не указан, может выполняться выполнение всех операций.</span><span class="sxs-lookup"><span data-stu-id="465e1-133">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="465e1-134">Допустимые значения этого параметра — разделенный запятыми список ключевых операций, определяемый спецификацией веб-ключа JSON.</span><span class="sxs-lookup"><span data-stu-id="465e1-134">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="465e1-135">Эти значения (с учетом регистра):</span><span class="sxs-lookup"><span data-stu-id="465e1-135">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="465e1-136">EFS</span><span class="sxs-lookup"><span data-stu-id="465e1-136">encrypt</span></span>
- <span data-ttu-id="465e1-137">расшифровки</span><span class="sxs-lookup"><span data-stu-id="465e1-137">decrypt</span></span>
- <span data-ttu-id="465e1-138">Инкапсулирует</span><span class="sxs-lookup"><span data-stu-id="465e1-138">wrap</span></span>
- <span data-ttu-id="465e1-139">разтекание</span><span class="sxs-lookup"><span data-stu-id="465e1-139">unwrap</span></span>
- <span data-ttu-id="465e1-140">рядом</span><span class="sxs-lookup"><span data-stu-id="465e1-140">sign</span></span>
- <span data-ttu-id="465e1-141">подтвержда</span><span class="sxs-lookup"><span data-stu-id="465e1-141">verify</span></span>
- <span data-ttu-id="465e1-142">копирование</span><span class="sxs-lookup"><span data-stu-id="465e1-142">backup</span></span>
- <span data-ttu-id="465e1-143">восстановление</span><span class="sxs-lookup"><span data-stu-id="465e1-143">restore</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="465e1-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="465e1-144">-Name</span></span>
<span data-ttu-id="465e1-145">Задает имя обновляемого ключа.</span><span class="sxs-lookup"><span data-stu-id="465e1-145">Specifies the name of the key to update.</span></span> <span data-ttu-id="465e1-146">Этот командлет создает полное доменное имя (FQDN) ключа на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="465e1-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="465e1-147">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="465e1-147">-NotBefore</span></span>
<span data-ttu-id="465e1-148">Указывает время в виде объекта **DateTime** , до которого невозможно использовать клавишу.</span><span class="sxs-lookup"><span data-stu-id="465e1-148">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="465e1-149">Этот параметр использует время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="465e1-149">This parameter uses UTC.</span></span>
<span data-ttu-id="465e1-150">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="465e1-150">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="465e1-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="465e1-151">-PassThru</span></span>
<span data-ttu-id="465e1-152">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="465e1-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="465e1-153">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="465e1-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="465e1-154">-Тег</span><span class="sxs-lookup"><span data-stu-id="465e1-154">-Tag</span></span>
<span data-ttu-id="465e1-155">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="465e1-155">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="465e1-156">Например:</span><span class="sxs-lookup"><span data-stu-id="465e1-156">For example:</span></span>

<span data-ttu-id="465e1-157">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="465e1-157">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="465e1-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="465e1-158">-VaultName</span></span>
<span data-ttu-id="465e1-159">Указывает имя хранилища ключей, в котором этот командлет изменяет ключ.</span><span class="sxs-lookup"><span data-stu-id="465e1-159">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="465e1-160">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="465e1-160">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="465e1-161">-Version</span><span class="sxs-lookup"><span data-stu-id="465e1-161">-Version</span></span>
<span data-ttu-id="465e1-162">Указывает версию ключа.</span><span class="sxs-lookup"><span data-stu-id="465e1-162">Specifies the key version.</span></span>
<span data-ttu-id="465e1-163">Этот командлет создает полное доменное имя ключа на основе имени хранилища ключей, текущей выбранной среды, имени ключа и версии ключа.</span><span class="sxs-lookup"><span data-stu-id="465e1-163">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="465e1-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="465e1-164">-WhatIf</span></span>
<span data-ttu-id="465e1-165">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="465e1-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="465e1-166">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="465e1-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="465e1-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="465e1-167">-DefaultProfile</span></span>
<span data-ttu-id="465e1-168">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="465e1-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="465e1-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="465e1-169">CommonParameters</span></span>
<span data-ttu-id="465e1-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="465e1-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="465e1-171">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="465e1-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="465e1-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="465e1-172">INPUTS</span></span>

## <span data-ttu-id="465e1-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="465e1-173">OUTPUTS</span></span>

### <span data-ttu-id="465e1-174">Microsoft. Azure. Commands. KeyVault. Models. KeyBundle</span><span class="sxs-lookup"><span data-stu-id="465e1-174">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="465e1-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="465e1-175">NOTES</span></span>

## <span data-ttu-id="465e1-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="465e1-176">RELATED LINKS</span></span>

[<span data-ttu-id="465e1-177">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="465e1-177">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="465e1-178">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="465e1-178">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="465e1-179">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="465e1-179">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
