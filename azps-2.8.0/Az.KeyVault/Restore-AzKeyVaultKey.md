---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: bcdcda3015c3d6f7e255b8b2778b69254b031cc0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720624"
---
# <span data-ttu-id="f61ab-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f61ab-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="f61ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f61ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f61ab-103">Создание ключа в хранилище ключей из резервной копии ключа.</span><span class="sxs-lookup"><span data-stu-id="f61ab-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="f61ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f61ab-104">SYNTAX</span></span>

### <span data-ttu-id="f61ab-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f61ab-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f61ab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f61ab-106">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f61ab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f61ab-107">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f61ab-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f61ab-108">DESCRIPTION</span></span>
<span data-ttu-id="f61ab-109">Командлет **RESTORE-AzKeyVaultKey** создает ключ в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f61ab-109">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="f61ab-110">Этот ключ является репликой резервного ключа в файле ввода и имеет то же имя, что и исходный ключ.</span><span class="sxs-lookup"><span data-stu-id="f61ab-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="f61ab-111">Если в хранилище ключей уже есть ключ с таким же именем, этот командлет не будет работать вместо перезаписи исходного ключа.</span><span class="sxs-lookup"><span data-stu-id="f61ab-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="f61ab-112">Если резервная копия имеет несколько версий ключа, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="f61ab-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="f61ab-113">Ключевое хранилище, в которое вы восстанавливаете ключ, может отличаться от того, с помощью которого была восстановлена клавиша.</span><span class="sxs-lookup"><span data-stu-id="f61ab-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="f61ab-114">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="f61ab-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="f61ab-115">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="f61ab-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="f61ab-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f61ab-116">EXAMPLES</span></span>

### <span data-ttu-id="f61ab-117">Пример 1: восстановление резервной копии ключа</span><span class="sxs-lookup"><span data-stu-id="f61ab-117">Example 1: Restore a backed-up key</span></span>
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

<span data-ttu-id="f61ab-118">Эта команда восстанавливает ключ, в том числе все его версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей с именем MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="f61ab-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="f61ab-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f61ab-119">PARAMETERS</span></span>

### <span data-ttu-id="f61ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f61ab-120">-DefaultProfile</span></span>
<span data-ttu-id="f61ab-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f61ab-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f61ab-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f61ab-122">-InputFile</span></span>
<span data-ttu-id="f61ab-123">Задает входной файл, содержащий резервную копию ключа для восстановления.</span><span class="sxs-lookup"><span data-stu-id="f61ab-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="f61ab-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f61ab-124">-InputObject</span></span>
<span data-ttu-id="f61ab-125">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="f61ab-125">KeyVault object</span></span>

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

### <span data-ttu-id="f61ab-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f61ab-126">-ResourceId</span></span>
<span data-ttu-id="f61ab-127">Идентификатор ресурса KeyVault</span><span class="sxs-lookup"><span data-stu-id="f61ab-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="f61ab-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f61ab-128">-VaultName</span></span>
<span data-ttu-id="f61ab-129">Указывает имя хранилища ключей, в которое восстанавливается ключ.</span><span class="sxs-lookup"><span data-stu-id="f61ab-129">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="f61ab-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f61ab-130">-Confirm</span></span>
<span data-ttu-id="f61ab-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f61ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f61ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f61ab-132">-WhatIf</span></span>
<span data-ttu-id="f61ab-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f61ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f61ab-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f61ab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f61ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f61ab-135">CommonParameters</span></span>
<span data-ttu-id="f61ab-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f61ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f61ab-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f61ab-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f61ab-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f61ab-138">INPUTS</span></span>

### <span data-ttu-id="f61ab-139">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f61ab-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f61ab-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f61ab-140">System.String</span></span>

## <span data-ttu-id="f61ab-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f61ab-141">OUTPUTS</span></span>

### <span data-ttu-id="f61ab-142">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f61ab-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="f61ab-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="f61ab-143">NOTES</span></span>

## <span data-ttu-id="f61ab-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f61ab-144">RELATED LINKS</span></span>

[<span data-ttu-id="f61ab-145">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f61ab-145">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="f61ab-146">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f61ab-146">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="f61ab-147">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f61ab-147">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="f61ab-148">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f61ab-148">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

