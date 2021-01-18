---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 958aeb36ba047284085d471f73aadad78b756839
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504716"
---
# <span data-ttu-id="722e2-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="722e2-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="722e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="722e2-102">SYNOPSIS</span></span>
<span data-ttu-id="722e2-103">Создает ключ в хранилище ключей из клавиши, создав ее.</span><span class="sxs-lookup"><span data-stu-id="722e2-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="722e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="722e2-104">SYNTAX</span></span>

### <span data-ttu-id="722e2-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="722e2-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="722e2-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="722e2-106">HsmByVaultName</span></span>
```
Restore-AzKeyVaultKey -HsmName <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="722e2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="722e2-107">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="722e2-108">HsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="722e2-108">HsmByInputObject</span></span>
```
Restore-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="722e2-109">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="722e2-109">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="722e2-110">HsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="722e2-110">HsmByResourceId</span></span>
```
Restore-AzKeyVaultKey -HsmResourceId <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="722e2-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="722e2-111">DESCRIPTION</span></span>
<span data-ttu-id="722e2-112">При **нажатии на клавиши Restore-AzKeyVaultKey** в указанном хранилище ключа создается ключ.</span><span class="sxs-lookup"><span data-stu-id="722e2-112">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="722e2-113">Этот ключ является копией файла ввода с тем же именем, что и у исходного ключа.</span><span class="sxs-lookup"><span data-stu-id="722e2-113">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="722e2-114">Если в хранилище ключей уже есть ключ с таким же именем, этот cmdlet не переопишет исходный ключ.</span><span class="sxs-lookup"><span data-stu-id="722e2-114">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="722e2-115">Если резервная копия содержит несколько версий ключа, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="722e2-115">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="722e2-116">Хранилище ключей, в которое вы восстанавливаете ключ, может быть не таким, как в хранилище ключей, из хранилища, в который вы его вернули.</span><span class="sxs-lookup"><span data-stu-id="722e2-116">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="722e2-117">Однако ключ должен использовать ту же подписку и быть в регионе Azure в той же географической области (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="722e2-117">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="722e2-118">См. центр управления доверием Microsoft Azure (сопоставление регионов https://azure.microsoft.com/support/trust-center/) Azure с регионами).</span><span class="sxs-lookup"><span data-stu-id="722e2-118">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="722e2-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="722e2-119">EXAMPLES</span></span>

### <span data-ttu-id="722e2-120">Пример 1. Восстановление back-up key</span><span class="sxs-lookup"><span data-stu-id="722e2-120">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="722e2-121">Эта команда восстанавливает ключ, включая все его версии, из файла резервной копии Backup.blob в хранилище ключей MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="722e2-121">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="722e2-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="722e2-122">PARAMETERS</span></span>

### <span data-ttu-id="722e2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="722e2-123">-DefaultProfile</span></span>
<span data-ttu-id="722e2-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="722e2-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="722e2-125">-HsmName</span><span class="sxs-lookup"><span data-stu-id="722e2-125">-HsmName</span></span>
<span data-ttu-id="722e2-126">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="722e2-126">HSM name.</span></span> <span data-ttu-id="722e2-127">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="722e2-127">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722e2-128">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="722e2-128">-HsmObject</span></span>
<span data-ttu-id="722e2-129">Объект HSM</span><span class="sxs-lookup"><span data-stu-id="722e2-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="722e2-130">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="722e2-130">-HsmResourceId</span></span>
<span data-ttu-id="722e2-131">Hsm Resource Id</span><span class="sxs-lookup"><span data-stu-id="722e2-131">Hsm Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="722e2-132">-InputFile</span><span class="sxs-lookup"><span data-stu-id="722e2-132">-InputFile</span></span>
<span data-ttu-id="722e2-133">Определяет входной файл, содержащий резервную копию ключа для восстановления.</span><span class="sxs-lookup"><span data-stu-id="722e2-133">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="722e2-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="722e2-134">-InputObject</span></span>
<span data-ttu-id="722e2-135">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="722e2-135">KeyVault object</span></span>

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

### <span data-ttu-id="722e2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="722e2-136">-ResourceId</span></span>
<span data-ttu-id="722e2-137">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="722e2-137">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="722e2-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="722e2-138">-VaultName</span></span>
<span data-ttu-id="722e2-139">Указывает имя сейфа ключа, в который нужно восстановить ключ.</span><span class="sxs-lookup"><span data-stu-id="722e2-139">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="722e2-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="722e2-140">-Confirm</span></span>
<span data-ttu-id="722e2-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="722e2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="722e2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="722e2-142">-WhatIf</span></span>
<span data-ttu-id="722e2-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="722e2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="722e2-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="722e2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="722e2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="722e2-145">CommonParameters</span></span>
<span data-ttu-id="722e2-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="722e2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="722e2-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="722e2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="722e2-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="722e2-148">INPUTS</span></span>

### <span data-ttu-id="722e2-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="722e2-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="722e2-150">System.String</span><span class="sxs-lookup"><span data-stu-id="722e2-150">System.String</span></span>

## <span data-ttu-id="722e2-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="722e2-151">OUTPUTS</span></span>

### <span data-ttu-id="722e2-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="722e2-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="722e2-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="722e2-153">NOTES</span></span>

## <span data-ttu-id="722e2-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="722e2-154">RELATED LINKS</span></span>

[<span data-ttu-id="722e2-155">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="722e2-155">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="722e2-156">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="722e2-156">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="722e2-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="722e2-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="722e2-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="722e2-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

