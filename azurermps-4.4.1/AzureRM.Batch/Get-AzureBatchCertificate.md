---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchCertificate.md
ms.openlocfilehash: 84b70c119cc91bbcfd468c84818f0b1d7856cae3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569720"
---
# <span data-ttu-id="c3fd5-101">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c3fd5-101">Get-AzureBatchCertificate</span></span>

## <span data-ttu-id="c3fd5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fd5-103">Возвращает сертификаты в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-103">Gets the certificates in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3fd5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3fd5-104">SYNTAX</span></span>

### <span data-ttu-id="c3fd5-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c3fd5-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3fd5-106">Отпечаток</span><span class="sxs-lookup"><span data-stu-id="c3fd5-106">Thumbprint</span></span>
```
Get-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3fd5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3fd5-107">DESCRIPTION</span></span>
<span data-ttu-id="c3fd5-108">Командлет **Get-AzureBatchCertificate** получает сертификаты из пакетной учетной записи Azure, которую указывает параметр *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="c3fd5-108">The **Get-AzureBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="c3fd5-109">Чтобы получить определенный сертификат, укажите параметры *ThumbprintAlgorithm* и *Thumbprint* .</span><span class="sxs-lookup"><span data-stu-id="c3fd5-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="c3fd5-110">Укажите параметр *фильтра* , чтобы получить сертификаты, соответствующие фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="c3fd5-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="c3fd5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3fd5-111">EXAMPLES</span></span>

### <span data-ttu-id="c3fd5-112">Пример 1: получение сертификата по отпечатку</span><span class="sxs-lookup"><span data-stu-id="c3fd5-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzureBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=C1E494A415149C5F211C4778B52F2E834A07247
C) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="c3fd5-113">Эта команда возвращает один сертификат с указанным отпечатком.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="c3fd5-114">Алгоритм отпечатка сертификата — SHA1.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="c3fd5-115">Пример 2: получение отфильтрованных сертификатов</span><span class="sxs-lookup"><span data-stu-id="c3fd5-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
Thumbprint                  : 025b351b087a084c5067f5e71eff8591970323f9
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=025b351b087a084c5067f5e71eff8591970323f9) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:17 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAyMB4XDTE1MTAwMjE2MjkxNFoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDIwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAJxagvVrlnKfv6hfzSiFJUkdGkPjC3tFiKebK6IaeHzesFdFfupXUE
wT0xOWh9xwa3OVkPECEc/u1sw3iVX/J4AODiwzmOWutoVRpWjxGFpgw9+dPvXMjs/Ue7JL7ag3siHs5EcarW91qKbgtko6i/r4emaRyk60U93TrbWQAWJ9AgMBAAGjS
zBJMEcGA1UdAQRAMD6AEAdqsOpyeXF/uDe7ZGKeez+hGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMoIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAA4GBAC0MaAem
6ByyURFvGnFZyjEepjXC5wcaGq+gguDFe8rG88ceig1ZqewdcmC1y4p05uBhbmETbYVWzJarNsHYq2LTihi4t2J4jt2YVYz/IRdUB82iaFFbJRSPrN+6xD3KM2lve5N
4OjtlZAdiXiSUYFf3I6ypberUsAdba3QQajCN
DeleteCertificateError      : 

Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=c1e494a415149c5f211c4778b52f2e834a07247c) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="c3fd5-116">Эта команда возвращает все сертификаты в активном состоянии из пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="c3fd5-117">Параметр *Filter* задает состояние.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="c3fd5-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3fd5-118">PARAMETERS</span></span>

### <span data-ttu-id="c3fd5-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c3fd5-119">-BatchContext</span></span>
<span data-ttu-id="c3fd5-120">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c3fd5-121">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c3fd5-122">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="c3fd5-122">-Filter</span></span>
<span data-ttu-id="c3fd5-123">Задает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-123">Specifies an OData filter clause.</span></span>
<span data-ttu-id="c3fd5-124">Если указать этот параметр, этот командлет получает сертификаты, соответствующие фильтру.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-124">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fd5-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c3fd5-125">-MaxCount</span></span>
<span data-ttu-id="c3fd5-126">Задает максимальное количество возвращаемых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-126">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="c3fd5-127">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-127">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="c3fd5-128">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-128">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fd5-129">-SELECT</span><span class="sxs-lookup"><span data-stu-id="c3fd5-129">-Select</span></span>
<span data-ttu-id="c3fd5-130">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-130">Specifies an OData select clause.</span></span>
<span data-ttu-id="c3fd5-131">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-131">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3fd5-132">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="c3fd5-132">-Thumbprint</span></span>
<span data-ttu-id="c3fd5-133">Указывает отпечаток сертификата, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-133">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fd5-134">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c3fd5-134">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="c3fd5-135">Указывает алгоритм, используемый для получения параметра *отпечатка* .</span><span class="sxs-lookup"><span data-stu-id="c3fd5-135">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="c3fd5-136">В настоящее время единственным допустимым значением является SHA1.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-136">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3fd5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3fd5-137">-DefaultProfile</span></span>
<span data-ttu-id="c3fd5-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3fd5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fd5-139">CommonParameters</span></span>
<span data-ttu-id="c3fd5-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fd5-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3fd5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fd5-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3fd5-142">INPUTS</span></span>

### <span data-ttu-id="c3fd5-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c3fd5-143">BatchAccountContext</span></span>
<span data-ttu-id="c3fd5-144">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c3fd5-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="c3fd5-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3fd5-145">OUTPUTS</span></span>

### <span data-ttu-id="c3fd5-146">Microsoft.Azure.Commands.BatCH. Models. PSCertificate</span><span class="sxs-lookup"><span data-stu-id="c3fd5-146">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="c3fd5-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3fd5-147">NOTES</span></span>

## <span data-ttu-id="c3fd5-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3fd5-148">RELATED LINKS</span></span>

[<span data-ttu-id="c3fd5-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c3fd5-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c3fd5-150">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c3fd5-150">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="c3fd5-151">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="c3fd5-151">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="c3fd5-152">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="c3fd5-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


