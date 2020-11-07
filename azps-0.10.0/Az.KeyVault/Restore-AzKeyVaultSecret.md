---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 4691d37532db3dd8e629bf1daad2654558a31de3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911165"
---
# <span data-ttu-id="12137-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="12137-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="12137-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12137-102">SYNOPSIS</span></span>
<span data-ttu-id="12137-103">Создает секретный ключ из резервного хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="12137-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="12137-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12137-104">SYNTAX</span></span>

```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12137-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12137-105">DESCRIPTION</span></span>
<span data-ttu-id="12137-106">Командлет **RESTORE-AzKeyVaultSecret** создает секрет в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="12137-106">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="12137-107">Этот секрет — это реплика резервного файла в файле входных данных с тем же именем, что и у первоначального секрета.</span><span class="sxs-lookup"><span data-stu-id="12137-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="12137-108">Если в хранилище ключей уже есть секрет с тем же именем, этот командлет не будет работать вместо перезаписи исходного секрета.</span><span class="sxs-lookup"><span data-stu-id="12137-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="12137-109">Если резервная копия имеет несколько версий секрета, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="12137-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="12137-110">Хранилище ключей, в которое вы восстановите секретный ключ, может отличаться от того, с помощью которого вы заархивированы из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="12137-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="12137-111">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="12137-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="12137-112">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="12137-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="12137-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12137-113">EXAMPLES</span></span>

### <span data-ttu-id="12137-114">Пример 1: восстановление резервной копии (секретной)</span><span class="sxs-lookup"><span data-stu-id="12137-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="12137-115">Эта команда восстанавливает секрет, в том числе все его версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей с именем MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="12137-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="12137-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12137-116">PARAMETERS</span></span>

### <span data-ttu-id="12137-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12137-117">-DefaultProfile</span></span>
<span data-ttu-id="12137-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="12137-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12137-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="12137-119">-InputFile</span></span>
<span data-ttu-id="12137-120">Задает входной файл, содержащий резервную копию секрета для восстановления.</span><span class="sxs-lookup"><span data-stu-id="12137-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="12137-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="12137-121">-VaultName</span></span>
<span data-ttu-id="12137-122">Указывает имя хранилища ключей, в которое нужно восстановить секретный код.</span><span class="sxs-lookup"><span data-stu-id="12137-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="12137-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12137-123">-Confirm</span></span>
<span data-ttu-id="12137-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="12137-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12137-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12137-125">-WhatIf</span></span>
<span data-ttu-id="12137-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="12137-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12137-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="12137-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12137-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12137-128">CommonParameters</span></span>
<span data-ttu-id="12137-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12137-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12137-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12137-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12137-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12137-131">INPUTS</span></span>

### <span data-ttu-id="12137-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="12137-132">None</span></span>
<span data-ttu-id="12137-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="12137-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12137-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12137-134">OUTPUTS</span></span>

### <span data-ttu-id="12137-135">Microsoft. Azure. Commands. KeyVault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="12137-135">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="12137-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="12137-136">NOTES</span></span>

## <span data-ttu-id="12137-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12137-137">RELATED LINKS</span></span>

[<span data-ttu-id="12137-138">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="12137-138">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="12137-139">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="12137-139">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="12137-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="12137-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="12137-141">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="12137-141">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

