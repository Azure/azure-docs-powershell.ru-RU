---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 153165406fd02561dbece79e18558065ff34c8f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973267"
---
# <span data-ttu-id="39250-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="39250-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="39250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39250-102">SYNOPSIS</span></span>
<span data-ttu-id="39250-103">Измените область шифрования для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="39250-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="39250-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39250-104">SYNTAX</span></span>

### <span data-ttu-id="39250-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39250-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39250-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="39250-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39250-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="39250-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39250-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="39250-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39250-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="39250-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39250-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="39250-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39250-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39250-111">DESCRIPTION</span></span>
<span data-ttu-id="39250-112">**Cmdlet Update-AzStorageEncryptionScope** изменяет область шифрования для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="39250-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="39250-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39250-113">EXAMPLES</span></span>

### <span data-ttu-id="39250-114">Пример 1. Отключение области шифрования</span><span class="sxs-lookup"><span data-stu-id="39250-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="39250-115">Эта команда отключает область шифрования.</span><span class="sxs-lookup"><span data-stu-id="39250-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="39250-116">Пример 2. Включить область шифрования</span><span class="sxs-lookup"><span data-stu-id="39250-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                                                           
----      -----    ------            -------------- -------------------------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="39250-117">Эта команда включает область шифрования.</span><span class="sxs-lookup"><span data-stu-id="39250-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="39250-118">Пример 3. Обновление области шифрования с использованием шифрования хранилища</span><span class="sxs-lookup"><span data-stu-id="39250-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                          
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="39250-119">Эта команда обновляет область шифрования с использованием шифрования хранилища.</span><span class="sxs-lookup"><span data-stu-id="39250-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="39250-120">Пример 4. Обновление области шифрования с использованием шифрования Keyvault</span><span class="sxs-lookup"><span data-stu-id="39250-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                                                          RequireInfrastructureEncryption 
----      -----    ------             --------------                                                                          -------------------------------
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57   
```

<span data-ttu-id="39250-121">Эта команда updtaes an encryption scope to use Keyvault Encryption.</span><span class="sxs-lookup"><span data-stu-id="39250-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="39250-122">Удостоверение учетной записи хранения должен иметь разрешения на доступ к клавише keyvault, переносы, а также разрешение на перенос.</span><span class="sxs-lookup"><span data-stu-id="39250-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="39250-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39250-123">PARAMETERS</span></span>

### <span data-ttu-id="39250-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39250-124">-DefaultProfile</span></span>
<span data-ttu-id="39250-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39250-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39250-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="39250-126">-EncryptionScopeName</span></span>
<span data-ttu-id="39250-127">Имя службы шифрования хранилищ Azure</span><span class="sxs-lookup"><span data-stu-id="39250-127">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault, AccountObject, AccountObjectKeyVault
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39250-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39250-128">-InputObject</span></span>
<span data-ttu-id="39250-129">Объект EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="39250-129">EncryptionScope object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope
Parameter Sets: EncryptionScopeObject, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39250-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="39250-130">-KeyUri</span></span>
<span data-ttu-id="39250-131">Ключевой URI</span><span class="sxs-lookup"><span data-stu-id="39250-131">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39250-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="39250-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="39250-133">Создание области шифрования с помощью keySource в качестве Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="39250-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39250-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39250-134">-ResourceGroupName</span></span>
<span data-ttu-id="39250-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39250-135">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39250-136">-State</span><span class="sxs-lookup"><span data-stu-id="39250-136">-State</span></span>
<span data-ttu-id="39250-137">Состояние области обновления, возможные значения: "Enabled", "Disabled".</span><span class="sxs-lookup"><span data-stu-id="39250-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39250-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="39250-138">-StorageAccount</span></span>
<span data-ttu-id="39250-139">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="39250-139">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39250-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="39250-140">-StorageAccountName</span></span>
<span data-ttu-id="39250-141">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="39250-141">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39250-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="39250-142">-StorageEncryption</span></span>
<span data-ttu-id="39250-143">Создайте область шифрования с помощью keySource в качестве Microsoft.Storage.</span><span class="sxs-lookup"><span data-stu-id="39250-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject, EncryptionScopeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39250-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39250-144">-Confirm</span></span>
<span data-ttu-id="39250-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39250-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39250-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39250-146">-WhatIf</span></span>
<span data-ttu-id="39250-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39250-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39250-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="39250-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39250-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39250-149">CommonParameters</span></span>
<span data-ttu-id="39250-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39250-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39250-151">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39250-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39250-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39250-152">INPUTS</span></span>

### <span data-ttu-id="39250-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39250-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="39250-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39250-154">OUTPUTS</span></span>

### <span data-ttu-id="39250-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="39250-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="39250-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39250-156">NOTES</span></span>

## <span data-ttu-id="39250-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39250-157">RELATED LINKS</span></span>
