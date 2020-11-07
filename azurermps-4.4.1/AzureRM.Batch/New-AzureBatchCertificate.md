---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: d567c176580cba0659d6c88c919ffa34cad393ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735066"
---
# <span data-ttu-id="00505-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="00505-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="00505-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00505-102">SYNOPSIS</span></span>
<span data-ttu-id="00505-103">Добавляет сертификат в указанную учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="00505-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00505-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00505-104">SYNTAX</span></span>

### <span data-ttu-id="00505-105">Файл (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00505-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00505-106">RawData</span><span class="sxs-lookup"><span data-stu-id="00505-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00505-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00505-107">DESCRIPTION</span></span>
<span data-ttu-id="00505-108">Командлет **New-AzureBatchCertificate** добавляет сертификат для указанной учетной записи пакетной службы Azure.</span><span class="sxs-lookup"><span data-stu-id="00505-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="00505-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00505-109">EXAMPLES</span></span>

### <span data-ttu-id="00505-110">Пример 1: Добавление сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="00505-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="00505-111">Эта команда добавляет сертификат в указанную учетную запись пакета с помощью файла E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="00505-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="00505-112">Пример 2: Добавление сертификата из необработанных данных</span><span class="sxs-lookup"><span data-stu-id="00505-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="00505-113">Первая команда считывает данные из файла с именем MyCert. pfx в переменную $RawData.</span><span class="sxs-lookup"><span data-stu-id="00505-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="00505-114">Вторая команда добавляет сертификат в указанную учетную запись пакета с помощью необработанных данных, хранящихся в $RawData.</span><span class="sxs-lookup"><span data-stu-id="00505-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="00505-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00505-115">PARAMETERS</span></span>

### <span data-ttu-id="00505-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="00505-116">-BatchContext</span></span>
<span data-ttu-id="00505-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="00505-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="00505-118">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="00505-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="00505-119">-FilePath</span><span class="sxs-lookup"><span data-stu-id="00505-119">-FilePath</span></span>
<span data-ttu-id="00505-120">Задает путь к файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="00505-120">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="00505-121">Файл сертификата должен быть в формате CER или PFX.</span><span class="sxs-lookup"><span data-stu-id="00505-121">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="00505-122">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="00505-122">-Password</span></span>
<span data-ttu-id="00505-123">Указывает пароль для доступа к закрытому ключу сертификата.</span><span class="sxs-lookup"><span data-stu-id="00505-123">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="00505-124">Вы должны указать этот параметр, если вы указали сертификат в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="00505-124">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="00505-125">-RawData</span><span class="sxs-lookup"><span data-stu-id="00505-125">-RawData</span></span>
<span data-ttu-id="00505-126">Задает необработанные данные сертификата в формате CER или PFX.</span><span class="sxs-lookup"><span data-stu-id="00505-126">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="00505-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00505-127">-DefaultProfile</span></span>
<span data-ttu-id="00505-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00505-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00505-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00505-129">CommonParameters</span></span>
<span data-ttu-id="00505-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00505-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00505-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00505-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00505-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00505-132">INPUTS</span></span>

### <span data-ttu-id="00505-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="00505-133">BatchAccountContext</span></span>
<span data-ttu-id="00505-134">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="00505-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="00505-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="00505-135">Byte[]</span></span>
<span data-ttu-id="00505-136">Параметр "RawData" принимает значение типа Byte [] из конвейера.</span><span class="sxs-lookup"><span data-stu-id="00505-136">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="00505-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00505-137">OUTPUTS</span></span>

## <span data-ttu-id="00505-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="00505-138">NOTES</span></span>

## <span data-ttu-id="00505-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00505-139">RELATED LINKS</span></span>

[<span data-ttu-id="00505-140">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="00505-140">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="00505-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="00505-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="00505-142">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="00505-142">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="00505-143">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="00505-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


