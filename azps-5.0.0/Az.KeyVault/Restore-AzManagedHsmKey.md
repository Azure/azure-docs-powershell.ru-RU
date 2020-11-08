---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
ms.openlocfilehash: 38e0dbf124643a7d669c1787314790166e88f6a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250201"
---
# <span data-ttu-id="a073b-101">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a073b-101">Restore-AzManagedHsmKey</span></span>

## <span data-ttu-id="a073b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a073b-102">SYNOPSIS</span></span>
<span data-ttu-id="a073b-103">Создание ключа в управляемом HSM-разделе из резервной клавиши.</span><span class="sxs-lookup"><span data-stu-id="a073b-103">Creates a key in a managed HSM from a backed-up key.</span></span>

## <span data-ttu-id="a073b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a073b-104">SYNTAX</span></span>

### <span data-ttu-id="a073b-105">ByHsmName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a073b-105">ByHsmName (Default)</span></span>
```
Restore-AzManagedHsmKey [-HsmName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a073b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a073b-106">ByInputObject</span></span>
```
Restore-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a073b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a073b-107">ByResourceId</span></span>
```
Restore-AzManagedHsmKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a073b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a073b-108">DESCRIPTION</span></span>
<span data-ttu-id="a073b-109">Командлет **RESTORE-AzManagedHsmKey** создает ключ в указанном управляемом HSM.</span><span class="sxs-lookup"><span data-stu-id="a073b-109">The **Restore-AzManagedHsmKey** cmdlet creates a key in the specified managed HSM.</span></span>
<span data-ttu-id="a073b-110">Этот ключ является репликой резервного ключа в файле ввода и имеет то же имя, что и исходный ключ.</span><span class="sxs-lookup"><span data-stu-id="a073b-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="a073b-111">Если управляемый HSM уже имеет ключ с таким же именем, этот командлет завершает работу с ошибкой вместо перезаписи исходного ключа.</span><span class="sxs-lookup"><span data-stu-id="a073b-111">If the managed HSM already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="a073b-112">Если резервная копия имеет несколько версий ключа, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="a073b-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="a073b-113">Управляемый HSM-код, в который вы восстанавливаете ключ, может отличаться от управляемого HSM-аппарата, для которого вы заархивированы ключ.</span><span class="sxs-lookup"><span data-stu-id="a073b-113">The managed HSM that you restore the key into can be different from the managed HSM that you backed up the key from.</span></span>
<span data-ttu-id="a073b-114">Однако управляемый HSM-файл должен использовать одну и ту же подписку и находиться в регионе Azure в том же географическом районе (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="a073b-114">However, the managed HSM must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="a073b-115">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="a073b-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="a073b-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a073b-116">EXAMPLES</span></span>

### <span data-ttu-id="a073b-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a073b-117">Example 1</span></span>
```powershell
PS C:\> Restore-AzManagedHsmKey -HsmName testmhsm -InputFile "C:\Backup.blob"

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="a073b-118">Эта команда восстанавливает ключ, в том числе все его версии, из файла резервной копии с именем Backup. BLOB в управляемый HSM-файл с именем testmhsm.</span><span class="sxs-lookup"><span data-stu-id="a073b-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the managed HSM named testmhsm.</span></span>

## <span data-ttu-id="a073b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a073b-119">PARAMETERS</span></span>

### <span data-ttu-id="a073b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a073b-120">-DefaultProfile</span></span>
<span data-ttu-id="a073b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a073b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a073b-122">-HsmName</span><span class="sxs-lookup"><span data-stu-id="a073b-122">-HsmName</span></span>
<span data-ttu-id="a073b-123">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="a073b-123">HSM name.</span></span> <span data-ttu-id="a073b-124">Командлет создает полное доменное имя управляемого HSM-файла на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="a073b-124">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHsmName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a073b-125">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a073b-125">-InputFile</span></span>
<span data-ttu-id="a073b-126">Входной файл.</span><span class="sxs-lookup"><span data-stu-id="a073b-126">Input file.</span></span>
<span data-ttu-id="a073b-127">Входной файл, содержащий заархивированный блоб</span><span class="sxs-lookup"><span data-stu-id="a073b-127">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="a073b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a073b-128">-InputObject</span></span>
<span data-ttu-id="a073b-129">Объект HSM</span><span class="sxs-lookup"><span data-stu-id="a073b-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a073b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a073b-130">-ResourceId</span></span>
<span data-ttu-id="a073b-131">Идентификатор ресурса HSM</span><span class="sxs-lookup"><span data-stu-id="a073b-131">HSM Resource Id</span></span>

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

### <span data-ttu-id="a073b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a073b-132">-Confirm</span></span>
<span data-ttu-id="a073b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a073b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a073b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a073b-134">-WhatIf</span></span>
<span data-ttu-id="a073b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a073b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a073b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a073b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a073b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a073b-137">CommonParameters</span></span>
<span data-ttu-id="a073b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a073b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a073b-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a073b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a073b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a073b-140">INPUTS</span></span>

### <span data-ttu-id="a073b-141">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a073b-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="a073b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a073b-142">System.String</span></span>

## <span data-ttu-id="a073b-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a073b-143">OUTPUTS</span></span>

### <span data-ttu-id="a073b-144">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="a073b-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="a073b-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="a073b-145">NOTES</span></span>

## <span data-ttu-id="a073b-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a073b-146">RELATED LINKS</span></span>

[<span data-ttu-id="a073b-147">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a073b-147">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="a073b-148">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a073b-148">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="a073b-149">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a073b-149">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="a073b-150">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="a073b-150">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="a073b-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a073b-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="a073b-152">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="a073b-152">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)