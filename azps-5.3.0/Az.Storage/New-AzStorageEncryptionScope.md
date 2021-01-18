---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: 011bdd96d69ae73ca62145b85f6e636751f8eb9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505686"
---
# <span data-ttu-id="b1727-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="b1727-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="b1727-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1727-102">SYNOPSIS</span></span>
<span data-ttu-id="b1727-103">Создает область шифрования для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b1727-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="b1727-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1727-104">SYNTAX</span></span>

### <span data-ttu-id="b1727-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1727-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1727-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="b1727-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1727-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b1727-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1727-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="b1727-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1727-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1727-109">DESCRIPTION</span></span>
<span data-ttu-id="b1727-110">Для учетной записи хранения создается область шифрования **New-AzStorageEncryptionScope.**</span><span class="sxs-lookup"><span data-stu-id="b1727-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="b1727-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1727-111">EXAMPLES</span></span>

### <span data-ttu-id="b1727-112">Пример 1. Создание области шифрования с помощью шифрования хранилища</span><span class="sxs-lookup"><span data-stu-id="b1727-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="b1727-113">Эта команда создает область шифрования с помощью шифрования хранилища.</span><span class="sxs-lookup"><span data-stu-id="b1727-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="b1727-114">Пример 2. Создание области шифрования с помощью шифрования Keyvault</span><span class="sxs-lookup"><span data-stu-id="b1727-114">Example 2: Create an encryption scope with Keyvault Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="b1727-115">Эта команда создает область шифрования с помощью шифрования Keyvault.</span><span class="sxs-lookup"><span data-stu-id="b1727-115">This command creates an encryption scope with Keyvault Encryption.</span></span>
<span data-ttu-id="b1727-116">Удостоверение учетной записи хранения должен иметь разрешения на доступ к клавише keyvault, переносы, а также разрешение на перенос.</span><span class="sxs-lookup"><span data-stu-id="b1727-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="b1727-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1727-117">PARAMETERS</span></span>

### <span data-ttu-id="b1727-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1727-118">-DefaultProfile</span></span>
<span data-ttu-id="b1727-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1727-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1727-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="b1727-120">-EncryptionScopeName</span></span>
<span data-ttu-id="b1727-121">Имя службы шифрования хранилищ Azure</span><span class="sxs-lookup"><span data-stu-id="b1727-121">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1727-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="b1727-122">-KeyUri</span></span>
<span data-ttu-id="b1727-123">Ключевой URI</span><span class="sxs-lookup"><span data-stu-id="b1727-123">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1727-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="b1727-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="b1727-125">Создание области шифрования с помощью keySource в качестве Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="b1727-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1727-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1727-126">-ResourceGroupName</span></span>
<span data-ttu-id="b1727-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1727-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b1727-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1727-128">-StorageAccount</span></span>
<span data-ttu-id="b1727-129">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b1727-129">Storage account object</span></span>

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

### <span data-ttu-id="b1727-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b1727-130">-StorageAccountName</span></span>
<span data-ttu-id="b1727-131">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b1727-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="b1727-132">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="b1727-132">-StorageEncryption</span></span>
<span data-ttu-id="b1727-133">Создайте область шифрования с помощью keySource в качестве Microsoft.Storage.</span><span class="sxs-lookup"><span data-stu-id="b1727-133">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1727-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1727-134">-Confirm</span></span>
<span data-ttu-id="b1727-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1727-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1727-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1727-136">-WhatIf</span></span>
<span data-ttu-id="b1727-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1727-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1727-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b1727-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1727-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1727-139">CommonParameters</span></span>
<span data-ttu-id="b1727-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1727-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1727-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1727-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1727-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1727-142">INPUTS</span></span>

### <span data-ttu-id="b1727-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b1727-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="b1727-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1727-144">OUTPUTS</span></span>

### <span data-ttu-id="b1727-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="b1727-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="b1727-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1727-146">NOTES</span></span>

## <span data-ttu-id="b1727-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1727-147">RELATED LINKS</span></span>
