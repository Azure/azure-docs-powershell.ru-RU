---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: eaddfaa6be725d588c8856031a34e1bdefcc3892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566995"
---
# <span data-ttu-id="a1ff1-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a1ff1-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="a1ff1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ff1-103">Получает ключи хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1ff1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1ff1-104">SYNTAX</span></span>

### <span data-ttu-id="a1ff1-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1ff1-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ff1-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="a1ff1-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ff1-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="a1ff1-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ff1-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="a1ff1-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ff1-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="a1ff1-109">ByInputObjectKeyName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ff1-110">ByKInputObjecteyVersions</span><span class="sxs-lookup"><span data-stu-id="a1ff1-110">ByKInputObjecteyVersions</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1ff1-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1ff1-111">DESCRIPTION</span></span>
<span data-ttu-id="a1ff1-112">Командлет **Get-AzureKeyVaultKey** получает ключи Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-112">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="a1ff1-113">Этот командлет получает определенный **Microsoft. Azure. Commands. KeyVault. Models. KeyBundle** или список всех объектов **KeyBundle** в хранилище ключей или по версии.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-113">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="a1ff1-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1ff1-114">EXAMPLES</span></span>

### <span data-ttu-id="a1ff1-115">Пример 1: получение всех ключей в хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="a1ff1-115">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="a1ff1-116">Эта команда получает все ключи из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-116">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="a1ff1-117">Пример 2: получение текущей версии ключа</span><span class="sxs-lookup"><span data-stu-id="a1ff1-117">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="a1ff1-118">Эта команда получает текущую версию ключа с именем ITPfx в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-118">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="a1ff1-119">Пример 3: получение всех версий ключа</span><span class="sxs-lookup"><span data-stu-id="a1ff1-119">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="a1ff1-120">Эта команда возвращает все версии Key с именем ITPfx в разделе Key vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-120">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="a1ff1-121">Пример 4: получение определенной версии ключа</span><span class="sxs-lookup"><span data-stu-id="a1ff1-121">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="a1ff1-122">Эта команда возвращает определенную версию ключа с именем ITPfx в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-122">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="a1ff1-123">После выполнения этой команды вы можете просматривать различные свойства ключа, перемещаясь по объекту $Key.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-123">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="a1ff1-124">Пример 5: получение всех ключей, которые были удалены, но не очищены для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-124">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="a1ff1-125">Эта команда возвращает все разделы, которые были ранее удалены, но не очищены, в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-125">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="a1ff1-126">Пример 6: получение ключа ITPfx, который был удален, но не очищен для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-126">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="a1ff1-127">Эта команда возвращает клавишу ITPfx, которая была ранее удалена, но не очищена, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-127">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="a1ff1-128">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного ключа.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-128">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="a1ff1-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1ff1-129">PARAMETERS</span></span>

### <span data-ttu-id="a1ff1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ff1-130">-DefaultProfile</span></span>
<span data-ttu-id="a1ff1-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a1ff1-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1ff1-132">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="a1ff1-132">-IncludeVersions</span></span>
<span data-ttu-id="a1ff1-133">Указывает на то, что этот командлет получает все версии ключа.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-133">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="a1ff1-134">Текущая версия ключа является первой в списке.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-134">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="a1ff1-135">Если указан этот параметр, необходимо также указать параметры *Name* и *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="a1ff1-135">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="a1ff1-136">Если параметр *IncludeVersions* не указан, этот командлет получает текущую версию ключа с указанным *именем*.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-136">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions, ByKInputObjecteyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1ff1-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1ff1-137">-InputObject</span></span>
<span data-ttu-id="a1ff1-138">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-138">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1ff1-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a1ff1-139">-InRemovedState</span></span>
<span data-ttu-id="a1ff1-140">Указывает, нужно ли отображать ранее удаленные разделы в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-140">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1ff1-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1ff1-141">-Name</span></span>
<span data-ttu-id="a1ff1-142">Указывает имя набора ключей, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-142">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1ff1-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a1ff1-143">-VaultName</span></span>
<span data-ttu-id="a1ff1-144">Указывает имя хранилища ключей, из которого этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-144">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="a1ff1-145">Этот командлет создает полное доменное имя (FQDN) для хранилища ключей, основываясь на имени, указанном этим параметром, и в выбранной среде.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-145">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1ff1-146">-Version</span><span class="sxs-lookup"><span data-stu-id="a1ff1-146">-Version</span></span>
<span data-ttu-id="a1ff1-147">Указывает версию ключа.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-147">Specifies the key version.</span></span>
<span data-ttu-id="a1ff1-148">Этот командлет создает полное доменное имя ключа на основе имени хранилища ключей, текущей выбранной среды, имени ключа и версии ключа.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-148">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByInputObjectKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1ff1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ff1-149">CommonParameters</span></span>
<span data-ttu-id="a1ff1-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1ff1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ff1-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1ff1-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ff1-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1ff1-152">INPUTS</span></span>

### <span data-ttu-id="a1ff1-153">Подстрок</span><span class="sxs-lookup"><span data-stu-id="a1ff1-153">String</span></span>

## <span data-ttu-id="a1ff1-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1ff1-154">OUTPUTS</span></span>

### <span data-ttu-id="a1ff1-155">List<Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem>, Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a1ff1-155">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="a1ff1-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1ff1-156">NOTES</span></span>

## <span data-ttu-id="a1ff1-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1ff1-157">RELATED LINKS</span></span>

[<span data-ttu-id="a1ff1-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a1ff1-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="a1ff1-159">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a1ff1-159">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="a1ff1-160">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="a1ff1-160">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="a1ff1-161">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="a1ff1-161">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

