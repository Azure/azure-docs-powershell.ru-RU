---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: b14e97ba09cba70a9ec571b2fbf1273de7157930
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911171"
---
# <span data-ttu-id="82dc2-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="82dc2-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="82dc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="82dc2-103">Возвращает секреты в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="82dc2-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="82dc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82dc2-104">SYNTAX</span></span>

### <span data-ttu-id="82dc2-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82dc2-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82dc2-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="82dc2-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82dc2-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="82dc2-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82dc2-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="82dc2-108">ByDeletedSecrets</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82dc2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82dc2-109">DESCRIPTION</span></span>
<span data-ttu-id="82dc2-110">Командлет **Get-AzKeyVaultSecret** получает секреты в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="82dc2-110">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="82dc2-111">Этот командлет получает определенный секрет или все секреты в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="82dc2-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="82dc2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82dc2-112">EXAMPLES</span></span>

### <span data-ttu-id="82dc2-113">Пример 1: получение всех текущих версий всех секретных данных в хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="82dc2-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="82dc2-114">Эта команда возвращает текущие версии всех секретных данных в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="82dc2-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="82dc2-115">Пример 2: получение всех версий определенного секрета</span><span class="sxs-lookup"><span data-stu-id="82dc2-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="82dc2-116">Эта команда получает все версии секрета с именем ITSecret в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="82dc2-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="82dc2-117">Пример 3: получение текущей версии определенного секрета</span><span class="sxs-lookup"><span data-stu-id="82dc2-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="82dc2-118">Эта команда получает текущую версию секрета с именем ITSecret в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="82dc2-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="82dc2-119">Пример 4: получение определенной версии определенного секрета</span><span class="sxs-lookup"><span data-stu-id="82dc2-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="82dc2-120">Эта команда возвращает определенную версию секрета с именем ITSecret в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="82dc2-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="82dc2-121">Пример 5: получение простого текстового значения текущей версии определенного секрета</span><span class="sxs-lookup"><span data-stu-id="82dc2-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="82dc2-122">Эти команды получают текущую версию секрета с именем ITSecret и выводят на экран значение в формате обычного текста этого секрета.</span><span class="sxs-lookup"><span data-stu-id="82dc2-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="82dc2-123">Пример 6: получение всех секретов, которые были удалены, но не очищены для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="82dc2-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="82dc2-124">Эта команда получает все секретные данные, которые были ранее удалены, но не очищены, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="82dc2-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="82dc2-125">Пример 7: возвращает секретный ITSecret, который был удален, но не очищен для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="82dc2-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="82dc2-126">Эта команда получает секретный ITSecret, который ранее был удален, но не очищен, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="82dc2-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="82dc2-127">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного секрета.</span><span class="sxs-lookup"><span data-stu-id="82dc2-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="82dc2-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82dc2-128">PARAMETERS</span></span>

### <span data-ttu-id="82dc2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82dc2-129">-DefaultProfile</span></span>
<span data-ttu-id="82dc2-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82dc2-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82dc2-131">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="82dc2-131">-IncludeVersions</span></span>
<span data-ttu-id="82dc2-132">Указывает на то, что этот командлет получает все версии секрета.</span><span class="sxs-lookup"><span data-stu-id="82dc2-132">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="82dc2-133">Текущая версия секрета является первой в списке.</span><span class="sxs-lookup"><span data-stu-id="82dc2-133">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="82dc2-134">Если указан этот параметр, необходимо также указать параметры *Name* и *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="82dc2-134">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="82dc2-135">Если параметр *IncludeVersions* не указан, этот командлет получает текущую версию секрета с указанным *именем*.</span><span class="sxs-lookup"><span data-stu-id="82dc2-135">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82dc2-136">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="82dc2-136">-InRemovedState</span></span>
<span data-ttu-id="82dc2-137">Указывает, нужно ли отображать ранее удаленные секреты в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="82dc2-137">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82dc2-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82dc2-138">-Name</span></span>
<span data-ttu-id="82dc2-139">Указывает имя секрета для получения.</span><span class="sxs-lookup"><span data-stu-id="82dc2-139">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82dc2-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="82dc2-140">-VaultName</span></span>
<span data-ttu-id="82dc2-141">Указывает имя хранилища ключей, к которому относится секрет.</span><span class="sxs-lookup"><span data-stu-id="82dc2-141">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="82dc2-142">Этот командлет создает полное доменное имя (FQDN) хранилища ключей, основываясь на имени, которое указывает этот параметр, и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="82dc2-142">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82dc2-143">-Version</span><span class="sxs-lookup"><span data-stu-id="82dc2-143">-Version</span></span>
<span data-ttu-id="82dc2-144">Указывает секретную версию.</span><span class="sxs-lookup"><span data-stu-id="82dc2-144">Specifies the secret version.</span></span>
<span data-ttu-id="82dc2-145">Этот командлет создает полное доменное имя секрета на основе имени хранилища ключей, текущей выбранной среды, имени секрета и секретной версии.</span><span class="sxs-lookup"><span data-stu-id="82dc2-145">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82dc2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82dc2-146">CommonParameters</span></span>
<span data-ttu-id="82dc2-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82dc2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82dc2-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82dc2-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82dc2-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82dc2-149">INPUTS</span></span>

### <span data-ttu-id="82dc2-150">Подстрок</span><span class="sxs-lookup"><span data-stu-id="82dc2-150">String</span></span>

## <span data-ttu-id="82dc2-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82dc2-151">OUTPUTS</span></span>

### <span data-ttu-id="82dc2-152">List<Microsoft. Azure. Commands. KeyVault. Models. SecretIdentityItem>, Microsoft. Azure.,. KeyVault. Models. Secret, List<Microsoft. Azure. Commands. KeyVault>. Models. DeletedSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="82dc2-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="82dc2-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="82dc2-153">NOTES</span></span>

## <span data-ttu-id="82dc2-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82dc2-154">RELATED LINKS</span></span>

[<span data-ttu-id="82dc2-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="82dc2-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="82dc2-156">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="82dc2-156">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="82dc2-157">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="82dc2-157">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

