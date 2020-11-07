---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 2117dee69ee21b4a6061de93e2106a70137070c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734056"
---
# <span data-ttu-id="9bd71-101">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9bd71-101">Remove-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="9bd71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bd71-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd71-103">Удаляет управляемую учетную запись хранилища Azure с основным хранилищем и все связанные определения SAS.</span><span class="sxs-lookup"><span data-stu-id="9bd71-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bd71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bd71-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bd71-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bd71-105">DESCRIPTION</span></span>
<span data-ttu-id="9bd71-106">Отменяет связь учетной записи хранения Azure из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="9bd71-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="9bd71-107">Это не приведет к удалению учетной записи хранения Azure, но удаляет ключи учетной записи из управления с помощью Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9bd71-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="9bd71-108">Также удаляются все связанные определения SAS хранилища управляемых хранилищ.</span><span class="sxs-lookup"><span data-stu-id="9bd71-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="9bd71-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bd71-109">EXAMPLES</span></span>

### <span data-ttu-id="9bd71-110">Пример 1: Удаление учетной записи хранения для хранилища ключей, управляемой службой хранилища Azure, и всех связанных определений SAS.</span><span class="sxs-lookup"><span data-stu-id="9bd71-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="9bd71-111">Отменяет связь учетной записи хранилища Azure "mystorageaccount" с основным хранилищем "myvault" и останавливает управление ключами из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="9bd71-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="9bd71-112">Учетная запись "mystorageaccount" не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="9bd71-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="9bd71-113">Все определения SAS хранилища с управляемым хранилищем, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="9bd71-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="9bd71-114">Пример 2: Удаление учетной записи хранения для хранилища ключей в службе управления правами и всех связанных определений SAS без подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9bd71-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="9bd71-115">Отменяет связь учетной записи хранилища Azure "mystorageaccount" с основным хранилищем "myvault" и останавливает управление ключами из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="9bd71-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="9bd71-116">Учетная запись "mystorageaccount" не будет удалена.</span><span class="sxs-lookup"><span data-stu-id="9bd71-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="9bd71-117">Все определения SAS хранилища с управляемым хранилищем, связанные с этой учетной записью, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="9bd71-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="9bd71-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bd71-118">PARAMETERS</span></span>

### <span data-ttu-id="9bd71-119">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="9bd71-119">-AccountName</span></span>
<span data-ttu-id="9bd71-120">Имя учетной записи хранилища с управляемым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="9bd71-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="9bd71-121">Командлет создает полное доменное имя управляемой учетной записи хранения из имени хранилища, выбранной в данный момент среды и управляемого имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9bd71-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bd71-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9bd71-122">-Force</span></span>
<span data-ttu-id="9bd71-123">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9bd71-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9bd71-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bd71-124">-PassThru</span></span>
<span data-ttu-id="9bd71-125">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="9bd71-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9bd71-126">Если этот параметр указан, командлет возвращает управляемую учетную запись хранения, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="9bd71-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="9bd71-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9bd71-127">-VaultName</span></span>
<span data-ttu-id="9bd71-128">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="9bd71-128">Vault name.</span></span>
<span data-ttu-id="9bd71-129">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="9bd71-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9bd71-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bd71-130">-Confirm</span></span>
<span data-ttu-id="9bd71-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9bd71-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bd71-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd71-132">-WhatIf</span></span>
<span data-ttu-id="9bd71-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9bd71-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bd71-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9bd71-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bd71-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd71-135">-DefaultProfile</span></span>
<span data-ttu-id="9bd71-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd71-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bd71-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd71-137">CommonParameters</span></span>
<span data-ttu-id="9bd71-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bd71-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd71-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd71-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd71-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bd71-140">INPUTS</span></span>

### <span data-ttu-id="9bd71-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9bd71-141">System.String</span></span>

## <span data-ttu-id="9bd71-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bd71-142">OUTPUTS</span></span>

### <span data-ttu-id="9bd71-143">Microsoft. Azure. Commands. KeyVault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9bd71-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="9bd71-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bd71-144">NOTES</span></span>

## <span data-ttu-id="9bd71-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bd71-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

