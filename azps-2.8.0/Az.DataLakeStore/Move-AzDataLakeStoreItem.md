---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: 8a8cc4d60bfba73b9cbcc9d323b063bff87f8a2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721298"
---
# <span data-ttu-id="b460f-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b460f-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="b460f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b460f-102">SYNOPSIS</span></span>
<span data-ttu-id="b460f-103">Перемещение или переименование файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b460f-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b460f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b460f-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b460f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b460f-105">DESCRIPTION</span></span>
<span data-ttu-id="b460f-106">Командлет **Move-AzDataLakeStoreItem** перемещает или переименовывает файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b460f-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b460f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b460f-107">EXAMPLES</span></span>

### <span data-ttu-id="b460f-108">Пример 1: перемещение и переименование элемента</span><span class="sxs-lookup"><span data-stu-id="b460f-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="b460f-109">Эта команда переименовывает элемент File.txt в RenamedFile.txt и перемещает его в другую папку.</span><span class="sxs-lookup"><span data-stu-id="b460f-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="b460f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b460f-110">PARAMETERS</span></span>

### <span data-ttu-id="b460f-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b460f-111">-Account</span></span>
<span data-ttu-id="b460f-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b460f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b460f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b460f-113">-DefaultProfile</span></span>
<span data-ttu-id="b460f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b460f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b460f-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="b460f-115">-Destination</span></span>
<span data-ttu-id="b460f-116">Указывает путь к Data Lake Store, куда нужно переместить элемент, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="b460f-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b460f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b460f-117">-Force</span></span>
<span data-ttu-id="b460f-118">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="b460f-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="b460f-119">-Path</span><span class="sxs-lookup"><span data-stu-id="b460f-119">-Path</span></span>
<span data-ttu-id="b460f-120">Указывает путь к Data Lake Store для элемента, который нужно переместить или переименовать, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="b460f-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b460f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b460f-121">-Confirm</span></span>
<span data-ttu-id="b460f-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b460f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b460f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b460f-123">-WhatIf</span></span>
<span data-ttu-id="b460f-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b460f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b460f-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b460f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b460f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b460f-126">CommonParameters</span></span>
<span data-ttu-id="b460f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b460f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b460f-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b460f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b460f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b460f-129">INPUTS</span></span>

### <span data-ttu-id="b460f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b460f-130">System.String</span></span>

### <span data-ttu-id="b460f-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b460f-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b460f-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b460f-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b460f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b460f-133">OUTPUTS</span></span>

### <span data-ttu-id="b460f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b460f-134">System.String</span></span>

## <span data-ttu-id="b460f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="b460f-135">NOTES</span></span>

## <span data-ttu-id="b460f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b460f-136">RELATED LINKS</span></span>

[<span data-ttu-id="b460f-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b460f-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="b460f-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b460f-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="b460f-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b460f-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="b460f-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b460f-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="b460f-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b460f-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="b460f-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="b460f-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


