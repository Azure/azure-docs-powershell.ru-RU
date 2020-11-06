---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://go.microsoft.com/fwlink/?LinkId=690298
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: f6fca9ec6b5f5696cbaa1fb82942e5aa6dfadf80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559787"
---
# <span data-ttu-id="aa61b-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aa61b-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="aa61b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa61b-102">SYNOPSIS</span></span>
<span data-ttu-id="aa61b-103">Возвращает секреты в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="aa61b-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa61b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa61b-104">SYNTAX</span></span>

### <span data-ttu-id="aa61b-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa61b-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa61b-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="aa61b-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa61b-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="aa61b-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa61b-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="aa61b-108">ByDeletedSecrets</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa61b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa61b-109">DESCRIPTION</span></span>
<span data-ttu-id="aa61b-110">Командлет **Get-AzureKeyVaultSecret** получает секреты в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="aa61b-110">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="aa61b-111">Этот командлет получает определенный секрет или все секреты в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="aa61b-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="aa61b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa61b-112">EXAMPLES</span></span>

### <span data-ttu-id="aa61b-113">Пример 1: получение всех текущих версий всех секретных данных в хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="aa61b-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="aa61b-114">Эта команда возвращает текущие версии всех секретных данных в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="aa61b-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="aa61b-115">Пример 2: получение всех версий определенного секрета</span><span class="sxs-lookup"><span data-stu-id="aa61b-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="aa61b-116">Эта команда получает все версии секрета с именем ITSecret в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="aa61b-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="aa61b-117">Пример 3: получение текущей версии определенного секрета</span><span class="sxs-lookup"><span data-stu-id="aa61b-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="aa61b-118">Эта команда получает текущую версию секрета с именем ITSecret в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="aa61b-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="aa61b-119">Пример 4: получение определенной версии определенного секрета</span><span class="sxs-lookup"><span data-stu-id="aa61b-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="aa61b-120">Эта команда возвращает определенную версию секрета с именем ITSecret в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="aa61b-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="aa61b-121">Пример 5: получение простого текстового значения текущей версии определенного секрета</span><span class="sxs-lookup"><span data-stu-id="aa61b-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="aa61b-122">Эти команды получают текущую версию секрета с именем ITSecret и выводят на экран значение в формате обычного текста этого секрета.</span><span class="sxs-lookup"><span data-stu-id="aa61b-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="aa61b-123">Пример 6: получение всех секретов, которые были удалены, но не очищены для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="aa61b-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="aa61b-124">Эта команда получает все секретные данные, которые были ранее удалены, но не очищены, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="aa61b-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="aa61b-125">Пример 7: возвращает секретный ITSecret, который был удален, но не очищен для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="aa61b-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="aa61b-126">Эта команда получает секретный ITSecret, который ранее был удален, но не очищен, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="aa61b-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="aa61b-127">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного секрета.</span><span class="sxs-lookup"><span data-stu-id="aa61b-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="aa61b-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa61b-128">PARAMETERS</span></span>

### <span data-ttu-id="aa61b-129">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="aa61b-129">-IncludeVersions</span></span>
<span data-ttu-id="aa61b-130">Указывает на то, что этот командлет получает все версии секрета.</span><span class="sxs-lookup"><span data-stu-id="aa61b-130">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="aa61b-131">Текущая версия секрета является первой в списке.</span><span class="sxs-lookup"><span data-stu-id="aa61b-131">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="aa61b-132">Если указан этот параметр, необходимо также указать параметры *Name* и *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="aa61b-132">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="aa61b-133">Если параметр *IncludeVersions* не указан, этот командлет получает текущую версию секрета с указанным *именем*.</span><span class="sxs-lookup"><span data-stu-id="aa61b-133">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa61b-134">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="aa61b-134">-InRemovedState</span></span>
<span data-ttu-id="aa61b-135">Указывает, нужно ли отображать ранее удаленные секреты в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="aa61b-135">Specifies whether to show the previously deleted secrets in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa61b-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa61b-136">-Name</span></span>
<span data-ttu-id="aa61b-137">Указывает имя секрета для получения.</span><span class="sxs-lookup"><span data-stu-id="aa61b-137">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa61b-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="aa61b-138">-VaultName</span></span>
<span data-ttu-id="aa61b-139">Указывает имя хранилища ключей, к которому относится секрет.</span><span class="sxs-lookup"><span data-stu-id="aa61b-139">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="aa61b-140">Этот командлет создает полное доменное имя (FQDN) хранилища ключей, основываясь на имени, которое указывает этот параметр, и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="aa61b-140">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="aa61b-141">-Version</span><span class="sxs-lookup"><span data-stu-id="aa61b-141">-Version</span></span>
<span data-ttu-id="aa61b-142">Указывает секретную версию.</span><span class="sxs-lookup"><span data-stu-id="aa61b-142">Specifies the secret version.</span></span>
<span data-ttu-id="aa61b-143">Этот командлет создает полное доменное имя секрета на основе имени хранилища ключей, текущей выбранной среды, имени секрета и секретной версии.</span><span class="sxs-lookup"><span data-stu-id="aa61b-143">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa61b-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa61b-144">-DefaultProfile</span></span>
<span data-ttu-id="aa61b-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa61b-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa61b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa61b-146">CommonParameters</span></span>
<span data-ttu-id="aa61b-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa61b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa61b-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa61b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa61b-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa61b-149">INPUTS</span></span>

### <span data-ttu-id="aa61b-150">Подстрок</span><span class="sxs-lookup"><span data-stu-id="aa61b-150">String</span></span>

## <span data-ttu-id="aa61b-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa61b-151">OUTPUTS</span></span>

### <span data-ttu-id="aa61b-152">List<Microsoft. Azure. Commands. KeyVault. Models. SecretIdentityItem>, Microsoft. Azure.,. KeyVault. Models. Secret, List<Microsoft. Azure. Commands. KeyVault>. Models. DeletedSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="aa61b-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="aa61b-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa61b-153">NOTES</span></span>

## <span data-ttu-id="aa61b-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa61b-154">RELATED LINKS</span></span>

[<span data-ttu-id="aa61b-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aa61b-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="aa61b-156">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="aa61b-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="aa61b-157">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aa61b-157">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

