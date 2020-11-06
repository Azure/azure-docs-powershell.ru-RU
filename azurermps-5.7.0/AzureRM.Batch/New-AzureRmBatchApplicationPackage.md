---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 621aa03b2819815dc538650ea30120c63009235e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568251"
---
# <span data-ttu-id="95050-101">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="95050-101">New-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="95050-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95050-102">SYNOPSIS</span></span>
<span data-ttu-id="95050-103">Создает пакет приложения в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="95050-103">Creates an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95050-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95050-104">SYNTAX</span></span>

### <span data-ttu-id="95050-105">UploadAndActivate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95050-105">UploadAndActivate (Default)</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95050-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="95050-106">ActivateOnly</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95050-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95050-107">DESCRIPTION</span></span>
<span data-ttu-id="95050-108">Командлет **New-AzureRmBatchApplicationPackage** создает пакет приложения в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="95050-108">The **New-AzureRmBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="95050-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95050-109">EXAMPLES</span></span>

### <span data-ttu-id="95050-110">Пример 1: Установка пакета приложения в учетную запись пакета</span><span class="sxs-lookup"><span data-stu-id="95050-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="95050-111">Эта команда создает и активирует версию 1,0 приложения беседа Litware и передает содержимое litware.1.0.zip как содержимое пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="95050-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="95050-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95050-112">PARAMETERS</span></span>

### <span data-ttu-id="95050-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="95050-113">-AccountName</span></span>
<span data-ttu-id="95050-114">Указывает имя пакетной учетной записи, к которой этот командлет добавляет пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="95050-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95050-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="95050-115">-ActivateOnly</span></span>
<span data-ttu-id="95050-116">Указывает на то, что этот командлет активирует пакет приложения, который уже был отправлен.</span><span class="sxs-lookup"><span data-stu-id="95050-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ActivateOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95050-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="95050-117">-ApplicationId</span></span>
<span data-ttu-id="95050-118">Указывает идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="95050-118">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95050-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="95050-119">-ApplicationVersion</span></span>
<span data-ttu-id="95050-120">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="95050-120">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95050-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95050-121">-DefaultProfile</span></span>
<span data-ttu-id="95050-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95050-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95050-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="95050-123">-FilePath</span></span>
<span data-ttu-id="95050-124">Указывает файл, который нужно отправить как двоичный файл пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="95050-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: String
Parameter Sets: UploadAndActivate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95050-125">-Format</span><span class="sxs-lookup"><span data-stu-id="95050-125">-Format</span></span>
<span data-ttu-id="95050-126">Задает формат двоичного файла пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="95050-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95050-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95050-127">-ResourceGroupName</span></span>
<span data-ttu-id="95050-128">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="95050-128">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95050-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95050-129">CommonParameters</span></span>
<span data-ttu-id="95050-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95050-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95050-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95050-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95050-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95050-132">INPUTS</span></span>

### <span data-ttu-id="95050-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="95050-133">None</span></span>
<span data-ttu-id="95050-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="95050-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95050-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95050-135">OUTPUTS</span></span>

### <span data-ttu-id="95050-136">Microsoft.Azure.Commands.BatCH. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="95050-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="95050-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="95050-137">NOTES</span></span>

## <span data-ttu-id="95050-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95050-138">RELATED LINKS</span></span>

[<span data-ttu-id="95050-139">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="95050-139">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="95050-140">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="95050-140">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="95050-141">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="95050-141">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="95050-142">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="95050-142">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="95050-143">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="95050-143">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="95050-144">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="95050-144">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


