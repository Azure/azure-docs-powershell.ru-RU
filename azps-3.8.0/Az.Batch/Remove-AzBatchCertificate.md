---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: f34500b72936191182c5486051a97b9e74cada16
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077207"
---
# <span data-ttu-id="63ea3-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="63ea3-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="63ea3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="63ea3-103">Удаление сертификата из учетной записи.</span><span class="sxs-lookup"><span data-stu-id="63ea3-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="63ea3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63ea3-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63ea3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="63ea3-106">Командлет **Remove-AzBatchCertificate** Удаляет сертификат из указанной пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="63ea3-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="63ea3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63ea3-107">EXAMPLES</span></span>

### <span data-ttu-id="63ea3-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="63ea3-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="63ea3-109">Эта команда удаляет сертификат с указанным отпечатком.</span><span class="sxs-lookup"><span data-stu-id="63ea3-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="63ea3-110">Пример 2: удаление всех активных сертификатов</span><span class="sxs-lookup"><span data-stu-id="63ea3-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="63ea3-111">Эта команда получает все активные сертификаты с помощью командлета Get-AzBatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="63ea3-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="63ea3-112">Команда передает активные сертификаты в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="63ea3-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="63ea3-113">Этот командлет удаляет каждый сертификат.</span><span class="sxs-lookup"><span data-stu-id="63ea3-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="63ea3-114">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="63ea3-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="63ea3-115">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="63ea3-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="63ea3-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63ea3-116">PARAMETERS</span></span>

### <span data-ttu-id="63ea3-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="63ea3-117">-BatchContext</span></span>
<span data-ttu-id="63ea3-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="63ea3-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="63ea3-119">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="63ea3-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="63ea3-120">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="63ea3-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="63ea3-121">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="63ea3-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="63ea3-122">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="63ea3-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="63ea3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ea3-123">-DefaultProfile</span></span>
<span data-ttu-id="63ea3-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63ea3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63ea3-125">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="63ea3-125">-Thumbprint</span></span>
<span data-ttu-id="63ea3-126">Указывает отпечаток сертификата, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="63ea3-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="63ea3-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="63ea3-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="63ea3-128">Указывает алгоритм, используемый для получения параметра *отпечатка* .</span><span class="sxs-lookup"><span data-stu-id="63ea3-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="63ea3-129">В настоящее время единственным допустимым значением является SHA1.</span><span class="sxs-lookup"><span data-stu-id="63ea3-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="63ea3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63ea3-130">-Confirm</span></span>
<span data-ttu-id="63ea3-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63ea3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63ea3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63ea3-132">-WhatIf</span></span>
<span data-ttu-id="63ea3-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63ea3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63ea3-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63ea3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63ea3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ea3-135">CommonParameters</span></span>
<span data-ttu-id="63ea3-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63ea3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ea3-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63ea3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ea3-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63ea3-138">INPUTS</span></span>

### <span data-ttu-id="63ea3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="63ea3-139">System.String</span></span>

### <span data-ttu-id="63ea3-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="63ea3-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="63ea3-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63ea3-141">OUTPUTS</span></span>

### <span data-ttu-id="63ea3-142">System. void</span><span class="sxs-lookup"><span data-stu-id="63ea3-142">System.Void</span></span>

## <span data-ttu-id="63ea3-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="63ea3-143">NOTES</span></span>

## <span data-ttu-id="63ea3-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63ea3-144">RELATED LINKS</span></span>

[<span data-ttu-id="63ea3-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="63ea3-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="63ea3-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="63ea3-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="63ea3-147">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="63ea3-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="63ea3-148">Остановить-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="63ea3-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="63ea3-149">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="63ea3-149">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


