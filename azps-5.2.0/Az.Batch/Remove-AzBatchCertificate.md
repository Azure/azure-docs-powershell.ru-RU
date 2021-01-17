---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 2f751a6efcf4b798c69bb0dfd9ecd38c33a65d01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411487"
---
# <span data-ttu-id="32e0a-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="32e0a-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="32e0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="32e0a-103">Удаляет сертификат из учетной записи.</span><span class="sxs-lookup"><span data-stu-id="32e0a-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="32e0a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32e0a-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32e0a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32e0a-105">DESCRIPTION</span></span>
<span data-ttu-id="32e0a-106">При **этом из указанной** учетной записи Пакета Azure удаляется сертификат.</span><span class="sxs-lookup"><span data-stu-id="32e0a-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="32e0a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32e0a-107">EXAMPLES</span></span>

### <span data-ttu-id="32e0a-108">Пример 1. Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="32e0a-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="32e0a-109">Эта команда удаляет сертификат с указанным эскизом.</span><span class="sxs-lookup"><span data-stu-id="32e0a-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="32e0a-110">Пример 2. Удаление всех активных сертификатов</span><span class="sxs-lookup"><span data-stu-id="32e0a-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="32e0a-111">Эта команда получает все сертификаты, которые активны с помощью Get-AzBatchCertificate командлета.</span><span class="sxs-lookup"><span data-stu-id="32e0a-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="32e0a-112">Команда передает активные сертификаты текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="32e0a-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="32e0a-113">Этот cmdlet удаляет все сертификаты.</span><span class="sxs-lookup"><span data-stu-id="32e0a-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="32e0a-114">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="32e0a-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="32e0a-115">Таким образом, команда не будет запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="32e0a-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="32e0a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32e0a-116">PARAMETERS</span></span>

### <span data-ttu-id="32e0a-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="32e0a-117">-BatchContext</span></span>
<span data-ttu-id="32e0a-118">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="32e0a-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="32e0a-119">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32e0a-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="32e0a-120">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="32e0a-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="32e0a-121">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="32e0a-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="32e0a-122">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="32e0a-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="32e0a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e0a-123">-DefaultProfile</span></span>
<span data-ttu-id="32e0a-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32e0a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32e0a-125">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="32e0a-125">-Thumbprint</span></span>
<span data-ttu-id="32e0a-126">Определяет эскиз сертификата, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e0a-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="32e0a-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="32e0a-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="32e0a-128">Алгоритм, используемый для получения *параметра Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="32e0a-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="32e0a-129">В настоящее время допустимым значением является только sha1.</span><span class="sxs-lookup"><span data-stu-id="32e0a-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="32e0a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32e0a-130">-Confirm</span></span>
<span data-ttu-id="32e0a-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e0a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32e0a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32e0a-132">-WhatIf</span></span>
<span data-ttu-id="32e0a-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e0a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32e0a-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="32e0a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32e0a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e0a-135">CommonParameters</span></span>
<span data-ttu-id="32e0a-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e0a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e0a-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32e0a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e0a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32e0a-138">INPUTS</span></span>

### <span data-ttu-id="32e0a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="32e0a-139">System.String</span></span>

### <span data-ttu-id="32e0a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="32e0a-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="32e0a-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32e0a-141">OUTPUTS</span></span>

### <span data-ttu-id="32e0a-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="32e0a-142">System.Void</span></span>

## <span data-ttu-id="32e0a-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32e0a-143">NOTES</span></span>

## <span data-ttu-id="32e0a-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32e0a-144">RELATED LINKS</span></span>

[<span data-ttu-id="32e0a-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="32e0a-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="32e0a-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="32e0a-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="32e0a-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="32e0a-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="32e0a-148">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="32e0a-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="32e0a-149">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="32e0a-149">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
