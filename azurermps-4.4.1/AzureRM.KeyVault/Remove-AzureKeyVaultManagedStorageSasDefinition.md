---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: fadf6b15eb25f07d88254a5d3a998f1692e5cf29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734054"
---
# <span data-ttu-id="3de8b-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="3de8b-101">Remove-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="3de8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3de8b-102">SYNOPSIS</span></span>
<span data-ttu-id="3de8b-103">Удаляет определения SAS из хранилища ключей для управляемых хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="3de8b-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3de8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3de8b-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3de8b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3de8b-105">DESCRIPTION</span></span>
<span data-ttu-id="3de8b-106">Удаляет определения SAS из хранилища ключей для управляемых хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="3de8b-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="3de8b-107">Кроме того, он удаляет секрет, используемый для получения маркера SAS для этого определения SAS.</span><span class="sxs-lookup"><span data-stu-id="3de8b-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="3de8b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3de8b-108">EXAMPLES</span></span>

### <span data-ttu-id="3de8b-109">Пример 1: Удаление определения SAS хранилища управляемых хранилищ Azure с помощью хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3de8b-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="3de8b-110">Удаляет из хранилища ключей определение SAS "mysasdef", связанного с учетной записью "mystorageaccount" в хранилище "myvault".</span><span class="sxs-lookup"><span data-stu-id="3de8b-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="3de8b-111">Пример 2: Удаление определения управляемого хранилища Azure с хранилищем ключей без подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3de8b-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="3de8b-112">Удаляет из хранилища ключей определение SAS "mysasdef", связанного с учетной записью "mystorageaccount" в хранилище "myvault".</span><span class="sxs-lookup"><span data-stu-id="3de8b-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="3de8b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3de8b-113">PARAMETERS</span></span>

### <span data-ttu-id="3de8b-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="3de8b-114">-AccountName</span></span>
<span data-ttu-id="3de8b-115">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3de8b-115">Storage account name.</span></span>
<span data-ttu-id="3de8b-116">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3de8b-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3de8b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3de8b-117">-Force</span></span>
<span data-ttu-id="3de8b-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="3de8b-118">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3de8b-119">-Name</span></span>
<span data-ttu-id="3de8b-120">Имя определения SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="3de8b-120">Storage sas definition name.</span></span>
<span data-ttu-id="3de8b-121">Командлет создает полное доменное имя определения SAS хранилища из имени хранилища, выбранной среды, имени учетной записи хранения и имени определения SAS.</span><span class="sxs-lookup"><span data-stu-id="3de8b-121">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3de8b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3de8b-122">-PassThru</span></span>
<span data-ttu-id="3de8b-123">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="3de8b-123">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3de8b-124">Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="3de8b-124">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8b-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3de8b-125">-VaultName</span></span>
<span data-ttu-id="3de8b-126">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="3de8b-126">Vault name.</span></span>
<span data-ttu-id="3de8b-127">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="3de8b-127">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3de8b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3de8b-128">-Confirm</span></span>
<span data-ttu-id="3de8b-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3de8b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de8b-130">-WhatIf</span></span>
<span data-ttu-id="3de8b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3de8b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3de8b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3de8b-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de8b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de8b-133">-DefaultProfile</span></span>
<span data-ttu-id="3de8b-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3de8b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3de8b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de8b-135">CommonParameters</span></span>
<span data-ttu-id="3de8b-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3de8b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de8b-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3de8b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de8b-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3de8b-138">INPUTS</span></span>

### <span data-ttu-id="3de8b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3de8b-139">System.String</span></span>

## <span data-ttu-id="3de8b-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3de8b-140">OUTPUTS</span></span>

### <span data-ttu-id="3de8b-141">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="3de8b-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="3de8b-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3de8b-142">NOTES</span></span>

## <span data-ttu-id="3de8b-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3de8b-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

