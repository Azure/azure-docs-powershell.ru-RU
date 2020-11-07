---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a0d79aa0d1699f6e6645f86475732c235447342f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910296"
---
# <span data-ttu-id="edbc2-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="edbc2-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="edbc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="edbc2-102">SYNOPSIS</span></span>
<span data-ttu-id="edbc2-103">Получает ключи хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="edbc2-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="edbc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="edbc2-104">SYNTAX</span></span>

### <span data-ttu-id="edbc2-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="edbc2-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edbc2-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="edbc2-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edbc2-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="edbc2-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edbc2-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="edbc2-108">ByDeletedKey</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edbc2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edbc2-109">DESCRIPTION</span></span>
<span data-ttu-id="edbc2-110">Командлет **Get-AzKeyVaultKey** получает ключи Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="edbc2-110">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="edbc2-111">Этот командлет получает определенный **Microsoft. Azure. Commands. KeyVault. Models. KeyBundle** или список всех объектов **KeyBundle** в хранилище ключей или по версии.</span><span class="sxs-lookup"><span data-stu-id="edbc2-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="edbc2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="edbc2-112">EXAMPLES</span></span>

### <span data-ttu-id="edbc2-113">Пример 1: получение всех ключей в хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="edbc2-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="edbc2-114">Эта команда получает все ключи из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="edbc2-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="edbc2-115">Пример 2: получение текущей версии ключа</span><span class="sxs-lookup"><span data-stu-id="edbc2-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="edbc2-116">Эта команда получает текущую версию ключа с именем ITPfx в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="edbc2-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="edbc2-117">Пример 3: получение всех версий ключа</span><span class="sxs-lookup"><span data-stu-id="edbc2-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="edbc2-118">Эта команда возвращает все версии Key с именем ITPfx в разделе Key vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="edbc2-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="edbc2-119">Пример 4: получение определенной версии ключа</span><span class="sxs-lookup"><span data-stu-id="edbc2-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="edbc2-120">Эта команда возвращает определенную версию ключа с именем ITPfx в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="edbc2-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="edbc2-121">После выполнения этой команды вы можете просматривать различные свойства ключа, перемещаясь по объекту $Key.</span><span class="sxs-lookup"><span data-stu-id="edbc2-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="edbc2-122">Пример 5: получение всех ключей, которые были удалены, но не очищены для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="edbc2-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="edbc2-123">Эта команда возвращает все разделы, которые были ранее удалены, но не очищены, в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="edbc2-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="edbc2-124">Пример 6: получение ключа ITPfx, который был удален, но не очищен для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="edbc2-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="edbc2-125">Эта команда возвращает клавишу ITPfx, которая была ранее удалена, но не очищена, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="edbc2-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="edbc2-126">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного ключа.</span><span class="sxs-lookup"><span data-stu-id="edbc2-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="edbc2-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="edbc2-127">PARAMETERS</span></span>

### <span data-ttu-id="edbc2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edbc2-128">-DefaultProfile</span></span>
<span data-ttu-id="edbc2-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="edbc2-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edbc2-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="edbc2-130">-IncludeVersions</span></span>
<span data-ttu-id="edbc2-131">Указывает на то, что этот командлет получает все версии ключа.</span><span class="sxs-lookup"><span data-stu-id="edbc2-131">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="edbc2-132">Текущая версия ключа является первой в списке.</span><span class="sxs-lookup"><span data-stu-id="edbc2-132">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="edbc2-133">Если указан этот параметр, необходимо также указать параметры *Name* и *VaultName* .</span><span class="sxs-lookup"><span data-stu-id="edbc2-133">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="edbc2-134">Если параметр *IncludeVersions* не указан, этот командлет получает текущую версию ключа с указанным *именем*.</span><span class="sxs-lookup"><span data-stu-id="edbc2-134">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbc2-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="edbc2-135">-InRemovedState</span></span>
<span data-ttu-id="edbc2-136">Указывает, нужно ли отображать ранее удаленные разделы в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="edbc2-136">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbc2-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="edbc2-137">-Name</span></span>
<span data-ttu-id="edbc2-138">Указывает имя набора ключей, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="edbc2-138">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbc2-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="edbc2-139">-VaultName</span></span>
<span data-ttu-id="edbc2-140">Указывает имя хранилища ключей, из которого этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="edbc2-140">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="edbc2-141">Этот командлет создает полное доменное имя (FQDN) для хранилища ключей, основываясь на имени, указанном этим параметром, и в выбранной среде.</span><span class="sxs-lookup"><span data-stu-id="edbc2-141">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="edbc2-142">-Version</span><span class="sxs-lookup"><span data-stu-id="edbc2-142">-Version</span></span>
<span data-ttu-id="edbc2-143">Указывает версию ключа.</span><span class="sxs-lookup"><span data-stu-id="edbc2-143">Specifies the key version.</span></span>
<span data-ttu-id="edbc2-144">Этот командлет создает полное доменное имя ключа на основе имени хранилища ключей, текущей выбранной среды, имени ключа и версии ключа.</span><span class="sxs-lookup"><span data-stu-id="edbc2-144">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbc2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edbc2-145">CommonParameters</span></span>
<span data-ttu-id="edbc2-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="edbc2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edbc2-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edbc2-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edbc2-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="edbc2-148">INPUTS</span></span>

### <span data-ttu-id="edbc2-149">Подстрок</span><span class="sxs-lookup"><span data-stu-id="edbc2-149">String</span></span>

## <span data-ttu-id="edbc2-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="edbc2-150">OUTPUTS</span></span>

### <span data-ttu-id="edbc2-151">List<Microsoft. Azure. Commands. KeyVault. Models. KeyIdentityItem>, Microsoft. Azure. Commands. KeyVault. Models. KeyBundle, List<Microsoft. Azure. Commands. KeyVault>. Models. DeletedKeyIdentityItem, Microsoft. Azure. s. KeyVault. Models. DeletedKeyBundle</span><span class="sxs-lookup"><span data-stu-id="edbc2-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="edbc2-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="edbc2-152">NOTES</span></span>

## <span data-ttu-id="edbc2-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edbc2-153">RELATED LINKS</span></span>

[<span data-ttu-id="edbc2-154">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="edbc2-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="edbc2-155">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="edbc2-155">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="edbc2-156">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="edbc2-156">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="edbc2-157">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="edbc2-157">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

