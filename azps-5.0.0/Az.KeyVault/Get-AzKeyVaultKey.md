---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 515a238aa7e6bb49117dd38954dbb67f840abd9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248661"
---
# <span data-ttu-id="1e0fe-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e0fe-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="1e0fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0fe-103">Получает ключи хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="1e0fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e0fe-104">SYNTAX</span></span>

### <span data-ttu-id="1e0fe-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e0fe-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e0fe-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="1e0fe-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e0fe-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="1e0fe-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e0fe-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="1e0fe-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e0fe-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="1e0fe-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e0fe-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="1e0fe-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e0fe-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="1e0fe-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e0fe-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="1e0fe-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e0fe-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="1e0fe-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e0fe-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e0fe-114">DESCRIPTION</span></span>
<span data-ttu-id="1e0fe-115">Командлет **Get-AzKeyVaultKey** получает ключи Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="1e0fe-116">Этот командлет получает определенный **Microsoft. Azure. Commands. KeyVault. Models. KeyBundle** или список всех объектов **KeyBundle** в хранилище ключей или по версии.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="1e0fe-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e0fe-117">EXAMPLES</span></span>

### <span data-ttu-id="1e0fe-118">Пример 1: получение всех ключей в хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="1e0fe-118">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e0fe-119">Эта команда получает все ключи из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="1e0fe-120">Пример 2: получение текущей версии ключа</span><span class="sxs-lookup"><span data-stu-id="1e0fe-120">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e0fe-121">Эта команда получает текущую версию ключа с именем Test1 в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="1e0fe-122">Пример 3: получение всех версий ключа</span><span class="sxs-lookup"><span data-stu-id="1e0fe-122">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e0fe-123">Эта команда получает ключ с именем ITPfx в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-123">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="1e0fe-124">Пример 4: получение определенной версии ключа</span><span class="sxs-lookup"><span data-stu-id="1e0fe-124">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e0fe-125">Эта команда возвращает определенную версию ключа test1 в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="1e0fe-126">После выполнения этой команды вы можете просматривать различные свойства ключа, перемещаясь по объекту $Key.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="1e0fe-127">Пример 5: получение всех ключей, которые были удалены, но не очищены для этого хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="1e0fe-127">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="1e0fe-128">Эта команда возвращает все разделы, которые были ранее удалены, но не очищены, в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="1e0fe-129">Пример 6: получение ключа ITPfx, который был удален, но не очищен для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="1e0fe-130">Эта команда возвращает клавишу test3, которая была ранее удалена, но не очищена, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="1e0fe-131">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного ключа.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="1e0fe-132">Пример 7: получение всех ключей в хранилище ключей с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="1e0fe-132">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="1e0fe-133">Эта команда получает все ключи из хранилища ключей Contoso, которые начинаются с "Test".</span><span class="sxs-lookup"><span data-stu-id="1e0fe-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="1e0fe-134">Пример 8: Загрузка открытого ключа в виде PEM-файла</span><span class="sxs-lookup"><span data-stu-id="1e0fe-134">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="1e0fe-135">Открытый ключ ключа RSA можно загрузить, указав `-OutFile` параметр.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-135">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="1e0fe-136">Это один из этапов импорта ключей, защищенных с защитой от HSM, в Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-136">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="1e0fe-137">Обнаружить https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="1e0fe-137">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="1e0fe-138">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e0fe-138">PARAMETERS</span></span>

### <span data-ttu-id="1e0fe-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0fe-139">-DefaultProfile</span></span>
<span data-ttu-id="1e0fe-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1e0fe-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e0fe-141">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="1e0fe-141">-IncludeVersions</span></span>
<span data-ttu-id="1e0fe-142">Указывает на то, что этот командлет получает все версии ключа.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-142">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="1e0fe-143">Текущая версия ключа является первой в списке.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-143">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="1e0fe-144">Если указан этот параметр, необходимо также указать параметры *Name* и *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="1e0fe-144">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="1e0fe-145">Если параметр *IncludeVersions* не указан, этот командлет получает текущую версию ключа с указанным *именем*.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-145">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, ByInputObjectKeyVersions, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e0fe-146">-InputObject</span></span>
<span data-ttu-id="1e0fe-147">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-147">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-148">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="1e0fe-148">-InRemovedState</span></span>
<span data-ttu-id="1e0fe-149">Указывает, нужно ли отображать ранее удаленные разделы в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-149">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-150">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e0fe-150">-Name</span></span>
<span data-ttu-id="1e0fe-151">Указывает имя набора ключей, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-151">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-152">-Файл</span><span class="sxs-lookup"><span data-stu-id="1e0fe-152">-OutFile</span></span>
<span data-ttu-id="1e0fe-153">Указывает выходной файл, для которого этот командлет сохраняет ключ.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-153">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="1e0fe-154">Открытый ключ по умолчанию сохраняется в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-154">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="1e0fe-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e0fe-155">-ResourceId</span></span>
<span data-ttu-id="1e0fe-156">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-156">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-157">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1e0fe-157">-VaultName</span></span>
<span data-ttu-id="1e0fe-158">Указывает имя хранилища ключей, из которого этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-158">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="1e0fe-159">Этот командлет создает полное доменное имя (FQDN) для хранилища ключей, основываясь на имени, указанном этим параметром, и в выбранной среде.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-159">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-160">-Version</span><span class="sxs-lookup"><span data-stu-id="1e0fe-160">-Version</span></span>
<span data-ttu-id="1e0fe-161">Указывает версию ключа.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-161">Specifies the key version.</span></span>
<span data-ttu-id="1e0fe-162">Этот командлет создает полное доменное имя ключа на основе имени хранилища ключей, текущей выбранной среды, имени ключа и версии ключа.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-162">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByInputObjectKeyName, ByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e0fe-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0fe-163">CommonParameters</span></span>
<span data-ttu-id="1e0fe-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e0fe-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e0fe-165">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e0fe-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0fe-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e0fe-166">INPUTS</span></span>

### <span data-ttu-id="1e0fe-167">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1e0fe-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1e0fe-168">System. String</span><span class="sxs-lookup"><span data-stu-id="1e0fe-168">System.String</span></span>

## <span data-ttu-id="1e0fe-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e0fe-169">OUTPUTS</span></span>

### <span data-ttu-id="1e0fe-170">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1e0fe-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="1e0fe-171">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e0fe-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="1e0fe-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1e0fe-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="1e0fe-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e0fe-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="1e0fe-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e0fe-174">NOTES</span></span>

## <span data-ttu-id="1e0fe-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e0fe-175">RELATED LINKS</span></span>

[<span data-ttu-id="1e0fe-176">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e0fe-176">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="1e0fe-177">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e0fe-177">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="1e0fe-178">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="1e0fe-178">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="1e0fe-179">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="1e0fe-179">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

