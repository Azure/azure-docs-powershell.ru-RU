---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 53c4f4c24e0a5b1c868facd0fed8d3754fda7a41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509545"
---
# <span data-ttu-id="a167f-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="a167f-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="a167f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a167f-102">SYNOPSIS</span></span>
<span data-ttu-id="a167f-103">Отмена сбойного удаления сертификата.</span><span class="sxs-lookup"><span data-stu-id="a167f-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="a167f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a167f-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a167f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a167f-105">DESCRIPTION</span></span>
<span data-ttu-id="a167f-106">**Cmdlet Stop-AzBatchCertificateDeletion** отменяет сбой удаления сертификата в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="a167f-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="a167f-107">Удаление можно прекратить только в том случае, если сертификат имеет состояние **DeleteFailed.**</span><span class="sxs-lookup"><span data-stu-id="a167f-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="a167f-108">Этот cmdlet восстанавливает состояние **"Активная" сертификата.**</span><span class="sxs-lookup"><span data-stu-id="a167f-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="a167f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a167f-109">EXAMPLES</span></span>

### <span data-ttu-id="a167f-110">Пример 1. Отмена удаления</span><span class="sxs-lookup"><span data-stu-id="a167f-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="a167f-111">Эта команда отменяет удаление сертификата с указанным эскизом.</span><span class="sxs-lookup"><span data-stu-id="a167f-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="a167f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a167f-112">PARAMETERS</span></span>

### <span data-ttu-id="a167f-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a167f-113">-BatchContext</span></span>
<span data-ttu-id="a167f-114">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="a167f-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a167f-115">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a167f-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a167f-116">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="a167f-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a167f-117">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a167f-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a167f-118">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a167f-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a167f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a167f-119">-DefaultProfile</span></span>
<span data-ttu-id="a167f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a167f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a167f-121">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="a167f-121">-Thumbprint</span></span>
<span data-ttu-id="a167f-122">Определяет эскиз сертификата, который этот cmdlet восстанавливает состояние **"Активный".**</span><span class="sxs-lookup"><span data-stu-id="a167f-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="a167f-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="a167f-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="a167f-124">Алгоритм, используемый для получения *параметра Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="a167f-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="a167f-125">В настоящее время допустимым значением является только sha1.</span><span class="sxs-lookup"><span data-stu-id="a167f-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="a167f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a167f-126">CommonParameters</span></span>
<span data-ttu-id="a167f-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a167f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a167f-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a167f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a167f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a167f-129">INPUTS</span></span>

### <span data-ttu-id="a167f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a167f-130">System.String</span></span>

### <span data-ttu-id="a167f-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a167f-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a167f-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a167f-132">OUTPUTS</span></span>

### <span data-ttu-id="a167f-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="a167f-133">System.Void</span></span>

## <span data-ttu-id="a167f-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a167f-134">NOTES</span></span>

## <span data-ttu-id="a167f-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a167f-135">RELATED LINKS</span></span>

[<span data-ttu-id="a167f-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a167f-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a167f-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="a167f-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="a167f-138">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="a167f-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
