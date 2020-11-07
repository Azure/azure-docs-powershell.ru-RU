---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5d975e70423e03e3ab17bbfc8631ff8e1f892cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733744"
---
# <span data-ttu-id="b07e4-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="b07e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b07e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b07e4-103">Перемещение или переименование файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b07e4-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b07e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b07e4-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b07e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b07e4-105">DESCRIPTION</span></span>
<span data-ttu-id="b07e4-106">Командлет **Move-AzureRmDataLakeStoreItem** перемещает или переименовывает файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b07e4-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b07e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b07e4-107">EXAMPLES</span></span>

### <span data-ttu-id="b07e4-108">Пример 1: перемещение и переименование элемента</span><span class="sxs-lookup"><span data-stu-id="b07e4-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="b07e4-109">Эта команда переименовывает элемент File.txt в RenamedFile.txt и перемещает его в другую папку.</span><span class="sxs-lookup"><span data-stu-id="b07e4-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="b07e4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b07e4-110">PARAMETERS</span></span>

### <span data-ttu-id="b07e4-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b07e4-111">-Account</span></span>
<span data-ttu-id="b07e4-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b07e4-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07e4-113">-Destination</span><span class="sxs-lookup"><span data-stu-id="b07e4-113">-Destination</span></span>
<span data-ttu-id="b07e4-114">Указывает путь к Data Lake Store, куда нужно переместить элемент, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="b07e4-114">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07e4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b07e4-115">-Force</span></span>
<span data-ttu-id="b07e4-116">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="b07e4-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07e4-117">-Path</span><span class="sxs-lookup"><span data-stu-id="b07e4-117">-Path</span></span>
<span data-ttu-id="b07e4-118">Указывает путь к Data Lake Store для элемента, который нужно переместить или переименовать, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="b07e4-118">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07e4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b07e4-119">-Confirm</span></span>
<span data-ttu-id="b07e4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b07e4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b07e4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b07e4-121">-WhatIf</span></span>
<span data-ttu-id="b07e4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b07e4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b07e4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b07e4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b07e4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07e4-124">-DefaultProfile</span></span>
<span data-ttu-id="b07e4-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b07e4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b07e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07e4-126">CommonParameters</span></span>
<span data-ttu-id="b07e4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b07e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07e4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b07e4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07e4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b07e4-129">INPUTS</span></span>

## <span data-ttu-id="b07e4-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b07e4-130">OUTPUTS</span></span>

### <span data-ttu-id="b07e4-131">подстрок</span><span class="sxs-lookup"><span data-stu-id="b07e4-131">string</span></span>
<span data-ttu-id="b07e4-132">Полный путь к перемещенному файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="b07e4-132">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="b07e4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b07e4-133">NOTES</span></span>

## <span data-ttu-id="b07e4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b07e4-134">RELATED LINKS</span></span>

[<span data-ttu-id="b07e4-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b07e4-136">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b07e4-137">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b07e4-138">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b07e4-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="b07e4-140">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b07e4-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


