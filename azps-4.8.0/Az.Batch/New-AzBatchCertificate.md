---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079198"
---
# <span data-ttu-id="d12ef-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d12ef-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="d12ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d12ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d12ef-103">Добавляет сертификат в указанную учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="d12ef-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="d12ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d12ef-104">SYNTAX</span></span>

### <span data-ttu-id="d12ef-105">Файл (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d12ef-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d12ef-106">RawData</span><span class="sxs-lookup"><span data-stu-id="d12ef-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d12ef-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d12ef-107">DESCRIPTION</span></span>
<span data-ttu-id="d12ef-108">Командлет **New-AzBatchCertificate** добавляет сертификат для указанной учетной записи пакетной службы Azure.</span><span class="sxs-lookup"><span data-stu-id="d12ef-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="d12ef-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d12ef-109">EXAMPLES</span></span>

### <span data-ttu-id="d12ef-110">Пример 1: Добавление сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="d12ef-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="d12ef-111">Эта команда добавляет сертификат в указанную учетную запись пакета с помощью файла E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="d12ef-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="d12ef-112">Пример 2: Добавление сертификата из необработанных данных</span><span class="sxs-lookup"><span data-stu-id="d12ef-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="d12ef-113">Первая команда считывает данные из файла с именем MyCert. pfx в переменную $RawData.</span><span class="sxs-lookup"><span data-stu-id="d12ef-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="d12ef-114">Вторая команда добавляет сертификат в указанную учетную запись пакета с помощью необработанных данных, хранящихся в $RawData.</span><span class="sxs-lookup"><span data-stu-id="d12ef-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="d12ef-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d12ef-115">PARAMETERS</span></span>

### <span data-ttu-id="d12ef-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d12ef-116">-BatchContext</span></span>
<span data-ttu-id="d12ef-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="d12ef-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d12ef-118">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="d12ef-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d12ef-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="d12ef-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d12ef-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="d12ef-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d12ef-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d12ef-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d12ef-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d12ef-122">-DefaultProfile</span></span>
<span data-ttu-id="d12ef-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d12ef-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d12ef-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d12ef-124">-FilePath</span></span>
<span data-ttu-id="d12ef-125">Задает путь к файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="d12ef-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="d12ef-126">Файл сертификата должен быть в формате CER или PFX.</span><span class="sxs-lookup"><span data-stu-id="d12ef-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="d12ef-127">-Видах</span><span class="sxs-lookup"><span data-stu-id="d12ef-127">-Kind</span></span>
<span data-ttu-id="d12ef-128">Создаваемый сертификат.</span><span class="sxs-lookup"><span data-stu-id="d12ef-128">The kind of certificate to create.</span></span> <span data-ttu-id="d12ef-129">Если этот параметр не указан, предполагается, что все сертификаты без пароля — CER, а все сертификаты с паролем — PFX.</span><span class="sxs-lookup"><span data-stu-id="d12ef-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

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

### <span data-ttu-id="d12ef-130">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="d12ef-130">-Password</span></span>
<span data-ttu-id="d12ef-131">Указывает пароль для доступа к закрытому ключу сертификата.</span><span class="sxs-lookup"><span data-stu-id="d12ef-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="d12ef-132">Вы должны указать этот параметр, если вы указали сертификат в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="d12ef-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="d12ef-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="d12ef-133">-RawData</span></span>
<span data-ttu-id="d12ef-134">Задает необработанные данные сертификата в формате CER или PFX.</span><span class="sxs-lookup"><span data-stu-id="d12ef-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="d12ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d12ef-135">CommonParameters</span></span>
<span data-ttu-id="d12ef-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d12ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d12ef-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d12ef-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d12ef-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d12ef-138">INPUTS</span></span>

### <span data-ttu-id="d12ef-139">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="d12ef-139">System.Byte[]</span></span>

### <span data-ttu-id="d12ef-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d12ef-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d12ef-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d12ef-141">OUTPUTS</span></span>

### <span data-ttu-id="d12ef-142">System. void</span><span class="sxs-lookup"><span data-stu-id="d12ef-142">System.Void</span></span>

## <span data-ttu-id="d12ef-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="d12ef-143">NOTES</span></span>

## <span data-ttu-id="d12ef-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d12ef-144">RELATED LINKS</span></span>

[<span data-ttu-id="d12ef-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d12ef-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="d12ef-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="d12ef-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d12ef-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d12ef-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="d12ef-148">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="d12ef-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)