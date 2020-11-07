---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: bd619f6c4ec9891972d23738c1f2510cba0e2272
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733113"
---
# <span data-ttu-id="25850-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="25850-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="25850-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25850-102">SYNOPSIS</span></span>
<span data-ttu-id="25850-103">Создает секретный ключ из резервного хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="25850-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25850-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25850-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25850-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25850-105">DESCRIPTION</span></span>
<span data-ttu-id="25850-106">Командлет **RESTORE-AzureKeyVaultSecret** создает секрет в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="25850-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="25850-107">Этот секрет — это реплика резервного файла в файле входных данных с тем же именем, что и у первоначального секрета.</span><span class="sxs-lookup"><span data-stu-id="25850-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="25850-108">Если в хранилище ключей уже есть секрет с тем же именем, этот командлет не будет работать вместо перезаписи исходного секрета.</span><span class="sxs-lookup"><span data-stu-id="25850-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="25850-109">Если резервная копия имеет несколько версий секрета, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="25850-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="25850-110">Хранилище ключей, в которое вы восстановите секретный ключ, может отличаться от того, с помощью которого вы заархивированы из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="25850-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="25850-111">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="25850-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="25850-112">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="25850-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="25850-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25850-113">EXAMPLES</span></span>

### <span data-ttu-id="25850-114">Пример 1: восстановление резервной копии (секретной)</span><span class="sxs-lookup"><span data-stu-id="25850-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="25850-115">Эта команда восстанавливает секрет, в том числе все его версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей с именем MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="25850-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="25850-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25850-116">PARAMETERS</span></span>

### <span data-ttu-id="25850-117">-InputFile</span><span class="sxs-lookup"><span data-stu-id="25850-117">-InputFile</span></span>
<span data-ttu-id="25850-118">Задает входной файл, содержащий резервную копию секрета для восстановления.</span><span class="sxs-lookup"><span data-stu-id="25850-118">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="25850-119">-VaultName</span><span class="sxs-lookup"><span data-stu-id="25850-119">-VaultName</span></span>
<span data-ttu-id="25850-120">Указывает имя хранилища ключей, в которое нужно восстановить секретный код.</span><span class="sxs-lookup"><span data-stu-id="25850-120">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25850-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25850-121">-Confirm</span></span>
<span data-ttu-id="25850-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25850-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25850-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25850-123">-WhatIf</span></span>
<span data-ttu-id="25850-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25850-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25850-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25850-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25850-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25850-126">-DefaultProfile</span></span>
<span data-ttu-id="25850-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25850-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25850-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25850-128">CommonParameters</span></span>
<span data-ttu-id="25850-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25850-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25850-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25850-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25850-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25850-131">INPUTS</span></span>

## <span data-ttu-id="25850-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25850-132">OUTPUTS</span></span>

### <span data-ttu-id="25850-133">Microsoft. Azure. Commands. KeyVault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="25850-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="25850-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="25850-134">NOTES</span></span>

## <span data-ttu-id="25850-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25850-135">RELATED LINKS</span></span>

[<span data-ttu-id="25850-136">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="25850-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="25850-137">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="25850-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="25850-138">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="25850-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="25850-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="25850-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

