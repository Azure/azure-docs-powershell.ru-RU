---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: 011bdd96d69ae73ca62145b85f6e636751f8eb9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224924"
---
# <span data-ttu-id="41031-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="41031-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="41031-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41031-102">SYNOPSIS</span></span>
<span data-ttu-id="41031-103">Создает область шифрования для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="41031-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="41031-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="41031-104">SYNTAX</span></span>

### <span data-ttu-id="41031-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41031-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41031-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="41031-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41031-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="41031-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41031-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="41031-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41031-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41031-109">DESCRIPTION</span></span>
<span data-ttu-id="41031-110">Для учетной записи хранения создается область шифрования **New-AzStorageEncryptionScope.**</span><span class="sxs-lookup"><span data-stu-id="41031-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="41031-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="41031-111">EXAMPLES</span></span>

### <span data-ttu-id="41031-112">Пример 1. Создание области шифрования с помощью шифрования хранилища</span><span class="sxs-lookup"><span data-stu-id="41031-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="41031-113">Эта команда создает область шифрования с помощью шифрования хранилища.</span><span class="sxs-lookup"><span data-stu-id="41031-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="41031-114">Пример 2. Создание области шифрования с помощью шифрования Keyvault</span><span class="sxs-lookup"><span data-stu-id="41031-114">Example 2: Create an encryption scope with Keyvault Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="41031-115">Эта команда создает область шифрования с помощью шифрования Keyvault.</span><span class="sxs-lookup"><span data-stu-id="41031-115">This command creates an encryption scope with Keyvault Encryption.</span></span>
<span data-ttu-id="41031-116">Удостоверение учетной записи хранения должен иметь разрешения на доступ к клавише keyvault, переносы, а также разрешение на перенос.</span><span class="sxs-lookup"><span data-stu-id="41031-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="41031-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41031-117">PARAMETERS</span></span>

### <span data-ttu-id="41031-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41031-118">-DefaultProfile</span></span>
<span data-ttu-id="41031-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41031-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41031-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="41031-120">-EncryptionScopeName</span></span>
<span data-ttu-id="41031-121">Имя службы шифрования хранилищ Azure</span><span class="sxs-lookup"><span data-stu-id="41031-121">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="41031-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="41031-122">-KeyUri</span></span>
<span data-ttu-id="41031-123">Ключевой URI</span><span class="sxs-lookup"><span data-stu-id="41031-123">The key Uri</span></span>

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

### <span data-ttu-id="41031-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="41031-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="41031-125">Создание области шифрования с помощью keySource в качестве Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="41031-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="41031-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41031-126">-ResourceGroupName</span></span>
<span data-ttu-id="41031-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41031-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="41031-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="41031-128">-StorageAccount</span></span>
<span data-ttu-id="41031-129">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="41031-129">Storage account object</span></span>

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

### <span data-ttu-id="41031-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="41031-130">-StorageAccountName</span></span>
<span data-ttu-id="41031-131">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="41031-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="41031-132">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="41031-132">-StorageEncryption</span></span>
<span data-ttu-id="41031-133">Создайте область шифрования с помощью keySource в качестве Microsoft.Storage.</span><span class="sxs-lookup"><span data-stu-id="41031-133">Create encryption scope with keySource as Microsoft.Storage.</span></span>

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

### <span data-ttu-id="41031-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41031-134">-Confirm</span></span>
<span data-ttu-id="41031-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="41031-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41031-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41031-136">-WhatIf</span></span>
<span data-ttu-id="41031-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41031-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41031-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="41031-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41031-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41031-139">CommonParameters</span></span>
<span data-ttu-id="41031-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41031-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41031-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41031-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41031-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41031-142">INPUTS</span></span>

### <span data-ttu-id="41031-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41031-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="41031-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41031-144">OUTPUTS</span></span>

### <span data-ttu-id="41031-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="41031-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="41031-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="41031-146">NOTES</span></span>

## <span data-ttu-id="41031-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41031-147">RELATED LINKS</span></span>
