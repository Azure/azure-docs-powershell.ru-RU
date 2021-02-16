---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 842e571794fbf257473843ab824c1e6497f5c4a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226441"
---
# <span data-ttu-id="31982-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31982-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="31982-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31982-102">SYNOPSIS</span></span>
<span data-ttu-id="31982-103">Получает клавиши сейфа.</span><span class="sxs-lookup"><span data-stu-id="31982-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="31982-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31982-104">SYNTAX</span></span>

### <span data-ttu-id="31982-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31982-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="31982-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="31982-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-108">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="31982-108">HsmByKeyName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-109">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="31982-109">HsmByVaultName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-110">HsmByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="31982-110">HsmByKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-111">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="31982-111">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-112">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="31982-112">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-113">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="31982-113">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-114">HsmByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="31982-114">HsmByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-115">HsmByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="31982-115">HsmByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-116">HsmByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="31982-116">HsmByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-117">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="31982-117">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-118">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="31982-118">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-119">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="31982-119">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-120">HsmByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="31982-120">HsmByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-121">HsmByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="31982-121">HsmByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31982-122">HsmByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="31982-122">HsmByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31982-123">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31982-123">DESCRIPTION</span></span>
<span data-ttu-id="31982-124">Для получения ключей хранилища Azure задаются **клавиши Get-AzKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="31982-124">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="31982-125">Этот командлет возвращает конкретный **microsoft.Azure.Commands.KeyVault.Models.KeyBundle** или список всех объектов **keyBundle** в хранилище ключа или по версии.</span><span class="sxs-lookup"><span data-stu-id="31982-125">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="31982-126">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31982-126">EXAMPLES</span></span>

### <span data-ttu-id="31982-127">Пример 1. Все клавиши в хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="31982-127">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="31982-128">Эта команда получает все клавиши в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="31982-128">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="31982-129">Пример 2. Получить текущую версию ключа</span><span class="sxs-lookup"><span data-stu-id="31982-129">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="31982-130">Эта команда получает текущую версию ключа test1 в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="31982-130">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="31982-131">Пример 3. Получить все версии ключа</span><span class="sxs-lookup"><span data-stu-id="31982-131">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="31982-132">Эта команда получает все версии ключа ITPfx в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="31982-132">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="31982-133">Пример 4. Получить конкретную версию ключа</span><span class="sxs-lookup"><span data-stu-id="31982-133">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="31982-134">Эта команда получает определенную версию ключа test1 в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="31982-134">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="31982-135">После этого можно проверить различные свойства клавиши, переходя по $Key объекту.</span><span class="sxs-lookup"><span data-stu-id="31982-135">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="31982-136">Пример 5. Получите все удаленные, но не удаленные ключи для этого хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="31982-136">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
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

<span data-ttu-id="31982-137">Эта команда получает все ключи, которые были ранее удалены, но не удалены, в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="31982-137">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="31982-138">Пример 6. Получает ключ ITPfx, который был удален, но не был удален для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="31982-138">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="31982-139">Эта команда получает ключ test3, который ранее был удален, но не был удален, в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="31982-139">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="31982-140">Эта команда возвращает метаданные, такие как дата удаления и запланированная дата удаления этого ключа.</span><span class="sxs-lookup"><span data-stu-id="31982-140">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="31982-141">Пример 7. Все клавиши в хранилище ключей с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="31982-141">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="31982-142">Эта команда получает все ключи в хранилище ключей Contoso, которые начинаются с "test".</span><span class="sxs-lookup"><span data-stu-id="31982-142">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="31982-143">Пример 8. Скачивание открытого ключа в PEM-файл</span><span class="sxs-lookup"><span data-stu-id="31982-143">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="31982-144">Вы можете скачать открытый ключ ключа RSA, указав `-OutFile` параметр.</span><span class="sxs-lookup"><span data-stu-id="31982-144">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="31982-145">Это один из этапов импорта защищенных HSM ключей в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="31982-145">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="31982-146">См. https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="31982-146">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="31982-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31982-147">PARAMETERS</span></span>

### <span data-ttu-id="31982-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31982-148">-DefaultProfile</span></span>
<span data-ttu-id="31982-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="31982-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31982-150">-HsmName</span><span class="sxs-lookup"><span data-stu-id="31982-150">-HsmName</span></span>
<span data-ttu-id="31982-151">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="31982-151">HSM name.</span></span> <span data-ttu-id="31982-152">С его учетом именем и выбранной средой строится FQDN управляемой HSM- среды.</span><span class="sxs-lookup"><span data-stu-id="31982-152">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName, HsmByVaultName, HsmByKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31982-153">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="31982-153">-HsmObject</span></span>
<span data-ttu-id="31982-154">Объект HSM.</span><span class="sxs-lookup"><span data-stu-id="31982-154">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObjectVaultName, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31982-155">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="31982-155">-HsmResourceId</span></span>
<span data-ttu-id="31982-156">ИД ресурса HSM.</span><span class="sxs-lookup"><span data-stu-id="31982-156">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceIdVaultName, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31982-157">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="31982-157">-IncludeVersions</span></span>
<span data-ttu-id="31982-158">Указывает на то, что этот cmdlet получает все версии ключа.</span><span class="sxs-lookup"><span data-stu-id="31982-158">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="31982-159">Текущая версия ключа является первой в списке.</span><span class="sxs-lookup"><span data-stu-id="31982-159">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="31982-160">Если вы указали этот параметр, необходимо также указать параметры *Name* и *VaultName.*</span><span class="sxs-lookup"><span data-stu-id="31982-160">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="31982-161">Если не указать параметр *IncludeVersions,* этот cmdlet получит текущую версию ключа с указанным *именем.*</span><span class="sxs-lookup"><span data-stu-id="31982-161">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, HsmByKeyVersions, ByInputObjectKeyVersions, HsmByInputObjectKeyVersions, ByResourceIdKeyVersions, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31982-162">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31982-162">-InputObject</span></span>
<span data-ttu-id="31982-163">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="31982-163">KeyVault object.</span></span>

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

### <span data-ttu-id="31982-164">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="31982-164">-InRemovedState</span></span>
<span data-ttu-id="31982-165">Указывает, нужно ли показывать ранее удаленные ключи в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="31982-165">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31982-166">-Name</span><span class="sxs-lookup"><span data-stu-id="31982-166">-Name</span></span>
<span data-ttu-id="31982-167">Имя набора ключей, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="31982-167">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, HsmByKeyName, HsmByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="31982-168">-OutFile</span><span class="sxs-lookup"><span data-stu-id="31982-168">-OutFile</span></span>
<span data-ttu-id="31982-169">Определяет выходной файл, для которого этот cmdlet сохраняет ключ.</span><span class="sxs-lookup"><span data-stu-id="31982-169">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="31982-170">По умолчанию открытый ключ сохранен в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="31982-170">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="31982-171">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31982-171">-ResourceId</span></span>
<span data-ttu-id="31982-172">ИД ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="31982-172">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31982-173">-VaultName</span><span class="sxs-lookup"><span data-stu-id="31982-173">-VaultName</span></span>
<span data-ttu-id="31982-174">Указывает имя хранилища ключей, из которого этот cmdlet получает ключи.</span><span class="sxs-lookup"><span data-stu-id="31982-174">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="31982-175">Этот cmdlet конструирует полное доменное имя (FQDN) ключа хранилища на основе имени, указанного этим параметром, и выбранной среды.</span><span class="sxs-lookup"><span data-stu-id="31982-175">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="31982-176">-Версия</span><span class="sxs-lookup"><span data-stu-id="31982-176">-Version</span></span>
<span data-ttu-id="31982-177">Указывает версию ключа.</span><span class="sxs-lookup"><span data-stu-id="31982-177">Specifies the key version.</span></span>
<span data-ttu-id="31982-178">Этот cmdlet конструировать FQDN ключа на основе имени ключа хранилища, выбранной среды, имени ключа и версии ключа.</span><span class="sxs-lookup"><span data-stu-id="31982-178">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName, ByInputObjectKeyName, HsmByInputObjectKeyName, ByResourceIdKeyName, HsmByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31982-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31982-179">CommonParameters</span></span>
<span data-ttu-id="31982-180">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31982-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31982-181">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31982-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31982-182">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31982-182">INPUTS</span></span>

### <span data-ttu-id="31982-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="31982-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="31982-184">System.String</span><span class="sxs-lookup"><span data-stu-id="31982-184">System.String</span></span>

## <span data-ttu-id="31982-185">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31982-185">OUTPUTS</span></span>

### <span data-ttu-id="31982-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="31982-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="31982-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31982-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="31982-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="31982-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="31982-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31982-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="31982-190">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31982-190">NOTES</span></span>

## <span data-ttu-id="31982-191">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31982-191">RELATED LINKS</span></span>

[<span data-ttu-id="31982-192">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31982-192">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="31982-193">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31982-193">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="31982-194">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="31982-194">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="31982-195">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="31982-195">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

