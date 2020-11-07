---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: aee61173ee327d0c65f4cc04451fd64f51a79522
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732854"
---
# <span data-ttu-id="b2dd1-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2dd1-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="b2dd1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2dd1-102">SYNOPSIS</span></span>
<span data-ttu-id="b2dd1-103">Создание ключа в хранилище ключей из резервной копии ключа.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2dd1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2dd1-104">SYNTAX</span></span>

### <span data-ttu-id="b2dd1-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b2dd1-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2dd1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b2dd1-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2dd1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2dd1-107">DESCRIPTION</span></span>
<span data-ttu-id="b2dd1-108">Командлет **RESTORE-AzureKeyVaultKey** создает ключ в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-108">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="b2dd1-109">Этот ключ является репликой резервного ключа в файле ввода и имеет то же имя, что и исходный ключ.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-109">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="b2dd1-110">Если в хранилище ключей уже есть ключ с таким же именем, этот командлет не будет работать вместо перезаписи исходного ключа.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-110">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="b2dd1-111">Если резервная копия имеет несколько версий ключа, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-111">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="b2dd1-112">Ключевое хранилище, в которое вы восстанавливаете ключ, может отличаться от того, с помощью которого была восстановлена клавиша.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-112">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="b2dd1-113">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="b2dd1-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="b2dd1-114">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="b2dd1-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="b2dd1-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2dd1-115">EXAMPLES</span></span>

### <span data-ttu-id="b2dd1-116">Пример 1: восстановление резервной копии ключа</span><span class="sxs-lookup"><span data-stu-id="b2dd1-116">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="b2dd1-117">Эта команда восстанавливает ключ, в том числе все его версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей с именем MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-117">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="b2dd1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2dd1-118">PARAMETERS</span></span>

### <span data-ttu-id="b2dd1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2dd1-119">-DefaultProfile</span></span>
<span data-ttu-id="b2dd1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b2dd1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd1-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b2dd1-121">-InputFile</span></span>
<span data-ttu-id="b2dd1-122">Задает входной файл, содержащий резервную копию ключа для восстановления.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-122">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2dd1-123">-InputObject</span></span>
<span data-ttu-id="b2dd1-124">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="b2dd1-124">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd1-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b2dd1-125">-VaultName</span></span>
<span data-ttu-id="b2dd1-126">Указывает имя хранилища ключей, в которое восстанавливается ключ.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-126">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2dd1-127">-Confirm</span></span>
<span data-ttu-id="b2dd1-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2dd1-129">-WhatIf</span></span>
<span data-ttu-id="b2dd1-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2dd1-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dd1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2dd1-132">CommonParameters</span></span>
<span data-ttu-id="b2dd1-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2dd1-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2dd1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2dd1-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2dd1-135">INPUTS</span></span>

### <span data-ttu-id="b2dd1-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="b2dd1-136">None</span></span>
<span data-ttu-id="b2dd1-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b2dd1-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b2dd1-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2dd1-138">OUTPUTS</span></span>

### <span data-ttu-id="b2dd1-139">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2dd1-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="b2dd1-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2dd1-140">NOTES</span></span>

## <span data-ttu-id="b2dd1-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2dd1-141">RELATED LINKS</span></span>

[<span data-ttu-id="b2dd1-142">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2dd1-142">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="b2dd1-143">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2dd1-143">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="b2dd1-144">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2dd1-144">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="b2dd1-145">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2dd1-145">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

