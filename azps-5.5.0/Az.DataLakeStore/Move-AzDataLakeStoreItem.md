---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228713"
---
# <span data-ttu-id="8c776-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c776-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="8c776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c776-102">SYNOPSIS</span></span>
<span data-ttu-id="8c776-103">Перемещает или переименовыв файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8c776-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8c776-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c776-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c776-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c776-105">DESCRIPTION</span></span>
<span data-ttu-id="8c776-106">Для перемещения или переименования файла или папки в магазине Data Lake Store будет перемещаться или переименововывана **cmdataLakeStoreItem.**</span><span class="sxs-lookup"><span data-stu-id="8c776-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8c776-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c776-107">EXAMPLES</span></span>

### <span data-ttu-id="8c776-108">Пример 1. Перемещение и переименование элемента</span><span class="sxs-lookup"><span data-stu-id="8c776-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="8c776-109">Эта команда переименовает элемент File.txt RenamedFile.txt и перемещает его в другую папку.</span><span class="sxs-lookup"><span data-stu-id="8c776-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="8c776-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c776-110">PARAMETERS</span></span>

### <span data-ttu-id="8c776-111">-Account</span><span class="sxs-lookup"><span data-stu-id="8c776-111">-Account</span></span>
<span data-ttu-id="8c776-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8c776-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8c776-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c776-113">-DefaultProfile</span></span>
<span data-ttu-id="8c776-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c776-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c776-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="8c776-115">-Destination</span></span>
<span data-ttu-id="8c776-116">Путь к магазину данных для перемещения элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="8c776-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8c776-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8c776-117">-Force</span></span>
<span data-ttu-id="8c776-118">Указывает на то, что данной операцией можно переписать файл назначения, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="8c776-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="8c776-119">-Path</span><span class="sxs-lookup"><span data-stu-id="8c776-119">-Path</span></span>
<span data-ttu-id="8c776-120">Путь к элементу, который нужно переместить или переименовать, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="8c776-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8c776-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c776-121">-Confirm</span></span>
<span data-ttu-id="8c776-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c776-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c776-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c776-123">-WhatIf</span></span>
<span data-ttu-id="8c776-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c776-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c776-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8c776-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c776-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c776-126">CommonParameters</span></span>
<span data-ttu-id="8c776-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c776-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c776-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c776-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c776-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c776-129">INPUTS</span></span>

### <span data-ttu-id="8c776-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8c776-130">System.String</span></span>

### <span data-ttu-id="8c776-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="8c776-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="8c776-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c776-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8c776-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c776-133">OUTPUTS</span></span>

### <span data-ttu-id="8c776-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8c776-134">System.String</span></span>

## <span data-ttu-id="8c776-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c776-135">NOTES</span></span>

## <span data-ttu-id="8c776-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c776-136">RELATED LINKS</span></span>

[<span data-ttu-id="8c776-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c776-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="8c776-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c776-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="8c776-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c776-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="8c776-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c776-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="8c776-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c776-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="8c776-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8c776-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


