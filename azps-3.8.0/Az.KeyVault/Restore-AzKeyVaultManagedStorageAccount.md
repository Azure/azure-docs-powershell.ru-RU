---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 4750561aed6643c17fed6e42d13551be76635d72
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066101"
---
# <span data-ttu-id="8dc03-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8dc03-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8dc03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dc03-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc03-103">Восстанавливает управляемую учетную запись хранения в хранилище ключей из файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="8dc03-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="8dc03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dc03-104">SYNTAX</span></span>

### <span data-ttu-id="8dc03-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dc03-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc03-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8dc03-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc03-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc03-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc03-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dc03-108">DESCRIPTION</span></span>
<span data-ttu-id="8dc03-109">Командлет **RESTORE-AzKeyVaultManagedStorageAccount** создает управляемую учетную запись хранения в указанном хранилище ключей из файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="8dc03-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="8dc03-110">Эта управляемая учетная запись хранилища — это реплика архивированной управляемой учетной записи хранения в файле ввода и имеет то же имя, что и оригинал.</span><span class="sxs-lookup"><span data-stu-id="8dc03-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="8dc03-111">Если в хранилище ключей уже есть управляемая учетная запись хранения с тем же именем, этот командлет завершает работу с ошибкой вместо того, чтобы перезаписать оригинал.</span><span class="sxs-lookup"><span data-stu-id="8dc03-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="8dc03-112">Хранилище ключей, на которое вы восстанавливаете управляемая учетная запись хранения, может отличаться от хранилища ключей, для которого была задана резервная копия управляемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8dc03-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="8dc03-113">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="8dc03-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="8dc03-114">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="8dc03-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="8dc03-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dc03-115">EXAMPLES</span></span>

### <span data-ttu-id="8dc03-116">Пример 1: восстановление резервной учетной записи с управляемым хранилищем</span><span class="sxs-lookup"><span data-stu-id="8dc03-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Id                  : https://mykeyvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : MyKeyVault
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

<span data-ttu-id="8dc03-117">Эта команда восстанавливает управляемую учетную запись хранения, включая все ее версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей с именем MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="8dc03-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="8dc03-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dc03-118">PARAMETERS</span></span>

### <span data-ttu-id="8dc03-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc03-119">-DefaultProfile</span></span>
<span data-ttu-id="8dc03-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc03-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dc03-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="8dc03-121">-InputFile</span></span>
<span data-ttu-id="8dc03-122">Входной файл.</span><span class="sxs-lookup"><span data-stu-id="8dc03-122">Input file.</span></span>
<span data-ttu-id="8dc03-123">Входной файл, содержащий заархивированный блоб</span><span class="sxs-lookup"><span data-stu-id="8dc03-123">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc03-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dc03-124">-InputObject</span></span>
<span data-ttu-id="8dc03-125">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="8dc03-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc03-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc03-126">-ResourceId</span></span>
<span data-ttu-id="8dc03-127">Идентификатор ресурса KeyVault</span><span class="sxs-lookup"><span data-stu-id="8dc03-127">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc03-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8dc03-128">-VaultName</span></span>
<span data-ttu-id="8dc03-129">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="8dc03-129">Vault name.</span></span>
<span data-ttu-id="8dc03-130">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="8dc03-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc03-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dc03-131">-Confirm</span></span>
<span data-ttu-id="8dc03-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8dc03-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc03-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc03-133">-WhatIf</span></span>
<span data-ttu-id="8dc03-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8dc03-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc03-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8dc03-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc03-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc03-136">CommonParameters</span></span>
<span data-ttu-id="8dc03-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dc03-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc03-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dc03-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc03-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dc03-139">INPUTS</span></span>

### <span data-ttu-id="8dc03-140">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8dc03-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8dc03-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8dc03-141">System.String</span></span>

## <span data-ttu-id="8dc03-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dc03-142">OUTPUTS</span></span>

### <span data-ttu-id="8dc03-143">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8dc03-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8dc03-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dc03-144">NOTES</span></span>

## <span data-ttu-id="8dc03-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dc03-145">RELATED LINKS</span></span>
