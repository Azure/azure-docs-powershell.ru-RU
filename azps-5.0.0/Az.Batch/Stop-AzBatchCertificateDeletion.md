---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 53c4f4c24e0a5b1c868facd0fed8d3754fda7a41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317303"
---
# <span data-ttu-id="c14ab-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="c14ab-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="c14ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c14ab-102">SYNOPSIS</span></span>
<span data-ttu-id="c14ab-103">Отмена неудачного удаления сертификата.</span><span class="sxs-lookup"><span data-stu-id="c14ab-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="c14ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c14ab-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c14ab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c14ab-105">DESCRIPTION</span></span>
<span data-ttu-id="c14ab-106">Командлет **Stop-AzBatchCertificateDeletion** отменяет сбой при удалении сертификата в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="c14ab-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="c14ab-107">Вы можете прекратить удаление только в том случае, если сертификат находится в состоянии **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="c14ab-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="c14ab-108">Этот командлет восстанавливает сертификат в **активном** состоянии.</span><span class="sxs-lookup"><span data-stu-id="c14ab-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="c14ab-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c14ab-109">EXAMPLES</span></span>

### <span data-ttu-id="c14ab-110">Пример 1: Отмена удаления</span><span class="sxs-lookup"><span data-stu-id="c14ab-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="c14ab-111">Эта команда отменяет Удаление сертификата, для которого указан отпечаток.</span><span class="sxs-lookup"><span data-stu-id="c14ab-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="c14ab-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c14ab-112">PARAMETERS</span></span>

### <span data-ttu-id="c14ab-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c14ab-113">-BatchContext</span></span>
<span data-ttu-id="c14ab-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="c14ab-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c14ab-115">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="c14ab-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c14ab-116">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="c14ab-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c14ab-117">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="c14ab-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c14ab-118">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c14ab-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c14ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14ab-119">-DefaultProfile</span></span>
<span data-ttu-id="c14ab-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c14ab-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c14ab-121">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="c14ab-121">-Thumbprint</span></span>
<span data-ttu-id="c14ab-122">Указывает отпечаток сертификата, который этот командлет восстанавливает в **активном** состоянии.</span><span class="sxs-lookup"><span data-stu-id="c14ab-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="c14ab-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c14ab-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="c14ab-124">Указывает алгоритм, используемый для получения параметра *отпечатка* .</span><span class="sxs-lookup"><span data-stu-id="c14ab-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="c14ab-125">В настоящее время единственным допустимым значением является SHA1.</span><span class="sxs-lookup"><span data-stu-id="c14ab-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="c14ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14ab-126">CommonParameters</span></span>
<span data-ttu-id="c14ab-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c14ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14ab-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c14ab-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c14ab-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c14ab-129">INPUTS</span></span>

### <span data-ttu-id="c14ab-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c14ab-130">System.String</span></span>

### <span data-ttu-id="c14ab-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c14ab-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c14ab-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c14ab-132">OUTPUTS</span></span>

### <span data-ttu-id="c14ab-133">System. void</span><span class="sxs-lookup"><span data-stu-id="c14ab-133">System.Void</span></span>

## <span data-ttu-id="c14ab-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c14ab-134">NOTES</span></span>

## <span data-ttu-id="c14ab-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c14ab-135">RELATED LINKS</span></span>

[<span data-ttu-id="c14ab-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c14ab-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c14ab-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c14ab-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="c14ab-138">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="c14ab-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
