---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 12e1844be497baa24a3b9b4aa9c4e5690564f4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560159"
---
# <span data-ttu-id="ae76c-101">Restore-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae76c-101">Restore-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ae76c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae76c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae76c-103">Восстанавливает управляемую учетную запись хранения в хранилище ключей из файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="ae76c-103">Restores a managed storage account in a key vault from a backup file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae76c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae76c-104">SYNTAX</span></span>

### <span data-ttu-id="ae76c-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae76c-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae76c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ae76c-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae76c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae76c-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae76c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae76c-108">DESCRIPTION</span></span>
<span data-ttu-id="ae76c-109">Командлет **RESTORE-AzureKeyVaultManagedStorageAccount** создает управляемую учетную запись хранения в указанном хранилище ключей из файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="ae76c-109">The **Restore-AzureKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="ae76c-110">Эта управляемая учетная запись хранилища — это реплика архивированной управляемой учетной записи хранения в файле ввода и имеет то же имя, что и оригинал.</span><span class="sxs-lookup"><span data-stu-id="ae76c-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="ae76c-111">Если в хранилище ключей уже есть управляемая учетная запись хранения с тем же именем, этот командлет завершает работу с ошибкой вместо того, чтобы перезаписать оригинал.</span><span class="sxs-lookup"><span data-stu-id="ae76c-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="ae76c-112">Хранилище ключей, на которое вы восстанавливаете управляемая учетная запись хранения, может отличаться от хранилища ключей, для которого была задана резервная копия управляемой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ae76c-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="ae76c-113">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="ae76c-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ae76c-114">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="ae76c-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ae76c-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae76c-115">EXAMPLES</span></span>

### <span data-ttu-id="ae76c-116">Пример 1: восстановление резервной учетной записи с управляемым хранилищем</span><span class="sxs-lookup"><span data-stu-id="ae76c-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="ae76c-117">Эта команда восстанавливает управляемую учетную запись хранения, включая все ее версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей с именем MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="ae76c-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="ae76c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae76c-118">PARAMETERS</span></span>

### <span data-ttu-id="ae76c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae76c-119">-DefaultProfile</span></span>
<span data-ttu-id="ae76c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae76c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae76c-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ae76c-121">-InputFile</span></span>
<span data-ttu-id="ae76c-122">Входной файл.</span><span class="sxs-lookup"><span data-stu-id="ae76c-122">Input file.</span></span>
<span data-ttu-id="ae76c-123">Входной файл, содержащий заархивированный блоб</span><span class="sxs-lookup"><span data-stu-id="ae76c-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="ae76c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae76c-124">-InputObject</span></span>
<span data-ttu-id="ae76c-125">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="ae76c-125">KeyVault object</span></span>

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

### <span data-ttu-id="ae76c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae76c-126">-ResourceId</span></span>
<span data-ttu-id="ae76c-127">Идентификатор ресурса KeyVault</span><span class="sxs-lookup"><span data-stu-id="ae76c-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="ae76c-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ae76c-128">-VaultName</span></span>
<span data-ttu-id="ae76c-129">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="ae76c-129">Vault name.</span></span>
<span data-ttu-id="ae76c-130">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="ae76c-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ae76c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae76c-131">-Confirm</span></span>
<span data-ttu-id="ae76c-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae76c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae76c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae76c-133">-WhatIf</span></span>
<span data-ttu-id="ae76c-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae76c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae76c-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae76c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae76c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae76c-136">CommonParameters</span></span>
<span data-ttu-id="ae76c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae76c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae76c-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae76c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae76c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae76c-139">INPUTS</span></span>

### <span data-ttu-id="ae76c-140">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ae76c-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="ae76c-141">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae76c-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ae76c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ae76c-142">System.String</span></span>

## <span data-ttu-id="ae76c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae76c-143">OUTPUTS</span></span>

### <span data-ttu-id="ae76c-144">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae76c-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ae76c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae76c-145">NOTES</span></span>

## <span data-ttu-id="ae76c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae76c-146">RELATED LINKS</span></span>
