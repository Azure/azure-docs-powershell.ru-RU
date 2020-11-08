---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
ms.openlocfilehash: 89238992b99d86cdd56337a3002167be9c0d78d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250233"
---
# <span data-ttu-id="6a94e-101">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6a94e-101">Add-AzManagedHsmKey</span></span>

## <span data-ttu-id="6a94e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a94e-102">SYNOPSIS</span></span>
<span data-ttu-id="6a94e-103">Создание ключа в управляемом HSM-подразделении или импорт ключа в управляемый HSM-код.</span><span class="sxs-lookup"><span data-stu-id="6a94e-103">Creates a key in a managed HSM or imports a key into a managed HSM.</span></span>

## <span data-ttu-id="6a94e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a94e-104">SYNTAX</span></span>

### <span data-ttu-id="6a94e-105">InteractiveCreate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6a94e-105">InteractiveCreate (Default)</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a94e-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="6a94e-106">InteractiveImport</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a94e-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="6a94e-107">InputObjectCreate</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyType <String> [-CurveName <String>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-Size <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a94e-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="6a94e-108">InputObjectImport</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a94e-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="6a94e-109">ResourceIdCreate</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a94e-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="6a94e-110">ResourceIdImport</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a94e-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a94e-111">DESCRIPTION</span></span>
<span data-ttu-id="6a94e-112">Командлет **Add-AzManagedHsmKey** создает ключ в управляемом HSM в службе HSM, управляемом Azure, или импортирует ключ в управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="6a94e-112">The **Add-AzManagedHsmKey** cmdlet creates a key in a managed HSM in Azure Managed Hsm or imports a key into a managed HSM.</span></span>
<span data-ttu-id="6a94e-113">Используйте этот командлет для добавления клавиш одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="6a94e-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="6a94e-114">Создание ключа с ключевыми атрибутами по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6a94e-114">Create a key with default key attributes</span></span>
- <span data-ttu-id="6a94e-115">Создание ключа с заданными ключевыми атрибутами</span><span class="sxs-lookup"><span data-stu-id="6a94e-115">Create a key with given key attributes</span></span>
- <span data-ttu-id="6a94e-116">Импорт ключа из PFX-файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="6a94e-116">Import a key from a .pfx file on your computer.</span></span>
<span data-ttu-id="6a94e-117">Для любой из этих операций можно задать ключевые атрибуты или оставить параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6a94e-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="6a94e-118">При создании или импорте ключа с таким же именем, что и у существующего ключа в управляемом HSM-коде, исходный ключ обновляется с учетом значений, которые вы указали для нового ключа.</span><span class="sxs-lookup"><span data-stu-id="6a94e-118">If you create or import a key that has the same name as an existing key in your managed HSM, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="6a94e-119">Вы можете получить доступ к предыдущим значениям, используя универсальный код ресурса (URI) для указанной версии ключа.</span><span class="sxs-lookup"><span data-stu-id="6a94e-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="6a94e-120">Чтобы узнать о ключевых версиях и структуре URI, ознакомьтесь со статьей [разделы и секреты](http://go.microsoft.com/fwlink/?linkid=518560) в управляемой документации по API для функции HSM RESTful.</span><span class="sxs-lookup"><span data-stu-id="6a94e-120">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Managed HSM REST API documentation.</span></span>

## <span data-ttu-id="6a94e-121">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a94e-121">EXAMPLES</span></span>

### <span data-ttu-id="6a94e-122">Пример 1: создание ключа RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="6a94e-122">Example 1: Create a RSA-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType RSA

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 7:55:43 AM
Updated        : 10/14/2020 7:55:43 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="6a94e-123">Эта команда создает ключ RSA-HSM с именем TestKey в Managed HSM TestKey с именем testmhsm.</span><span class="sxs-lookup"><span data-stu-id="6a94e-123">This command creates a RSA-HSM key named testkey in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="6a94e-124">Пример 2: создание ключа EC-HSM</span><span class="sxs-lookup"><span data-stu-id="6a94e-124">Example 2: Create a EC-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType EC -CurveName P-256

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="6a94e-125">Эта команда создает ключ EC-HSM, именуемый TestKey, с помощью кривой P-256 в управляемом HSM TestKey с именем testmhsm.</span><span class="sxs-lookup"><span data-stu-id="6a94e-125">This command creates a EC-HSM key named testkey using P-256 curve in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="6a94e-126">Пример 3: создание ключа с нестандартными значениями из Oct-HSM</span><span class="sxs-lookup"><span data-stu-id="6a94e-126">Example 3: Create a oct-HSM key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType oct -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="6a94e-127">Первая команда сохраняет значения для расшифровки и проверки в переменной $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="6a94e-127">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="6a94e-128">Вторая команда создает объект **DateTime** , определенный в формате UTC, с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="6a94e-128">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="6a94e-129">Этот объект указывает на время в будущем на два года.</span><span class="sxs-lookup"><span data-stu-id="6a94e-129">That object specifies a time two years in the future.</span></span> <span data-ttu-id="6a94e-130">Команда сохраняет эту дату в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="6a94e-130">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="6a94e-131">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6a94e-131">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="6a94e-132">Третья команда создает объект **DateTime** с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="6a94e-132">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="6a94e-133">Этот объект указывает текущее время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="6a94e-133">That object specifies current UTC time.</span></span> <span data-ttu-id="6a94e-134">Команда сохраняет эту дату в переменной $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="6a94e-134">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="6a94e-135">Последняя команда создает ключ с именем TestKey, который является ключом Oct-HSM.</span><span class="sxs-lookup"><span data-stu-id="6a94e-135">The final command creates a key named testkey that is an oct-HSM key.</span></span> <span data-ttu-id="6a94e-136">Команда задает значения разрешенных операций с ключами, сохраненными $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="6a94e-136">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="6a94e-137">В команде указаны значения времени для параметров *Expires* и *NotBefore* , созданных в предыдущих командах, а также теги для высокого уровня важности и.</span><span class="sxs-lookup"><span data-stu-id="6a94e-137">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="6a94e-138">Новый ключ отключен.</span><span class="sxs-lookup"><span data-stu-id="6a94e-138">The new key is disabled.</span></span> <span data-ttu-id="6a94e-139">Это можно сделать с помощью командлета **Update-AzManagedHsmKey** .</span><span class="sxs-lookup"><span data-stu-id="6a94e-139">You can enable it by using the **Update-AzManagedHsmKey** cmdlet.</span></span>

## <span data-ttu-id="6a94e-140">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a94e-140">PARAMETERS</span></span>

### <span data-ttu-id="6a94e-141">-CurveName</span><span class="sxs-lookup"><span data-stu-id="6a94e-141">-CurveName</span></span>
<span data-ttu-id="6a94e-142">Указывает имя кривой для криптографии эллиптических кривых, это значение допустимо, если KeyType — EC.</span><span class="sxs-lookup"><span data-stu-id="6a94e-142">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

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

### <span data-ttu-id="6a94e-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a94e-143">-DefaultProfile</span></span>
<span data-ttu-id="6a94e-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a94e-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a94e-145">-Отключение</span><span class="sxs-lookup"><span data-stu-id="6a94e-145">-Disable</span></span>
<span data-ttu-id="6a94e-146">Указывает на то, что для добавляемого ключа задано начальное состояние "отключено".</span><span class="sxs-lookup"><span data-stu-id="6a94e-146">Indicates that the key you are adding is set to an initial state of disabled.</span></span>
<span data-ttu-id="6a94e-147">Любая попытка использования ключа завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="6a94e-147">Any attempt to use the key will fail.</span></span>
<span data-ttu-id="6a94e-148">Используйте этот параметр, если нужно предварительно загрузить ключи, которые нужно включить в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="6a94e-148">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="6a94e-149">-Истекает</span><span class="sxs-lookup"><span data-stu-id="6a94e-149">-Expires</span></span>
<span data-ttu-id="6a94e-150">Задает время окончания срока действия ключа в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="6a94e-150">Specifies the expiration time of the key in UTC.</span></span>
<span data-ttu-id="6a94e-151">Если не указано, срок действия ключа не истекает.</span><span class="sxs-lookup"><span data-stu-id="6a94e-151">If not specified, key will not expire.</span></span>

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

### <span data-ttu-id="6a94e-152">-HsmName</span><span class="sxs-lookup"><span data-stu-id="6a94e-152">-HsmName</span></span>
<span data-ttu-id="6a94e-153">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="6a94e-153">HSM name.</span></span> <span data-ttu-id="6a94e-154">Командлет создает полное доменное имя управляемого HSM-файла на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="6a94e-154">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a94e-155">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a94e-155">-InputObject</span></span>
<span data-ttu-id="6a94e-156">Объект HSM.</span><span class="sxs-lookup"><span data-stu-id="6a94e-156">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a94e-157">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="6a94e-157">-KeyFilePassword</span></span>
<span data-ttu-id="6a94e-158">Пароль локального файла, содержащего ключевой материал для импорта.</span><span class="sxs-lookup"><span data-stu-id="6a94e-158">Password of the local file containing the key material to be imported.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a94e-159">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="6a94e-159">-KeyFilePath</span></span>
<span data-ttu-id="6a94e-160">Путь к локальному файлу, содержащему ключевой материал для импорта.</span><span class="sxs-lookup"><span data-stu-id="6a94e-160">Path to the local file containing the key material to be imported.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a94e-161">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="6a94e-161">-KeyOps</span></span>
<span data-ttu-id="6a94e-162">Операции, которые можно выполнить с ключом.</span><span class="sxs-lookup"><span data-stu-id="6a94e-162">The operations that can be performed with the key.</span></span>
<span data-ttu-id="6a94e-163">Если этот режим отсутствует, можно выполнить все операции.</span><span class="sxs-lookup"><span data-stu-id="6a94e-163">If not present, all operations can be performed.</span></span>

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

### <span data-ttu-id="6a94e-164">-KeyType</span><span class="sxs-lookup"><span data-stu-id="6a94e-164">-KeyType</span></span>
<span data-ttu-id="6a94e-165">Задает тип ключа для этого ключа.</span><span class="sxs-lookup"><span data-stu-id="6a94e-165">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a94e-166">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6a94e-166">-Name</span></span>
<span data-ttu-id="6a94e-167">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="6a94e-167">Key name.</span></span>
<span data-ttu-id="6a94e-168">Командлет конструирует полное доменное имя ключа из управляемого имени HSM, в настоящее время выбранной среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="6a94e-168">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a94e-169">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="6a94e-169">-NotBefore</span></span>
<span data-ttu-id="6a94e-170">Время в формате UTC, до которого клавиша не может быть использована.</span><span class="sxs-lookup"><span data-stu-id="6a94e-170">The UTC time before which the key can't be used.</span></span>
<span data-ttu-id="6a94e-171">Если не указано, ограничение не действует.</span><span class="sxs-lookup"><span data-stu-id="6a94e-171">If not specified, there is no limitation.</span></span>

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

### <span data-ttu-id="6a94e-172">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a94e-172">-ResourceId</span></span>
<span data-ttu-id="6a94e-173">Идентификатор ресурса HSM.</span><span class="sxs-lookup"><span data-stu-id="6a94e-173">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a94e-174">-Size</span><span class="sxs-lookup"><span data-stu-id="6a94e-174">-Size</span></span>
<span data-ttu-id="6a94e-175">Размер ключа RSA в битах.</span><span class="sxs-lookup"><span data-stu-id="6a94e-175">RSA key size, in bits.</span></span>
<span data-ttu-id="6a94e-176">Если он не указан, служба обеспечивает безопасность по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6a94e-176">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a94e-177">-Тег</span><span class="sxs-lookup"><span data-stu-id="6a94e-177">-Tag</span></span>
<span data-ttu-id="6a94e-178">Хэш-таблица, представляющая Ключевые теги.</span><span class="sxs-lookup"><span data-stu-id="6a94e-178">A hashtable representing key tags.</span></span>

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

### <span data-ttu-id="6a94e-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a94e-179">-Confirm</span></span>
<span data-ttu-id="6a94e-180">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6a94e-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a94e-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a94e-181">-WhatIf</span></span>
<span data-ttu-id="6a94e-182">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6a94e-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a94e-183">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6a94e-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a94e-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a94e-184">CommonParameters</span></span>
<span data-ttu-id="6a94e-185">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a94e-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a94e-186">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a94e-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a94e-187">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a94e-187">INPUTS</span></span>

### <span data-ttu-id="6a94e-188">Microsoft. Azure. Commands. KeyVault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6a94e-188">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="6a94e-189">System. String</span><span class="sxs-lookup"><span data-stu-id="6a94e-189">System.String</span></span>

## <span data-ttu-id="6a94e-190">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a94e-190">OUTPUTS</span></span>

### <span data-ttu-id="6a94e-191">Microsoft. Azure. Commands. KeyVault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6a94e-191">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="6a94e-192">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a94e-192">NOTES</span></span>

## <span data-ttu-id="6a94e-193">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a94e-193">RELATED LINKS</span></span>

[<span data-ttu-id="6a94e-194">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6a94e-194">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="6a94e-195">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6a94e-195">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="6a94e-196">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6a94e-196">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="6a94e-197">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="6a94e-197">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="6a94e-198">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6a94e-198">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="6a94e-199">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6a94e-199">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)
