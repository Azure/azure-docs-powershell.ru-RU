---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 438d36a5c9081da3124c0ef5ee03c7eb9ad8f634
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913336"
---
# <span data-ttu-id="112e8-101">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="112e8-101">Remove-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="112e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="112e8-102">SYNOPSIS</span></span>
<span data-ttu-id="112e8-103">Удаляет управляемую учетную запись хранилища Azure с основным хранилищем и все связанные определения SAS.</span><span class="sxs-lookup"><span data-stu-id="112e8-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="112e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="112e8-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="112e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="112e8-105">DESCRIPTION</span></span>
<span data-ttu-id="112e8-106">Отменяет связь учетной записи хранения Azure из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="112e8-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="112e8-107">Это не приведет к удалению учетной записи хранения Azure, но удаляет ключи учетной записи из управления с помощью Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="112e8-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="112e8-108">Также удаляются все связанные определения SAS хранилища управляемых хранилищ.</span><span class="sxs-lookup"><span data-stu-id="112e8-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="112e8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="112e8-109">EXAMPLES</span></span>

### <span data-ttu-id="112e8-110">Пример 1: Удаление учетной записи хранения для хранилища ключей, управляемой службой хранилища Azure, и всех связанных определений SAS.</span><span class="sxs-lookup"><span data-stu-id="112e8-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="112e8-111">Отменяет связь учетной записи хранилища Azure "mystorageaccount" с основным хранилищем "myvault" и останавливает управление ключами из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="112e8-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="112e8-112">Учетная запись "mystorageaccount" не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="112e8-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="112e8-113">Все определения SAS хранилища с управляемым хранилищем, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="112e8-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="112e8-114">Пример 2: Удаление учетной записи хранения для хранилища ключей в службе управления правами и всех связанных определений SAS без подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="112e8-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="112e8-115">Отменяет связь учетной записи хранилища Azure "mystorageaccount" с основным хранилищем "myvault" и останавливает управление ключами из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="112e8-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="112e8-116">Учетная запись "mystorageaccount" не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="112e8-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="112e8-117">Все определения SAS хранилища с управляемым хранилищем, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="112e8-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="112e8-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="112e8-118">PARAMETERS</span></span>

### <span data-ttu-id="112e8-119">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="112e8-119">-AccountName</span></span>
<span data-ttu-id="112e8-120">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="112e8-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="112e8-121">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="112e8-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="112e8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112e8-122">-DefaultProfile</span></span>
<span data-ttu-id="112e8-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="112e8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="112e8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="112e8-124">-Force</span></span>
<span data-ttu-id="112e8-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="112e8-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="112e8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="112e8-126">-PassThru</span></span>
<span data-ttu-id="112e8-127">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="112e8-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="112e8-128">Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="112e8-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="112e8-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="112e8-129">-VaultName</span></span>
<span data-ttu-id="112e8-130">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="112e8-130">Vault name.</span></span>
<span data-ttu-id="112e8-131">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="112e8-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="112e8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="112e8-132">-Confirm</span></span>
<span data-ttu-id="112e8-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="112e8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="112e8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="112e8-134">-WhatIf</span></span>
<span data-ttu-id="112e8-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="112e8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="112e8-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="112e8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="112e8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112e8-137">CommonParameters</span></span>
<span data-ttu-id="112e8-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="112e8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112e8-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="112e8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112e8-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="112e8-140">INPUTS</span></span>

### <span data-ttu-id="112e8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="112e8-141">System.String</span></span>

## <span data-ttu-id="112e8-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="112e8-142">OUTPUTS</span></span>

### <span data-ttu-id="112e8-143">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="112e8-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="112e8-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="112e8-144">NOTES</span></span>

## <span data-ttu-id="112e8-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="112e8-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

