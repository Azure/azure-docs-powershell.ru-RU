---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: d57f672ef440515e69535503f006e08b4c924646
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910277"
---
# <span data-ttu-id="de7b0-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="de7b0-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="de7b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de7b0-102">SYNOPSIS</span></span>
<span data-ttu-id="de7b0-103">Удаляет управляемую учетную запись хранилища Azure с основным хранилищем и все связанные определения SAS.</span><span class="sxs-lookup"><span data-stu-id="de7b0-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="de7b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de7b0-104">SYNTAX</span></span>

```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de7b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de7b0-105">DESCRIPTION</span></span>
<span data-ttu-id="de7b0-106">Отменяет связь учетной записи хранения Azure из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="de7b0-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="de7b0-107">Это не приведет к удалению учетной записи хранения Azure, но удаляет ключи учетной записи из управления с помощью Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="de7b0-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="de7b0-108">Также удаляются все связанные определения SAS хранилища управляемых хранилищ.</span><span class="sxs-lookup"><span data-stu-id="de7b0-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="de7b0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de7b0-109">EXAMPLES</span></span>

### <span data-ttu-id="de7b0-110">Пример 1: Удаление учетной записи хранения для хранилища ключей, управляемой службой хранилища Azure, и всех связанных определений SAS.</span><span class="sxs-lookup"><span data-stu-id="de7b0-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="de7b0-111">Отменяет связь учетной записи хранилища Azure "mystorageaccount" с основным хранилищем "myvault" и останавливает управление ключами из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="de7b0-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="de7b0-112">Учетная запись "mystorageaccount" не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="de7b0-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="de7b0-113">Все определения SAS хранилища с управляемым хранилищем, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="de7b0-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="de7b0-114">Пример 2: Удаление учетной записи хранения для хранилища ключей в службе управления правами и всех связанных определений SAS без подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="de7b0-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="de7b0-115">Отменяет связь учетной записи хранилища Azure "mystorageaccount" с основным хранилищем "myvault" и останавливает управление ключами из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="de7b0-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="de7b0-116">Учетная запись "mystorageaccount" не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="de7b0-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="de7b0-117">Все определения SAS хранилища с управляемым хранилищем, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="de7b0-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="de7b0-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de7b0-118">PARAMETERS</span></span>

### <span data-ttu-id="de7b0-119">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="de7b0-119">-AccountName</span></span>
<span data-ttu-id="de7b0-120">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="de7b0-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="de7b0-121">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="de7b0-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de7b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de7b0-122">-DefaultProfile</span></span>
<span data-ttu-id="de7b0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="de7b0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de7b0-124">-Force</span><span class="sxs-lookup"><span data-stu-id="de7b0-124">-Force</span></span>
<span data-ttu-id="de7b0-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="de7b0-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="de7b0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de7b0-126">-PassThru</span></span>
<span data-ttu-id="de7b0-127">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="de7b0-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="de7b0-128">Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="de7b0-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="de7b0-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="de7b0-129">-VaultName</span></span>
<span data-ttu-id="de7b0-130">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="de7b0-130">Vault name.</span></span>
<span data-ttu-id="de7b0-131">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="de7b0-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="de7b0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de7b0-132">-Confirm</span></span>
<span data-ttu-id="de7b0-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="de7b0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de7b0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de7b0-134">-WhatIf</span></span>
<span data-ttu-id="de7b0-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="de7b0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de7b0-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de7b0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de7b0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de7b0-137">CommonParameters</span></span>
<span data-ttu-id="de7b0-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de7b0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de7b0-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de7b0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de7b0-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de7b0-140">INPUTS</span></span>

### <span data-ttu-id="de7b0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="de7b0-141">System.String</span></span>

## <span data-ttu-id="de7b0-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de7b0-142">OUTPUTS</span></span>

### <span data-ttu-id="de7b0-143">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="de7b0-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="de7b0-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="de7b0-144">NOTES</span></span>

## <span data-ttu-id="de7b0-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de7b0-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

