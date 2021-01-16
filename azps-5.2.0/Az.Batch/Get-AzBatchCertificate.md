---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
ms.openlocfilehash: 26bd35f59ae5e640093c1695e7caf991e1e1e956
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391764"
---
# <span data-ttu-id="636df-101">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="636df-101">Get-AzBatchCertificate</span></span>

## <span data-ttu-id="636df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="636df-102">SYNOPSIS</span></span>
<span data-ttu-id="636df-103">Получает сертификаты в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="636df-103">Gets the certificates in a Batch account.</span></span>

## <span data-ttu-id="636df-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="636df-104">SYNTAX</span></span>

### <span data-ttu-id="636df-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="636df-105">ODataFilter (Default)</span></span>
```
Get-AzBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="636df-106">Thumbprint</span><span class="sxs-lookup"><span data-stu-id="636df-106">Thumbprint</span></span>
```
Get-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="636df-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="636df-107">DESCRIPTION</span></span>
<span data-ttu-id="636df-108">Cmdlet **Get-AzBatchCertificate** получает сертификаты в учетной записи Azure Batch, задаваемой параметром *BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="636df-108">The **Get-AzBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="636df-109">Чтобы получить определенный сертификат, укажите параметры *ThumbprintAlgorithm* и *Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="636df-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="636df-110">Укажите *параметр Filter,* чтобы получить сертификаты, которые соответствуют фильтру OData.</span><span class="sxs-lookup"><span data-stu-id="636df-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="636df-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="636df-111">EXAMPLES</span></span>

### <span data-ttu-id="636df-112">Пример 1. Получить сертификат по thumbprint</span><span class="sxs-lookup"><span data-stu-id="636df-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
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

<span data-ttu-id="636df-113">Эта команда получает один сертификат с указанным эскизом.</span><span class="sxs-lookup"><span data-stu-id="636df-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="636df-114">Алгоритм печати сертификата имеет алгоритм sha1.</span><span class="sxs-lookup"><span data-stu-id="636df-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="636df-115">Пример 2. Получить отфильтрованные сертификаты</span><span class="sxs-lookup"><span data-stu-id="636df-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
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

<span data-ttu-id="636df-116">Эта команда получает все сертификаты в активном состоянии из учетной записи пакета.</span><span class="sxs-lookup"><span data-stu-id="636df-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="636df-117">Параметр *Filter* определяет состояние.</span><span class="sxs-lookup"><span data-stu-id="636df-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="636df-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="636df-118">PARAMETERS</span></span>

### <span data-ttu-id="636df-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="636df-119">-BatchContext</span></span>
<span data-ttu-id="636df-120">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="636df-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="636df-121">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="636df-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="636df-122">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="636df-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="636df-123">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="636df-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="636df-124">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="636df-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="636df-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="636df-125">-DefaultProfile</span></span>
<span data-ttu-id="636df-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="636df-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="636df-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="636df-127">-Filter</span></span>
<span data-ttu-id="636df-128">Указывает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="636df-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="636df-129">Если этот параметр задан, этот командлет получает сертификаты, которые соответствуют фильтру.</span><span class="sxs-lookup"><span data-stu-id="636df-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

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

### <span data-ttu-id="636df-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="636df-130">-MaxCount</span></span>
<span data-ttu-id="636df-131">Указывает максимальное количество сертификатов, которые нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="636df-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="636df-132">Если указать нулевое (ноль) или меньшее значение, для cmdlet не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="636df-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="636df-133">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="636df-133">The default value is 1000.</span></span>

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

### <span data-ttu-id="636df-134">-Select</span><span class="sxs-lookup"><span data-stu-id="636df-134">-Select</span></span>
<span data-ttu-id="636df-135">Указывает предложение выбора OData.</span><span class="sxs-lookup"><span data-stu-id="636df-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="636df-136">Укажите значение этого параметра, чтобы получить определенные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="636df-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="636df-137">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="636df-137">-Thumbprint</span></span>
<span data-ttu-id="636df-138">Определяет эскиз сертификата, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="636df-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="636df-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="636df-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="636df-140">Алгоритм, используемый для получения *параметра Thumbprint.*</span><span class="sxs-lookup"><span data-stu-id="636df-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="636df-141">В настоящее время допустимым значением является только sha1.</span><span class="sxs-lookup"><span data-stu-id="636df-141">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="636df-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="636df-142">CommonParameters</span></span>
<span data-ttu-id="636df-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="636df-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="636df-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="636df-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="636df-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="636df-145">INPUTS</span></span>

### <span data-ttu-id="636df-146">System.String</span><span class="sxs-lookup"><span data-stu-id="636df-146">System.String</span></span>

### <span data-ttu-id="636df-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="636df-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="636df-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="636df-148">OUTPUTS</span></span>

### <span data-ttu-id="636df-149">Microsoft.Azure.Commands.Batch. Models.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="636df-149">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="636df-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="636df-150">NOTES</span></span>

## <span data-ttu-id="636df-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="636df-151">RELATED LINKS</span></span>

[<span data-ttu-id="636df-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="636df-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="636df-153">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="636df-153">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="636df-154">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="636df-154">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="636df-155">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="636df-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
