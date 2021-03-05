---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 80ff79e71498cc76479592b65207da09fabed6a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976936"
---
# <span data-ttu-id="e040a-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="e040a-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="e040a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e040a-102">SYNOPSIS</span></span>
<span data-ttu-id="e040a-103">Повторно сгенерирует указанный ключ из key Vault Managed Azure Storage Account.</span><span class="sxs-lookup"><span data-stu-id="e040a-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="e040a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e040a-104">SYNTAX</span></span>

### <span data-ttu-id="e040a-105">ByDefinitionName (Default)</span><span class="sxs-lookup"><span data-stu-id="e040a-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e040a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e040a-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e040a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e040a-107">DESCRIPTION</span></span>
<span data-ttu-id="e040a-108">Повторно создает указанный ключ в управляемой учетной записи хранилища Azure Key Vault и задает его как активный ключ.</span><span class="sxs-lookup"><span data-stu-id="e040a-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="e040a-109">Ключ сейфа передает вызов диспетчеру ресурсов Azure для повторного сгенерации ключа.</span><span class="sxs-lookup"><span data-stu-id="e040a-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="e040a-110">Для повторного получения ключей в учетной записи службы хранилища Azure вызываемой вызываемой службе необходимо получить разрешения.</span><span class="sxs-lookup"><span data-stu-id="e040a-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="e040a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e040a-111">EXAMPLES</span></span>

### <span data-ttu-id="e040a-112">Пример 1. Повторное сгенерировать ключ</span><span class="sxs-lookup"><span data-stu-id="e040a-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="e040a-113">Повторно создает "ключ1" учетной записи "mystorageaccount" и задает "key1" в качестве активной учетной записи хранилища Azure, управляемой key Vault.</span><span class="sxs-lookup"><span data-stu-id="e040a-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="e040a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e040a-114">PARAMETERS</span></span>

### <span data-ttu-id="e040a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e040a-115">-AccountName</span></span>
<span data-ttu-id="e040a-116">Имя учетной записи, управляемой хранилищем Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e040a-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="e040a-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span><span class="sxs-lookup"><span data-stu-id="e040a-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e040a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e040a-118">-DefaultProfile</span></span>
<span data-ttu-id="e040a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e040a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e040a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e040a-120">-Force</span></span>
<span data-ttu-id="e040a-121">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e040a-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e040a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e040a-122">-InputObject</span></span>
<span data-ttu-id="e040a-123">Объект ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="e040a-123">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e040a-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e040a-124">-KeyName</span></span>
<span data-ttu-id="e040a-125">Имя ключа учетной записи хранения, который нужно сгенерировать и активировать.</span><span class="sxs-lookup"><span data-stu-id="e040a-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e040a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e040a-126">-PassThru</span></span>
<span data-ttu-id="e040a-127">По умолчанию cmdlet не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="e040a-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e040a-128">Если этот переключатель задан, возвращается удаленная учетная запись управляемого хранилища.</span><span class="sxs-lookup"><span data-stu-id="e040a-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="e040a-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e040a-129">-VaultName</span></span>
<span data-ttu-id="e040a-130">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="e040a-130">Vault name.</span></span>
<span data-ttu-id="e040a-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="e040a-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e040a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e040a-132">-Confirm</span></span>
<span data-ttu-id="e040a-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e040a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e040a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e040a-134">-WhatIf</span></span>
<span data-ttu-id="e040a-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e040a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e040a-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e040a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e040a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e040a-137">CommonParameters</span></span>
<span data-ttu-id="e040a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e040a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e040a-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e040a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e040a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e040a-140">INPUTS</span></span>

### <span data-ttu-id="e040a-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e040a-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="e040a-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e040a-142">OUTPUTS</span></span>

### <span data-ttu-id="e040a-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e040a-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="e040a-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e040a-144">NOTES</span></span>

## <span data-ttu-id="e040a-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e040a-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

