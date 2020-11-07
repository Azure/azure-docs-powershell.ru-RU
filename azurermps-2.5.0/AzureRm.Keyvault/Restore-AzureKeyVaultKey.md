---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 7bad1311d463b8372d07a33c549682a2cade4041
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913326"
---
# <span data-ttu-id="bb093-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb093-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="bb093-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb093-102">SYNOPSIS</span></span>
<span data-ttu-id="bb093-103">Создание ключа в хранилище ключей из резервной копии ключа.</span><span class="sxs-lookup"><span data-stu-id="bb093-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb093-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb093-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb093-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb093-105">DESCRIPTION</span></span>
<span data-ttu-id="bb093-106">Командлет **RESTORE-AzureKeyVaultKey** создает ключ в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="bb093-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="bb093-107">Этот ключ является репликой резервного ключа в файле ввода и имеет то же имя, что и исходный ключ.</span><span class="sxs-lookup"><span data-stu-id="bb093-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="bb093-108">Если в хранилище ключей уже есть ключ с таким же именем, этот командлет не будет работать вместо перезаписи исходного ключа.</span><span class="sxs-lookup"><span data-stu-id="bb093-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="bb093-109">Если резервная копия имеет несколько версий ключа, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="bb093-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="bb093-110">Ключевое хранилище, в которое вы восстанавливаете ключ, может отличаться от того, с помощью которого была восстановлена клавиша.</span><span class="sxs-lookup"><span data-stu-id="bb093-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="bb093-111">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="bb093-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="bb093-112">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="bb093-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="bb093-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb093-113">EXAMPLES</span></span>

### <span data-ttu-id="bb093-114">Пример 1: восстановление резервной копии ключа</span><span class="sxs-lookup"><span data-stu-id="bb093-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="bb093-115">Эта команда восстанавливает ключ, в том числе все его версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей с именем MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="bb093-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="bb093-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb093-116">PARAMETERS</span></span>

### <span data-ttu-id="bb093-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb093-117">-DefaultProfile</span></span>
<span data-ttu-id="bb093-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bb093-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb093-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="bb093-119">-InputFile</span></span>
<span data-ttu-id="bb093-120">Задает входной файл, содержащий резервную копию ключа для восстановления.</span><span class="sxs-lookup"><span data-stu-id="bb093-120">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="bb093-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bb093-121">-VaultName</span></span>
<span data-ttu-id="bb093-122">Указывает имя хранилища ключей, в которое восстанавливается ключ.</span><span class="sxs-lookup"><span data-stu-id="bb093-122">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb093-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb093-123">-Confirm</span></span>
<span data-ttu-id="bb093-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bb093-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb093-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb093-125">-WhatIf</span></span>
<span data-ttu-id="bb093-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb093-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb093-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb093-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb093-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb093-128">CommonParameters</span></span>
<span data-ttu-id="bb093-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb093-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb093-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb093-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb093-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb093-131">INPUTS</span></span>

## <span data-ttu-id="bb093-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb093-132">OUTPUTS</span></span>

### <span data-ttu-id="bb093-133">Microsoft. Azure. Commands. KeyVault. Models. KeyBundle</span><span class="sxs-lookup"><span data-stu-id="bb093-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="bb093-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb093-134">NOTES</span></span>

## <span data-ttu-id="bb093-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb093-135">RELATED LINKS</span></span>

[<span data-ttu-id="bb093-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb093-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="bb093-137">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb093-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="bb093-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb093-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="bb093-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb093-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

