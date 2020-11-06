---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: 7e8159a7a17276d749adb89ea4e1b82118f9b2bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565917"
---
# <span data-ttu-id="e3600-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e3600-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="e3600-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3600-102">SYNOPSIS</span></span>
<span data-ttu-id="e3600-103">Удаление сертификата из учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e3600-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3600-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3600-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3600-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3600-105">DESCRIPTION</span></span>
<span data-ttu-id="e3600-106">Командлет **Remove-AzureBatchCertificate** Удаляет сертификат из указанной пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="e3600-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="e3600-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3600-107">EXAMPLES</span></span>

### <span data-ttu-id="e3600-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="e3600-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="e3600-109">Эта команда удаляет сертификат с указанным отпечатком.</span><span class="sxs-lookup"><span data-stu-id="e3600-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="e3600-110">Пример 2: удаление всех активных сертификатов</span><span class="sxs-lookup"><span data-stu-id="e3600-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="e3600-111">Эта команда получает все активные сертификаты с помощью командлета Get-AzureBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="e3600-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="e3600-112">Команда передает активные сертификаты в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="e3600-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e3600-113">Этот командлет удаляет каждый сертификат.</span><span class="sxs-lookup"><span data-stu-id="e3600-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="e3600-114">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="e3600-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e3600-115">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e3600-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e3600-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3600-116">PARAMETERS</span></span>

### <span data-ttu-id="e3600-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e3600-117">-BatchContext</span></span>
<span data-ttu-id="e3600-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="e3600-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e3600-119">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="e3600-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e3600-120">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="e3600-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e3600-121">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="e3600-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e3600-122">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e3600-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3600-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3600-123">-DefaultProfile</span></span>
<span data-ttu-id="e3600-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3600-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3600-125">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="e3600-125">-Thumbprint</span></span>
<span data-ttu-id="e3600-126">Указывает отпечаток сертификата, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e3600-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e3600-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e3600-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e3600-128">Указывает алгоритм, используемый для получения параметра *отпечатка* .</span><span class="sxs-lookup"><span data-stu-id="e3600-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="e3600-129">В настоящее время единственным допустимым значением является SHA1.</span><span class="sxs-lookup"><span data-stu-id="e3600-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="e3600-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3600-130">-Confirm</span></span>
<span data-ttu-id="e3600-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e3600-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3600-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3600-132">-WhatIf</span></span>
<span data-ttu-id="e3600-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e3600-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3600-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e3600-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3600-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3600-135">CommonParameters</span></span>
<span data-ttu-id="e3600-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3600-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3600-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3600-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3600-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3600-138">INPUTS</span></span>

### <span data-ttu-id="e3600-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e3600-139">System.String</span></span>

### <span data-ttu-id="e3600-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e3600-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e3600-141">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e3600-141">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e3600-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3600-142">OUTPUTS</span></span>

### <span data-ttu-id="e3600-143">System. void</span><span class="sxs-lookup"><span data-stu-id="e3600-143">System.Void</span></span>

## <span data-ttu-id="e3600-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3600-144">NOTES</span></span>

## <span data-ttu-id="e3600-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3600-145">RELATED LINKS</span></span>

[<span data-ttu-id="e3600-146">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e3600-146">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="e3600-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e3600-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e3600-148">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e3600-148">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="e3600-149">Остановить-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="e3600-149">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="e3600-150">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="e3600-150">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


