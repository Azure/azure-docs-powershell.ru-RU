---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: fc23c99cabe76834204f2fac1f3c18ae7eea1df0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066915"
---
# <span data-ttu-id="198c3-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="198c3-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="198c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="198c3-102">SYNOPSIS</span></span>
<span data-ttu-id="198c3-103">Создает пакет приложения в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="198c3-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="198c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="198c3-104">SYNTAX</span></span>

### <span data-ttu-id="198c3-105">UploadAndActivate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="198c3-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="198c3-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="198c3-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="198c3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="198c3-107">DESCRIPTION</span></span>
<span data-ttu-id="198c3-108">Командлет **New-AzBatchApplicationPackage** создает пакет приложения в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="198c3-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="198c3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="198c3-109">EXAMPLES</span></span>

### <span data-ttu-id="198c3-110">Пример 1: Установка пакета приложения в учетную запись пакета</span><span class="sxs-lookup"><span data-stu-id="198c3-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="198c3-111">Эта команда создает и активирует версию 1,0 приложения беседа Litware и передает содержимое litware.1.0.zip как содержимое пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="198c3-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="198c3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="198c3-112">PARAMETERS</span></span>

### <span data-ttu-id="198c3-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="198c3-113">-AccountName</span></span>
<span data-ttu-id="198c3-114">Указывает имя пакетной учетной записи, к которой этот командлет добавляет пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="198c3-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="198c3-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="198c3-115">-ActivateOnly</span></span>
<span data-ttu-id="198c3-116">Указывает на то, что этот командлет активирует пакет приложения, который уже был отправлен.</span><span class="sxs-lookup"><span data-stu-id="198c3-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="198c3-117">-ИмяПриложения</span><span class="sxs-lookup"><span data-stu-id="198c3-117">-ApplicationName</span></span>
<span data-ttu-id="198c3-118">Указывает имя приложения.</span><span class="sxs-lookup"><span data-stu-id="198c3-118">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="198c3-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="198c3-119">-ApplicationVersion</span></span>
<span data-ttu-id="198c3-120">Определяет версию приложения.</span><span class="sxs-lookup"><span data-stu-id="198c3-120">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="198c3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="198c3-121">-DefaultProfile</span></span>
<span data-ttu-id="198c3-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="198c3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="198c3-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="198c3-123">-FilePath</span></span>
<span data-ttu-id="198c3-124">Указывает файл, который нужно отправить как двоичный файл пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="198c3-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="198c3-125">-Format</span><span class="sxs-lookup"><span data-stu-id="198c3-125">-Format</span></span>
<span data-ttu-id="198c3-126">Задает формат двоичного файла пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="198c3-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="198c3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="198c3-127">-ResourceGroupName</span></span>
<span data-ttu-id="198c3-128">Указывает имя группы ресурсов, которая содержит пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="198c3-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="198c3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="198c3-129">CommonParameters</span></span>
<span data-ttu-id="198c3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="198c3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="198c3-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="198c3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="198c3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="198c3-132">INPUTS</span></span>

### <span data-ttu-id="198c3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="198c3-133">System.String</span></span>

### <span data-ttu-id="198c3-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="198c3-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="198c3-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="198c3-135">OUTPUTS</span></span>

### <span data-ttu-id="198c3-136">Microsoft.Azure.Commands.BatCH. Models. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="198c3-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="198c3-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="198c3-137">NOTES</span></span>

## <span data-ttu-id="198c3-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="198c3-138">RELATED LINKS</span></span>

[<span data-ttu-id="198c3-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="198c3-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="198c3-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="198c3-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="198c3-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="198c3-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="198c3-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="198c3-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="198c3-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="198c3-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="198c3-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="198c3-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


