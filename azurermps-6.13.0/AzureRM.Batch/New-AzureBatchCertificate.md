---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: 7038f6c23273153a11aeccc8cbd12fdc6f629c28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563112"
---
# <span data-ttu-id="deeda-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="deeda-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="deeda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="deeda-102">SYNOPSIS</span></span>
<span data-ttu-id="deeda-103">Добавляет сертификат в указанную учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="deeda-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deeda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="deeda-104">SYNTAX</span></span>

### <span data-ttu-id="deeda-105">Файл (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="deeda-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="deeda-106">RawData</span><span class="sxs-lookup"><span data-stu-id="deeda-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="deeda-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="deeda-107">DESCRIPTION</span></span>
<span data-ttu-id="deeda-108">Командлет **New-AzureBatchCertificate** добавляет сертификат для указанной учетной записи пакетной службы Azure.</span><span class="sxs-lookup"><span data-stu-id="deeda-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="deeda-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="deeda-109">EXAMPLES</span></span>

### <span data-ttu-id="deeda-110">Пример 1: Добавление сертификата из файла</span><span class="sxs-lookup"><span data-stu-id="deeda-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="deeda-111">Эта команда добавляет сертификат в указанную учетную запись пакета с помощью файла E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="deeda-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="deeda-112">Пример 2: Добавление сертификата из необработанных данных</span><span class="sxs-lookup"><span data-stu-id="deeda-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="deeda-113">Первая команда считывает данные из файла с именем MyCert. pfx в переменную $RawData.</span><span class="sxs-lookup"><span data-stu-id="deeda-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="deeda-114">Вторая команда добавляет сертификат в указанную учетную запись пакета с помощью необработанных данных, хранящихся в $RawData.</span><span class="sxs-lookup"><span data-stu-id="deeda-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="deeda-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="deeda-115">PARAMETERS</span></span>

### <span data-ttu-id="deeda-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="deeda-116">-BatchContext</span></span>
<span data-ttu-id="deeda-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="deeda-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="deeda-118">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="deeda-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="deeda-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="deeda-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="deeda-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="deeda-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="deeda-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="deeda-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="deeda-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deeda-122">-DefaultProfile</span></span>
<span data-ttu-id="deeda-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="deeda-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deeda-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="deeda-124">-FilePath</span></span>
<span data-ttu-id="deeda-125">Задает путь к файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="deeda-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="deeda-126">Файл сертификата должен быть в формате CER или PFX.</span><span class="sxs-lookup"><span data-stu-id="deeda-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="deeda-127">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="deeda-127">-Password</span></span>
<span data-ttu-id="deeda-128">Указывает пароль для доступа к закрытому ключу сертификата.</span><span class="sxs-lookup"><span data-stu-id="deeda-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="deeda-129">Вы должны указать этот параметр, если вы указали сертификат в формате PFX.</span><span class="sxs-lookup"><span data-stu-id="deeda-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="deeda-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="deeda-130">-RawData</span></span>
<span data-ttu-id="deeda-131">Задает необработанные данные сертификата в формате CER или PFX.</span><span class="sxs-lookup"><span data-stu-id="deeda-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="deeda-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deeda-132">CommonParameters</span></span>
<span data-ttu-id="deeda-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="deeda-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deeda-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deeda-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deeda-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="deeda-135">INPUTS</span></span>

### <span data-ttu-id="deeda-136">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="deeda-136">System.Byte[]</span></span>

### <span data-ttu-id="deeda-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="deeda-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="deeda-138">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="deeda-138">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="deeda-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="deeda-139">OUTPUTS</span></span>

### <span data-ttu-id="deeda-140">System. void</span><span class="sxs-lookup"><span data-stu-id="deeda-140">System.Void</span></span>

## <span data-ttu-id="deeda-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="deeda-141">NOTES</span></span>

## <span data-ttu-id="deeda-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="deeda-142">RELATED LINKS</span></span>

[<span data-ttu-id="deeda-143">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="deeda-143">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="deeda-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="deeda-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="deeda-145">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="deeda-145">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="deeda-146">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="deeda-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


