---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: 4ef75210204cddc8de2aa129f0997cb4f12269b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972200"
---
# <span data-ttu-id="d0e42-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d0e42-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="d0e42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0e42-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e42-103">Добавляет сертификат в указанную учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="d0e42-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="d0e42-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d0e42-104">SYNTAX</span></span>

### <span data-ttu-id="d0e42-105">Файл (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0e42-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0e42-106">RawData</span><span class="sxs-lookup"><span data-stu-id="d0e42-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0e42-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0e42-107">DESCRIPTION</span></span>
<span data-ttu-id="d0e42-108">**Новый-AzBatchCertificate** добавляет сертификат к указанной учетной записи Пакета Azure.</span><span class="sxs-lookup"><span data-stu-id="d0e42-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="d0e42-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d0e42-109">EXAMPLES</span></span>

### <span data-ttu-id="d0e42-110">Пример 1. Добавление сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="d0e42-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="d0e42-111">Эта команда добавляет сертификат в указанную учетную запись пакета с помощью файла E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="d0e42-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="d0e42-112">Пример 2. Добавление сертификата из необработанных данных</span><span class="sxs-lookup"><span data-stu-id="d0e42-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="d0e42-113">Первая команда читает данные из файла MyCert.pfx в переменную $RawData.</span><span class="sxs-lookup"><span data-stu-id="d0e42-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="d0e42-114">Вторая команда добавляет сертификат в указанную учетную запись пакета с использованием необработанных данных, хранимых в $RawData.</span><span class="sxs-lookup"><span data-stu-id="d0e42-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="d0e42-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0e42-115">PARAMETERS</span></span>

### <span data-ttu-id="d0e42-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d0e42-116">-BatchContext</span></span>
<span data-ttu-id="d0e42-117">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="d0e42-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d0e42-118">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d0e42-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d0e42-119">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="d0e42-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d0e42-120">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d0e42-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d0e42-121">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d0e42-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d0e42-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e42-122">-DefaultProfile</span></span>
<span data-ttu-id="d0e42-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0e42-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0e42-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d0e42-124">-FilePath</span></span>
<span data-ttu-id="d0e42-125">Путь к файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="d0e42-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="d0e42-126">Файл сертификата должен иметь формат CER или PFX.</span><span class="sxs-lookup"><span data-stu-id="d0e42-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0e42-127">-Kind</span><span class="sxs-lookup"><span data-stu-id="d0e42-127">-Kind</span></span>
<span data-ttu-id="d0e42-128">Тип создаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="d0e42-128">The kind of certificate to create.</span></span> <span data-ttu-id="d0e42-129">Если этот не задан, предполагается, что все сертификаты без пароля являются CER, а все сертификаты с паролем — PFX.</span><span class="sxs-lookup"><span data-stu-id="d0e42-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0e42-130">-Password</span><span class="sxs-lookup"><span data-stu-id="d0e42-130">-Password</span></span>
<span data-ttu-id="d0e42-131">Пароль для доступа к закрытому ключу сертификата.</span><span class="sxs-lookup"><span data-stu-id="d0e42-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="d0e42-132">Этот параметр необходимо указать, если сертификат указан в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="d0e42-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0e42-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="d0e42-133">-RawData</span></span>
<span data-ttu-id="d0e42-134">Определяет необработанные данные сертификата в формате CER или PFX.</span><span class="sxs-lookup"><span data-stu-id="d0e42-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e42-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e42-135">CommonParameters</span></span>
<span data-ttu-id="d0e42-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e42-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e42-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0e42-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e42-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0e42-138">INPUTS</span></span>

### <span data-ttu-id="d0e42-139">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="d0e42-139">System.Byte[]</span></span>

### <span data-ttu-id="d0e42-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d0e42-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d0e42-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d0e42-141">OUTPUTS</span></span>

### <span data-ttu-id="d0e42-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="d0e42-142">System.Void</span></span>

## <span data-ttu-id="d0e42-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d0e42-143">NOTES</span></span>

## <span data-ttu-id="d0e42-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0e42-144">RELATED LINKS</span></span>

[<span data-ttu-id="d0e42-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d0e42-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="d0e42-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d0e42-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d0e42-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d0e42-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="d0e42-148">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="d0e42-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
