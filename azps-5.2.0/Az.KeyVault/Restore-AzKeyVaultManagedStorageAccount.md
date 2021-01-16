---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 4750561aed6643c17fed6e42d13551be76635d72
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328638"
---
# <span data-ttu-id="a0925-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0925-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="a0925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0925-102">SYNOPSIS</span></span>
<span data-ttu-id="a0925-103">Восстановление учетной записи управляемого хранилища в хранилище ключа из файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="a0925-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="a0925-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a0925-104">SYNTAX</span></span>

### <span data-ttu-id="a0925-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a0925-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0925-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a0925-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0925-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0925-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0925-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0925-108">DESCRIPTION</span></span>
<span data-ttu-id="a0925-109">С **его** учетной записью создается учетная запись управляемого хранилища в указанном хранилище из файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="a0925-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="a0925-110">Эта учетная запись управляемого хранения является копией архивной учетной записи управляемого хранилища во входных файлах и имеет то же имя, что и у исходного файла.</span><span class="sxs-lookup"><span data-stu-id="a0925-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="a0925-111">Если в хранилище ключей уже есть учетная запись управляемого хранения с таким же именем, при этом происходит сбой, а не переописывание исходного.</span><span class="sxs-lookup"><span data-stu-id="a0925-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="a0925-112">Ключевое хранилище, в которое вы восстанавливаете учетную запись управляемого хранения, может быть не таким, как в хранилище, из-за которым была восстановлена его основная учетная запись.</span><span class="sxs-lookup"><span data-stu-id="a0925-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="a0925-113">Однако ключ должен использовать ту же подписку и быть в регионе Azure в той же географической области (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="a0925-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="a0925-114">См. центр управления доверием Microsoft Azure (сопоставление регионов https://azure.microsoft.com/support/trust-center/) Azure с регионами).</span><span class="sxs-lookup"><span data-stu-id="a0925-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="a0925-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a0925-115">EXAMPLES</span></span>

### <span data-ttu-id="a0925-116">Пример 1. Восстановление учетной записи управляемого хранения</span><span class="sxs-lookup"><span data-stu-id="a0925-116">Example 1: Restore a backed-up managed storage account</span></span>
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

<span data-ttu-id="a0925-117">Эта команда восстанавливает учетную запись управляемого хранилища, включая все ее версии, из файла резервной копии Backup.blob в хранилище ключей MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="a0925-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="a0925-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0925-118">PARAMETERS</span></span>

### <span data-ttu-id="a0925-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0925-119">-DefaultProfile</span></span>
<span data-ttu-id="a0925-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0925-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0925-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a0925-121">-InputFile</span></span>
<span data-ttu-id="a0925-122">Входной файл.</span><span class="sxs-lookup"><span data-stu-id="a0925-122">Input file.</span></span>
<span data-ttu-id="a0925-123">Входной файл, содержащий исходный BLOB-файл</span><span class="sxs-lookup"><span data-stu-id="a0925-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="a0925-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0925-124">-InputObject</span></span>
<span data-ttu-id="a0925-125">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0925-125">KeyVault object</span></span>

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

### <span data-ttu-id="a0925-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0925-126">-ResourceId</span></span>
<span data-ttu-id="a0925-127">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="a0925-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="a0925-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a0925-128">-VaultName</span></span>
<span data-ttu-id="a0925-129">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="a0925-129">Vault name.</span></span>
<span data-ttu-id="a0925-130">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="a0925-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a0925-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0925-131">-Confirm</span></span>
<span data-ttu-id="a0925-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0925-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0925-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0925-133">-WhatIf</span></span>
<span data-ttu-id="a0925-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0925-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0925-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a0925-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0925-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0925-136">CommonParameters</span></span>
<span data-ttu-id="a0925-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0925-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0925-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0925-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0925-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0925-139">INPUTS</span></span>

### <span data-ttu-id="a0925-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a0925-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a0925-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a0925-141">System.String</span></span>

## <span data-ttu-id="a0925-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a0925-142">OUTPUTS</span></span>

### <span data-ttu-id="a0925-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0925-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="a0925-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a0925-144">NOTES</span></span>

## <span data-ttu-id="a0925-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0925-145">RELATED LINKS</span></span>
