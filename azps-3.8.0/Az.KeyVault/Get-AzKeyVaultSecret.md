---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: af2baec6b25b770c30f5f3207e6ed6b6a4b423f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065158"
---
# <span data-ttu-id="f754b-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f754b-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="f754b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f754b-102">SYNOPSIS</span></span>
<span data-ttu-id="f754b-103">Возвращает секреты в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f754b-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="f754b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f754b-104">SYNTAX</span></span>

### <span data-ttu-id="f754b-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f754b-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f754b-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="f754b-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f754b-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="f754b-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f754b-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="f754b-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f754b-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="f754b-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f754b-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="f754b-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f754b-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="f754b-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f754b-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="f754b-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f754b-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="f754b-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f754b-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f754b-114">DESCRIPTION</span></span>
<span data-ttu-id="f754b-115">Командлет **Get-AzKeyVaultSecret** получает секреты в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f754b-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="f754b-116">Этот командлет получает определенный секрет или все секреты в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f754b-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="f754b-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f754b-117">EXAMPLES</span></span>

### <span data-ttu-id="f754b-118">Пример 1: получение всех текущих версий всех секретных данных в хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="f754b-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="f754b-119">Эта команда возвращает текущие версии всех секретных данных в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="f754b-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="f754b-120">Пример 2: получение всех версий определенного секрета</span><span class="sxs-lookup"><span data-stu-id="f754b-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="f754b-121">Эта команда получает все версии секрета с именем secret1 в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="f754b-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="f754b-122">Пример 3: получение текущей версии определенного секрета</span><span class="sxs-lookup"><span data-stu-id="f754b-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="f754b-123">Эта команда получает текущую версию секрета с именем secret1 в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="f754b-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="f754b-124">Пример 4: получение определенной версии определенного секрета</span><span class="sxs-lookup"><span data-stu-id="f754b-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="f754b-125">Эта команда возвращает определенную версию секрета с именем secret1 в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="f754b-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="f754b-126">Пример 5: получение простого текстового значения текущей версии определенного секрета</span><span class="sxs-lookup"><span data-stu-id="f754b-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is:" $secret.SecretValueText

Secret Value is: P@ssw0rd
```

<span data-ttu-id="f754b-127">Эти команды получают текущую версию секрета с именем ITSecret и выводят на экран значение в формате обычного текста этого секрета.</span><span class="sxs-lookup"><span data-stu-id="f754b-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="f754b-128">Пример 6: получение всех секретов, которые были удалены, но не очищены для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f754b-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         : 
Tags                 :
```

<span data-ttu-id="f754b-129">Эта команда получает все секретные данные, которые были ранее удалены, но не очищены, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="f754b-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="f754b-130">Пример 7: возвращает секретный ITSecret, который был удален, но не очищен для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f754b-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="f754b-131">Эта команда получает секрет "secret1", который ранее был удален, но не очищен, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="f754b-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="f754b-132">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного секрета.</span><span class="sxs-lookup"><span data-stu-id="f754b-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="f754b-133">Пример 8: получение всех текущих версий всех секретных данных в ключевом хранилище с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="f754b-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name "secret*"

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="f754b-134">Эта команда возвращает текущие версии всех секретных данных в хранилище ключей, именуемом Contoso, и начинается с секретности.</span><span class="sxs-lookup"><span data-stu-id="f754b-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="f754b-135">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f754b-135">PARAMETERS</span></span>

### <span data-ttu-id="f754b-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f754b-136">-DefaultProfile</span></span>
<span data-ttu-id="f754b-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f754b-137">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f754b-138">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="f754b-138">-IncludeVersions</span></span>
<span data-ttu-id="f754b-139">Указывает на то, что этот командлет получает все версии секрета.</span><span class="sxs-lookup"><span data-stu-id="f754b-139">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="f754b-140">Текущая версия секрета является первой в списке.</span><span class="sxs-lookup"><span data-stu-id="f754b-140">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="f754b-141">Если указан этот параметр, необходимо также указать параметры *Name* и *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="f754b-141">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="f754b-142">Если параметр *IncludeVersions* не указан, этот командлет получает текущую версию секрета с указанным *именем*.</span><span class="sxs-lookup"><span data-stu-id="f754b-142">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f754b-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f754b-143">-InputObject</span></span>
<span data-ttu-id="f754b-144">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f754b-144">KeyVault Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f754b-145">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f754b-145">-InRemovedState</span></span>
<span data-ttu-id="f754b-146">Указывает, нужно ли отображать ранее удаленные секреты в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f754b-146">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="f754b-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f754b-147">-Name</span></span>
<span data-ttu-id="f754b-148">Указывает имя секрета для получения.</span><span class="sxs-lookup"><span data-stu-id="f754b-148">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f754b-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f754b-149">-ResourceId</span></span>
<span data-ttu-id="f754b-150">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f754b-150">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f754b-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f754b-151">-VaultName</span></span>
<span data-ttu-id="f754b-152">Указывает имя хранилища ключей, к которому относится секрет.</span><span class="sxs-lookup"><span data-stu-id="f754b-152">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="f754b-153">Этот командлет создает полное доменное имя (FQDN) хранилища ключей, основываясь на имени, которое указывает этот параметр, и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="f754b-153">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f754b-154">-Version</span><span class="sxs-lookup"><span data-stu-id="f754b-154">-Version</span></span>
<span data-ttu-id="f754b-155">Указывает секретную версию.</span><span class="sxs-lookup"><span data-stu-id="f754b-155">Specifies the secret version.</span></span>
<span data-ttu-id="f754b-156">Этот командлет создает полное доменное имя секрета на основе имени хранилища ключей, текущей выбранной среды, имени секрета и секретной версии.</span><span class="sxs-lookup"><span data-stu-id="f754b-156">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f754b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f754b-157">CommonParameters</span></span>
<span data-ttu-id="f754b-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f754b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f754b-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f754b-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f754b-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f754b-160">INPUTS</span></span>

### <span data-ttu-id="f754b-161">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f754b-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f754b-162">System. String</span><span class="sxs-lookup"><span data-stu-id="f754b-162">System.String</span></span>

## <span data-ttu-id="f754b-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f754b-163">OUTPUTS</span></span>

### <span data-ttu-id="f754b-164">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f754b-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="f754b-165">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f754b-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="f754b-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f754b-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="f754b-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f754b-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="f754b-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="f754b-168">NOTES</span></span>

## <span data-ttu-id="f754b-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f754b-169">RELATED LINKS</span></span>

[<span data-ttu-id="f754b-170">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f754b-170">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="f754b-171">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="f754b-171">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="f754b-172">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f754b-172">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

