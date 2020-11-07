---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: b8ce1dc13204cfeeb63f5b7eb45f57e2117da511
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913325"
---
# <span data-ttu-id="1876e-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1876e-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="1876e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1876e-102">SYNOPSIS</span></span>
<span data-ttu-id="1876e-103">Создает секретный ключ из резервного хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1876e-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1876e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1876e-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1876e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1876e-105">DESCRIPTION</span></span>
<span data-ttu-id="1876e-106">Командлет **RESTORE-AzureKeyVaultSecret** создает секрет в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="1876e-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="1876e-107">Этот секрет — это реплика резервного файла в файле входных данных с тем же именем, что и у первоначального секрета.</span><span class="sxs-lookup"><span data-stu-id="1876e-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="1876e-108">Если в хранилище ключей уже есть секрет с тем же именем, этот командлет не будет работать вместо перезаписи исходного секрета.</span><span class="sxs-lookup"><span data-stu-id="1876e-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="1876e-109">Если резервная копия имеет несколько версий секрета, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="1876e-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="1876e-110">Хранилище ключей, в которое вы восстановите секретный ключ, может отличаться от того, с помощью которого вы заархивированы из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1876e-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="1876e-111">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="1876e-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="1876e-112">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="1876e-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="1876e-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1876e-113">EXAMPLES</span></span>

### <span data-ttu-id="1876e-114">Пример 1: восстановление резервной копии (секретной)</span><span class="sxs-lookup"><span data-stu-id="1876e-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="1876e-115">Эта команда восстанавливает секрет, в том числе все его версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей с именем MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="1876e-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="1876e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1876e-116">PARAMETERS</span></span>

### <span data-ttu-id="1876e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1876e-117">-DefaultProfile</span></span>
<span data-ttu-id="1876e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1876e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1876e-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="1876e-119">-InputFile</span></span>
<span data-ttu-id="1876e-120">Задает входной файл, содержащий резервную копию секрета для восстановления.</span><span class="sxs-lookup"><span data-stu-id="1876e-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="1876e-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1876e-121">-VaultName</span></span>
<span data-ttu-id="1876e-122">Указывает имя хранилища ключей, в которое нужно восстановить секретный код.</span><span class="sxs-lookup"><span data-stu-id="1876e-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="1876e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1876e-123">-Confirm</span></span>
<span data-ttu-id="1876e-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1876e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1876e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1876e-125">-WhatIf</span></span>
<span data-ttu-id="1876e-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1876e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1876e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1876e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1876e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1876e-128">CommonParameters</span></span>
<span data-ttu-id="1876e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1876e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1876e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1876e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1876e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1876e-131">INPUTS</span></span>

## <span data-ttu-id="1876e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1876e-132">OUTPUTS</span></span>

### <span data-ttu-id="1876e-133">Microsoft. Azure. Commands. KeyVault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="1876e-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="1876e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="1876e-134">NOTES</span></span>

## <span data-ttu-id="1876e-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1876e-135">RELATED LINKS</span></span>

[<span data-ttu-id="1876e-136">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1876e-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="1876e-137">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1876e-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="1876e-138">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1876e-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="1876e-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="1876e-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

