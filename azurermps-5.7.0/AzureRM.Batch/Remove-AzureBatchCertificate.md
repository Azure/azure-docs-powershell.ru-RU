---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: e62aebd6a03f7d5a162f141eae55e3df6c9a0a88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568250"
---
# <span data-ttu-id="bec57-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="bec57-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="bec57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bec57-102">SYNOPSIS</span></span>
<span data-ttu-id="bec57-103">Удаление сертификата из учетной записи.</span><span class="sxs-lookup"><span data-stu-id="bec57-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bec57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bec57-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bec57-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bec57-105">DESCRIPTION</span></span>
<span data-ttu-id="bec57-106">Командлет **Remove-AzureBatchCertificate** Удаляет сертификат из указанной пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="bec57-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="bec57-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bec57-107">EXAMPLES</span></span>

### <span data-ttu-id="bec57-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="bec57-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="bec57-109">Эта команда удаляет сертификат с указанным отпечатком.</span><span class="sxs-lookup"><span data-stu-id="bec57-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="bec57-110">Пример 2: удаление всех активных сертификатов</span><span class="sxs-lookup"><span data-stu-id="bec57-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="bec57-111">Эта команда получает все активные сертификаты с помощью командлета Get-AzureBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="bec57-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="bec57-112">Команда передает активные сертификаты в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="bec57-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bec57-113">Этот командлет удаляет каждый сертификат.</span><span class="sxs-lookup"><span data-stu-id="bec57-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="bec57-114">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="bec57-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="bec57-115">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="bec57-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bec57-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bec57-116">PARAMETERS</span></span>

### <span data-ttu-id="bec57-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bec57-117">-BatchContext</span></span>
<span data-ttu-id="bec57-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="bec57-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bec57-119">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="bec57-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bec57-120">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="bec57-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bec57-121">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="bec57-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bec57-122">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bec57-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bec57-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec57-123">-DefaultProfile</span></span>
<span data-ttu-id="bec57-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bec57-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bec57-125">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="bec57-125">-Thumbprint</span></span>
<span data-ttu-id="bec57-126">Указывает отпечаток сертификата, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="bec57-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec57-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="bec57-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="bec57-128">Указывает алгоритм, используемый для получения параметра *отпечатка* .</span><span class="sxs-lookup"><span data-stu-id="bec57-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="bec57-129">В настоящее время единственным допустимым значением является SHA1.</span><span class="sxs-lookup"><span data-stu-id="bec57-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="bec57-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bec57-130">-Confirm</span></span>
<span data-ttu-id="bec57-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bec57-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec57-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec57-132">-WhatIf</span></span>
<span data-ttu-id="bec57-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bec57-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec57-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bec57-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec57-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec57-135">CommonParameters</span></span>
<span data-ttu-id="bec57-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bec57-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec57-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec57-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec57-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bec57-138">INPUTS</span></span>

### <span data-ttu-id="bec57-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bec57-139">BatchAccountContext</span></span>
<span data-ttu-id="bec57-140">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bec57-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="bec57-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bec57-141">OUTPUTS</span></span>

## <span data-ttu-id="bec57-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="bec57-142">NOTES</span></span>

## <span data-ttu-id="bec57-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bec57-143">RELATED LINKS</span></span>

[<span data-ttu-id="bec57-144">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="bec57-144">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="bec57-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bec57-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bec57-146">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="bec57-146">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="bec57-147">Остановить-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="bec57-147">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="bec57-148">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="bec57-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


