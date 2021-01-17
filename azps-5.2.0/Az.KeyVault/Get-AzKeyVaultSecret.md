---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 18b87f6a83f335958e9c10e392d859ae307e9e87
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411748"
---
# <span data-ttu-id="a9cb7-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a9cb7-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="a9cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="a9cb7-103">Получает секрет в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="a9cb7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a9cb7-104">SYNTAX</span></span>

### <span data-ttu-id="a9cb7-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9cb7-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="a9cb7-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9cb7-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="a9cb7-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9cb7-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="a9cb7-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9cb7-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="a9cb7-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9cb7-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="a9cb7-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9cb7-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="a9cb7-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9cb7-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="a9cb7-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9cb7-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="a9cb7-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9cb7-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9cb7-114">DESCRIPTION</span></span>
<span data-ttu-id="a9cb7-115">Для секретов в ключевом сейфе есть секрет для **get-AzKeyVaultSecret.**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="a9cb7-116">Этот cmdlet получает определенную секрет или все секретные секреты в ключевом сейфе.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="a9cb7-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a9cb7-117">EXAMPLES</span></span>

### <span data-ttu-id="a9cb7-118">Пример 1. Получить все текущие версии всех секретов в ключевом сейфе</span><span class="sxs-lookup"><span data-stu-id="a9cb7-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
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

<span data-ttu-id="a9cb7-119">Эта команда получает текущие версии всех секретов в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="a9cb7-120">Пример 2. Получите все версии определенного секрета</span><span class="sxs-lookup"><span data-stu-id="a9cb7-120">Example 2: Get all versions of a specific secret</span></span>
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

<span data-ttu-id="a9cb7-121">Эта команда получает все версии секретного секретного1 в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="a9cb7-122">Пример 3. Получить текущую версию определенной секретной</span><span class="sxs-lookup"><span data-stu-id="a9cb7-122">Example 3: Get the current version of a specific secret</span></span>
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

<span data-ttu-id="a9cb7-123">Эта команда получает текущую версию секретной1 в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="a9cb7-124">Пример 4. Получите определенную версию определенного секрета</span><span class="sxs-lookup"><span data-stu-id="a9cb7-124">Example 4: Get a specific version of a specific secret</span></span>
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

<span data-ttu-id="a9cb7-125">Эта команда получает определенную версию секретного секретного1 в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="a9cb7-126">Пример 5. Получите обычное текстовое значение текущей версии определенной секретной версии</span><span class="sxs-lookup"><span data-stu-id="a9cb7-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'

# Method 1: requires PowerShell >= 7.0
PS C:\> $secretInPlainText = $secret.SecretValue | ConvertFrom-SecureString -AsPlainText

# Method 2: works on older PowerShell versions
PS C:\> $secretValueText = '';
PS C:\> $ssPtr = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue)
PS C:\> try {
    $secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR($ssPtr)
} finally {
    [System.Runtime.InteropServices.Marshal]::ZeroFreeBSTR($ssPtr)
}

# Method 3: works in ConstrainedLanguage mode
$secretInPlainText = [pscredential]::new("DoesntMatter", $secret.SecretValue).GetNetworkCredential().Password
```

<span data-ttu-id="a9cb7-127">Эти команды получают текущую версию секретного ИТ-секрета и отображают ее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

<span data-ttu-id="a9cb7-128">(Примечание. Используйте метод 3, если вы работаете в режиме PowerShell [ConstrainedLanguage,](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_language_modes?view=powershell-7.1#constrained-language-constrained-language)например на рабочих станциях с защищенным и привилегированным доступом.)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-128">(Note: use method 3 if you are working in PowerShell [ConstrainedLanguage mode](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_language_modes?view=powershell-7.1#constrained-language-constrained-language), for example, on secure/privileged access workstations.)</span></span>

### <span data-ttu-id="a9cb7-129">Пример 6. Получите все секреты, которые были удалены, но не удалены из этого сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-129">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="a9cb7-130">Эта команда возвращает все секреты, которые были ранее удалены, но не удалены, в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-130">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="a9cb7-131">Пример 7. Получает секретный ИТ-секрет, который был удален, но не удален для этого сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-131">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="a9cb7-132">Эта команда получает секретную "секрет1", которая ранее была удалена, но не была удалена, в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-132">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="a9cb7-133">Эта команда возвращает метаданные, такие как дата удаления и запланированная дата удаления этой секретной.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-133">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="a9cb7-134">Пример 8. Получите все текущие версии всех секретов в ключевом сейфе с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="a9cb7-134">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
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

<span data-ttu-id="a9cb7-135">Эта команда получает текущие версии всех секретов в сейфе Contoso, которые начинаются с "секрет".</span><span class="sxs-lookup"><span data-stu-id="a9cb7-135">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="a9cb7-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9cb7-136">PARAMETERS</span></span>

### <span data-ttu-id="a9cb7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9cb7-137">-DefaultProfile</span></span>
<span data-ttu-id="a9cb7-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a9cb7-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9cb7-139">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="a9cb7-139">-IncludeVersions</span></span>
<span data-ttu-id="a9cb7-140">Указывает на то, что этот cmdlet получает все версии секрета.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-140">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="a9cb7-141">Секретная версия является первой в списке.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-141">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="a9cb7-142">Если вы указали этот параметр, необходимо также указать параметры *Name* и *VaultName.*</span><span class="sxs-lookup"><span data-stu-id="a9cb7-142">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="a9cb7-143">Если не указать параметр *IncludeVersions,* этот cmdlet получит текущую версию секретного с указанным *именем.*</span><span class="sxs-lookup"><span data-stu-id="a9cb7-143">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="a9cb7-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9cb7-144">-InputObject</span></span>
<span data-ttu-id="a9cb7-145">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-145">KeyVault Object.</span></span>

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

### <span data-ttu-id="a9cb7-146">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a9cb7-146">-InRemovedState</span></span>
<span data-ttu-id="a9cb7-147">Определяет, нужно ли показывать в выходных данных удаленные ранее секреты.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-147">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="a9cb7-148">-Name</span><span class="sxs-lookup"><span data-stu-id="a9cb7-148">-Name</span></span>
<span data-ttu-id="a9cb7-149">Имя секрета, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-149">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a9cb7-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9cb7-150">-ResourceId</span></span>
<span data-ttu-id="a9cb7-151">ИД ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-151">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="a9cb7-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a9cb7-152">-VaultName</span></span>
<span data-ttu-id="a9cb7-153">Указывает имя ключного сейфа, к которому относится секрет.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-153">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="a9cb7-154">Этот cmdlet конструирует полное доменное имя (FQDN) ключа хранилища на основе имени, указанного этим параметром, и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-154">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="a9cb7-155">-Версия</span><span class="sxs-lookup"><span data-stu-id="a9cb7-155">-Version</span></span>
<span data-ttu-id="a9cb7-156">Указывает секретную версию.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-156">Specifies the secret version.</span></span>
<span data-ttu-id="a9cb7-157">Этот cmdlet конструируются FQDN секретного сейфа на основе имени ключа сейфа, выбранной среды, секретного имени и секретной версии.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="a9cb7-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9cb7-158">CommonParameters</span></span>
<span data-ttu-id="a9cb7-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9cb7-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9cb7-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9cb7-161">INPUTS</span></span>

### <span data-ttu-id="a9cb7-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a9cb7-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a9cb7-163">System.String</span><span class="sxs-lookup"><span data-stu-id="a9cb7-163">System.String</span></span>

## <span data-ttu-id="a9cb7-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a9cb7-164">OUTPUTS</span></span>

### <span data-ttu-id="a9cb7-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a9cb7-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="a9cb7-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a9cb7-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="a9cb7-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a9cb7-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="a9cb7-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a9cb7-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="a9cb7-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a9cb7-169">NOTES</span></span>

## <span data-ttu-id="a9cb7-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9cb7-170">RELATED LINKS</span></span>

[<span data-ttu-id="a9cb7-171">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a9cb7-171">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="a9cb7-172">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="a9cb7-172">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="a9cb7-173">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a9cb7-173">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

