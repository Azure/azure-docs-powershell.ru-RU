---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: 1fb58d348af5f507e1bd3c8451f12918c69b309b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569376"
---
# <span data-ttu-id="0ebff-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0ebff-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="0ebff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ebff-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebff-103">Создание ключа в хранилище ключей из резервной копии ключа.</span><span class="sxs-lookup"><span data-stu-id="0ebff-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ebff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ebff-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ebff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ebff-105">DESCRIPTION</span></span>
<span data-ttu-id="0ebff-106">Командлет **RESTORE-AzureKeyVaultKey** создает ключ в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="0ebff-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="0ebff-107">Этот ключ является репликой резервного ключа в файле ввода и имеет то же имя, что и исходный ключ.</span><span class="sxs-lookup"><span data-stu-id="0ebff-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="0ebff-108">Если в хранилище ключей уже есть ключ с таким же именем, этот командлет не будет работать вместо перезаписи исходного ключа.</span><span class="sxs-lookup"><span data-stu-id="0ebff-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="0ebff-109">Если резервная копия имеет несколько версий ключа, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="0ebff-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="0ebff-110">Ключевое хранилище, в которое вы восстанавливаете ключ, может отличаться от того, с помощью которого была восстановлена клавиша.</span><span class="sxs-lookup"><span data-stu-id="0ebff-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="0ebff-111">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="0ebff-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="0ebff-112">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="0ebff-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="0ebff-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ebff-113">EXAMPLES</span></span>

### <span data-ttu-id="0ebff-114">Пример 1: восстановление резервной копии ключа</span><span class="sxs-lookup"><span data-stu-id="0ebff-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="0ebff-115">Эта команда восстанавливает ключ, в том числе все его версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей с именем MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0ebff-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="0ebff-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ebff-116">PARAMETERS</span></span>

### <span data-ttu-id="0ebff-117">-InputFile</span><span class="sxs-lookup"><span data-stu-id="0ebff-117">-InputFile</span></span>
<span data-ttu-id="0ebff-118">Задает входной файл, содержащий резервную копию ключа для восстановления.</span><span class="sxs-lookup"><span data-stu-id="0ebff-118">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="0ebff-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0ebff-119">-VaultName</span></span>
<span data-ttu-id="0ebff-120">Указывает имя хранилища ключей, в которое восстанавливается ключ.</span><span class="sxs-lookup"><span data-stu-id="0ebff-120">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ebff-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ebff-121">-Confirm</span></span>
<span data-ttu-id="0ebff-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ebff-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ebff-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ebff-123">-WhatIf</span></span>
<span data-ttu-id="0ebff-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ebff-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ebff-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ebff-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ebff-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebff-126">-DefaultProfile</span></span>
<span data-ttu-id="0ebff-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebff-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ebff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebff-128">CommonParameters</span></span>
<span data-ttu-id="0ebff-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ebff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebff-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ebff-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebff-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ebff-131">INPUTS</span></span>

## <span data-ttu-id="0ebff-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ebff-132">OUTPUTS</span></span>

### <span data-ttu-id="0ebff-133">Microsoft. Azure. Commands. KeyVault. Models. KeyBundle</span><span class="sxs-lookup"><span data-stu-id="0ebff-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="0ebff-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ebff-134">NOTES</span></span>

## <span data-ttu-id="0ebff-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ebff-135">RELATED LINKS</span></span>

[<span data-ttu-id="0ebff-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0ebff-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="0ebff-137">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0ebff-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="0ebff-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0ebff-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="0ebff-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0ebff-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

