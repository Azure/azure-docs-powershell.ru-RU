---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: cab778247e6e3ae9db3549beae7fcd7495526757
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412101"
---
# <span data-ttu-id="89674-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="89674-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="89674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89674-102">SYNOPSIS</span></span>
<span data-ttu-id="89674-103">Получает клавиши сейфа.</span><span class="sxs-lookup"><span data-stu-id="89674-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="89674-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89674-104">SYNTAX</span></span>

### <span data-ttu-id="89674-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89674-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89674-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="89674-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89674-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="89674-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89674-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="89674-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89674-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="89674-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89674-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="89674-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89674-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="89674-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89674-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="89674-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89674-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="89674-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89674-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89674-114">DESCRIPTION</span></span>
<span data-ttu-id="89674-115">Для получения ключей хранилища Azure задаются **клавиши Get-AzKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="89674-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="89674-116">Этот командлет возвращает конкретный **microsoft.Azure.Commands.KeyVault.Models.KeyBundle** или список всех объектов **keyBundle** в хранилище ключа или по версии.</span><span class="sxs-lookup"><span data-stu-id="89674-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="89674-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89674-117">EXAMPLES</span></span>

### <span data-ttu-id="89674-118">Пример 1. Получить все клавиши в хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="89674-118">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="89674-119">Эта команда получает все клавиши в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="89674-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="89674-120">Пример 2. Получить текущую версию ключа</span><span class="sxs-lookup"><span data-stu-id="89674-120">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="89674-121">Эта команда получает текущую версию ключа test1 в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="89674-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="89674-122">Пример 3. Получить все версии ключа</span><span class="sxs-lookup"><span data-stu-id="89674-122">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="89674-123">Эта команда получает все версии ключа ITPfx в ключе Contoso.</span><span class="sxs-lookup"><span data-stu-id="89674-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="89674-124">Пример 4. Получить конкретную версию ключа</span><span class="sxs-lookup"><span data-stu-id="89674-124">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="89674-125">Эта команда получает определенную версию ключа test1 в хранилище ключей с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="89674-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="89674-126">После этого можно проверить различные свойства клавиши, переходя по $Key объекту.</span><span class="sxs-lookup"><span data-stu-id="89674-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="89674-127">Пример 5. Получите все ключи, которые были удалены, но не удалены из этого сейфа.</span><span class="sxs-lookup"><span data-stu-id="89674-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="89674-128">Эта команда получает все ключи, которые были ранее удалены, но не удалены, в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="89674-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="89674-129">Пример 6. Получает ключ ITPfx, который был удален, но не был удален для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="89674-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="89674-130">Эта команда получает ключ test3, который ранее был удален, но не был удален, в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="89674-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="89674-131">Эта команда возвращает метаданные, такие как дата удаления и запланированная дата удаления этого удаленного ключа.</span><span class="sxs-lookup"><span data-stu-id="89674-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="89674-132">Пример 7. Все клавиши в хранилище ключей с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="89674-132">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="89674-133">Эта команда получает все ключи в хранилище ключей Contoso, которые начинаются с "test".</span><span class="sxs-lookup"><span data-stu-id="89674-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

## <span data-ttu-id="89674-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89674-134">PARAMETERS</span></span>

### <span data-ttu-id="89674-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89674-135">-DefaultProfile</span></span>
<span data-ttu-id="89674-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="89674-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89674-137">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="89674-137">-IncludeVersions</span></span>
<span data-ttu-id="89674-138">Указывает на то, что этот cmdlet получает все версии ключа.</span><span class="sxs-lookup"><span data-stu-id="89674-138">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="89674-139">Текущая версия ключа является первой в списке.</span><span class="sxs-lookup"><span data-stu-id="89674-139">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="89674-140">Если вы указали этот параметр, необходимо также указать параметры *Name* и *VaultName.*</span><span class="sxs-lookup"><span data-stu-id="89674-140">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="89674-141">Если не указать параметр *IncludeVersions,* этот cmdlet получит текущую версию ключа с указанным *именем.*</span><span class="sxs-lookup"><span data-stu-id="89674-141">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="89674-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89674-142">-InputObject</span></span>
<span data-ttu-id="89674-143">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="89674-143">KeyVault object.</span></span>

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

### <span data-ttu-id="89674-144">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="89674-144">-InRemovedState</span></span>
<span data-ttu-id="89674-145">Указывает, нужно ли показывать ранее удаленные ключи в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="89674-145">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="89674-146">-Name</span><span class="sxs-lookup"><span data-stu-id="89674-146">-Name</span></span>
<span data-ttu-id="89674-147">Имя набора ключей, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="89674-147">Specifies the name of the key bundle to get.</span></span>

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

### <span data-ttu-id="89674-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89674-148">-ResourceId</span></span>
<span data-ttu-id="89674-149">ИД ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="89674-149">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="89674-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="89674-150">-VaultName</span></span>
<span data-ttu-id="89674-151">Указывает имя хранилища ключей, из которого этот cmdlet получает ключи.</span><span class="sxs-lookup"><span data-stu-id="89674-151">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="89674-152">Этот cmdlet конструирует полное доменное имя (FQDN) ключа хранилища на основе имени, указанного этим параметром, и выбранной среды.</span><span class="sxs-lookup"><span data-stu-id="89674-152">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="89674-153">-Версия</span><span class="sxs-lookup"><span data-stu-id="89674-153">-Version</span></span>
<span data-ttu-id="89674-154">Указывает версию ключа.</span><span class="sxs-lookup"><span data-stu-id="89674-154">Specifies the key version.</span></span>
<span data-ttu-id="89674-155">Этот cmdlet строит FQDN ключа на основе имени ключа хранилища, выбранной среды, имени ключа и версии ключа.</span><span class="sxs-lookup"><span data-stu-id="89674-155">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="89674-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89674-156">CommonParameters</span></span>
<span data-ttu-id="89674-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89674-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89674-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89674-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89674-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89674-159">INPUTS</span></span>

### <span data-ttu-id="89674-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="89674-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="89674-161">System.String</span><span class="sxs-lookup"><span data-stu-id="89674-161">System.String</span></span>

## <span data-ttu-id="89674-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89674-162">OUTPUTS</span></span>

### <span data-ttu-id="89674-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="89674-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="89674-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="89674-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="89674-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="89674-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="89674-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="89674-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="89674-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89674-167">NOTES</span></span>

## <span data-ttu-id="89674-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89674-168">RELATED LINKS</span></span>

[<span data-ttu-id="89674-169">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="89674-169">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="89674-170">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="89674-170">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="89674-171">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="89674-171">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)


