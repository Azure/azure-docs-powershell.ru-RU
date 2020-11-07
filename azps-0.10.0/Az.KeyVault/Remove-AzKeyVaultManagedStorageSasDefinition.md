---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 98c4cca6b2de508ca48da4ccbc5cf9f9a31eaa0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910276"
---
# <span data-ttu-id="203de-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="203de-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="203de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="203de-102">SYNOPSIS</span></span>
<span data-ttu-id="203de-103">Удаляет определения SAS из хранилища ключей для управляемых хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="203de-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="203de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="203de-104">SYNTAX</span></span>

```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="203de-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="203de-105">DESCRIPTION</span></span>
<span data-ttu-id="203de-106">Удаляет определения SAS из хранилища ключей для управляемых хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="203de-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="203de-107">Кроме того, он удаляет секрет, используемый для получения маркера SAS для этого определения SAS.</span><span class="sxs-lookup"><span data-stu-id="203de-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="203de-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="203de-108">EXAMPLES</span></span>

### <span data-ttu-id="203de-109">Пример 1: Удаление определения SAS хранилища управляемых хранилищ Azure с помощью хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="203de-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="203de-110">Удаляет из хранилища ключей определение SAS "mysasdef", связанного с учетной записью "mystorageaccount" в хранилище "myvault".</span><span class="sxs-lookup"><span data-stu-id="203de-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="203de-111">Пример 2: Удаление определения управляемого хранилища Azure с хранилищем ключей без подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="203de-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="203de-112">Удаляет из хранилища ключей определение SAS "mysasdef", связанного с учетной записью "mystorageaccount" в хранилище "myvault".</span><span class="sxs-lookup"><span data-stu-id="203de-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="203de-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="203de-113">PARAMETERS</span></span>

### <span data-ttu-id="203de-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="203de-114">-AccountName</span></span>
<span data-ttu-id="203de-115">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="203de-115">Storage account name.</span></span>
<span data-ttu-id="203de-116">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="203de-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="203de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203de-117">-DefaultProfile</span></span>
<span data-ttu-id="203de-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="203de-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="203de-119">-Force</span><span class="sxs-lookup"><span data-stu-id="203de-119">-Force</span></span>
<span data-ttu-id="203de-120">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="203de-120">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="203de-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="203de-121">-Name</span></span>
<span data-ttu-id="203de-122">Имя определения SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="203de-122">Storage sas definition name.</span></span>
<span data-ttu-id="203de-123">Командлет создает полное доменное имя определения SAS хранилища из имени хранилища, выбранной среды, имени учетной записи хранения и имени определения SAS.</span><span class="sxs-lookup"><span data-stu-id="203de-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="203de-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="203de-124">-PassThru</span></span>
<span data-ttu-id="203de-125">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="203de-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="203de-126">Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="203de-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="203de-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="203de-127">-VaultName</span></span>
<span data-ttu-id="203de-128">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="203de-128">Vault name.</span></span>
<span data-ttu-id="203de-129">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="203de-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="203de-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="203de-130">-Confirm</span></span>
<span data-ttu-id="203de-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="203de-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="203de-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="203de-132">-WhatIf</span></span>
<span data-ttu-id="203de-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="203de-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="203de-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="203de-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="203de-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203de-135">CommonParameters</span></span>
<span data-ttu-id="203de-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="203de-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203de-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="203de-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203de-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="203de-138">INPUTS</span></span>

### <span data-ttu-id="203de-139">System. String</span><span class="sxs-lookup"><span data-stu-id="203de-139">System.String</span></span>

## <span data-ttu-id="203de-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="203de-140">OUTPUTS</span></span>

### <span data-ttu-id="203de-141">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="203de-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="203de-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="203de-142">NOTES</span></span>

## <span data-ttu-id="203de-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="203de-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

