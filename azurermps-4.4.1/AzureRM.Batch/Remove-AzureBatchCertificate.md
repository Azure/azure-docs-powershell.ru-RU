---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: c63caed99a10851d6172e0db5dcc33e3404be215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560503"
---
# <span data-ttu-id="f7971-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f7971-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="f7971-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7971-102">SYNOPSIS</span></span>
<span data-ttu-id="f7971-103">Удаление сертификата из учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f7971-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7971-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7971-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7971-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7971-105">DESCRIPTION</span></span>
<span data-ttu-id="f7971-106">Командлет **Remove-AzureBatchCertificate** Удаляет сертификат из указанной пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="f7971-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="f7971-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7971-107">EXAMPLES</span></span>

### <span data-ttu-id="f7971-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="f7971-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="f7971-109">Эта команда удаляет сертификат с указанным отпечатком.</span><span class="sxs-lookup"><span data-stu-id="f7971-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="f7971-110">Пример 2: удаление всех активных сертификатов</span><span class="sxs-lookup"><span data-stu-id="f7971-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="f7971-111">Эта команда получает все активные сертификаты с помощью командлета Get-AzureBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="f7971-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="f7971-112">Команда передает активные сертификаты в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="f7971-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f7971-113">Этот командлет удаляет каждый сертификат.</span><span class="sxs-lookup"><span data-stu-id="f7971-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="f7971-114">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="f7971-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f7971-115">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f7971-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f7971-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7971-116">PARAMETERS</span></span>

### <span data-ttu-id="f7971-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f7971-117">-BatchContext</span></span>
<span data-ttu-id="f7971-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="f7971-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f7971-119">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="f7971-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="f7971-120">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="f7971-120">-Thumbprint</span></span>
<span data-ttu-id="f7971-121">Указывает отпечаток сертификата, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f7971-121">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="f7971-122">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f7971-122">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="f7971-123">Указывает алгоритм, используемый для получения параметра *отпечатка* .</span><span class="sxs-lookup"><span data-stu-id="f7971-123">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="f7971-124">В настоящее время единственным допустимым значением является SHA1.</span><span class="sxs-lookup"><span data-stu-id="f7971-124">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="f7971-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7971-125">-Confirm</span></span>
<span data-ttu-id="f7971-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7971-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7971-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7971-127">-WhatIf</span></span>
<span data-ttu-id="f7971-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7971-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7971-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7971-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7971-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7971-130">-DefaultProfile</span></span>
<span data-ttu-id="f7971-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7971-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7971-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7971-132">CommonParameters</span></span>
<span data-ttu-id="f7971-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7971-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7971-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7971-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7971-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7971-135">INPUTS</span></span>

### <span data-ttu-id="f7971-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f7971-136">BatchAccountContext</span></span>
<span data-ttu-id="f7971-137">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f7971-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="f7971-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7971-138">OUTPUTS</span></span>

## <span data-ttu-id="f7971-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7971-139">NOTES</span></span>

## <span data-ttu-id="f7971-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7971-140">RELATED LINKS</span></span>

[<span data-ttu-id="f7971-141">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f7971-141">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="f7971-142">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f7971-142">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f7971-143">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="f7971-143">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="f7971-144">Остановить-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="f7971-144">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="f7971-145">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="f7971-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


