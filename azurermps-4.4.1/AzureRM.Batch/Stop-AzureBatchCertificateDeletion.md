---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 820e94b75c19d49f4e49ee8419f7807a839f925b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566303"
---
# <span data-ttu-id="12d99-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="12d99-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="12d99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12d99-102">SYNOPSIS</span></span>
<span data-ttu-id="12d99-103">Отмена неудачного удаления сертификата.</span><span class="sxs-lookup"><span data-stu-id="12d99-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12d99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12d99-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12d99-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12d99-105">DESCRIPTION</span></span>
<span data-ttu-id="12d99-106">Командлет **Stop-AzureBatchCertificateDeletion** отменяет сбой при удалении сертификата в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="12d99-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="12d99-107">Вы можете прекратить удаление только в том случае, если сертификат находится в состоянии **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="12d99-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="12d99-108">Этот cmldet восстанавливает состояние сертификата в **активном** состоянии.</span><span class="sxs-lookup"><span data-stu-id="12d99-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="12d99-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12d99-109">EXAMPLES</span></span>

### <span data-ttu-id="12d99-110">Пример 1: Отмена удаления</span><span class="sxs-lookup"><span data-stu-id="12d99-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="12d99-111">Эта команда отменяет Удаление сертификата, для которого указан отпечаток.</span><span class="sxs-lookup"><span data-stu-id="12d99-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="12d99-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12d99-112">PARAMETERS</span></span>

### <span data-ttu-id="12d99-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="12d99-113">-BatchContext</span></span>
<span data-ttu-id="12d99-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="12d99-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="12d99-115">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="12d99-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="12d99-116">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="12d99-116">-Thumbprint</span></span>
<span data-ttu-id="12d99-117">Указывает отпечаток сертификата, который этот командлет восстанавливает в **активном** состоянии.</span><span class="sxs-lookup"><span data-stu-id="12d99-117">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="12d99-118">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="12d99-118">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="12d99-119">Указывает алгоритм, используемый для получения параметра *отпечатка* .</span><span class="sxs-lookup"><span data-stu-id="12d99-119">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="12d99-120">В настоящее время единственным допустимым значением является SHA1.</span><span class="sxs-lookup"><span data-stu-id="12d99-120">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="12d99-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d99-121">-DefaultProfile</span></span>
<span data-ttu-id="12d99-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12d99-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12d99-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d99-123">CommonParameters</span></span>
<span data-ttu-id="12d99-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12d99-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d99-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d99-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d99-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12d99-126">INPUTS</span></span>

### <span data-ttu-id="12d99-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="12d99-127">BatchAccountContext</span></span>
<span data-ttu-id="12d99-128">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="12d99-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="12d99-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12d99-129">OUTPUTS</span></span>

## <span data-ttu-id="12d99-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="12d99-130">NOTES</span></span>

## <span data-ttu-id="12d99-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12d99-131">RELATED LINKS</span></span>

[<span data-ttu-id="12d99-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="12d99-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="12d99-133">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="12d99-133">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="12d99-134">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="12d99-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


