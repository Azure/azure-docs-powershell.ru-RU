---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402791"
---
# <span data-ttu-id="c09f0-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c09f0-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="c09f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c09f0-102">SYNOPSIS</span></span>
<span data-ttu-id="c09f0-103">Перемещает или переименовыв файл или папку в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c09f0-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c09f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c09f0-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c09f0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c09f0-105">DESCRIPTION</span></span>
<span data-ttu-id="c09f0-106">Для перемещения или переименования файла или папки в магазине Data Lake Store будет перемещаться или переименовывана **cmdataLakeStoreItem.**</span><span class="sxs-lookup"><span data-stu-id="c09f0-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c09f0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c09f0-107">EXAMPLES</span></span>

### <span data-ttu-id="c09f0-108">Пример 1. Перемещение и переименование элемента</span><span class="sxs-lookup"><span data-stu-id="c09f0-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="c09f0-109">Эта команда переименовает элемент File.txt RenamedFile.txt и перемещает его в другую папку.</span><span class="sxs-lookup"><span data-stu-id="c09f0-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="c09f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c09f0-110">PARAMETERS</span></span>

### <span data-ttu-id="c09f0-111">-Account</span><span class="sxs-lookup"><span data-stu-id="c09f0-111">-Account</span></span>
<span data-ttu-id="c09f0-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c09f0-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c09f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c09f0-113">-DefaultProfile</span></span>
<span data-ttu-id="c09f0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c09f0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c09f0-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="c09f0-115">-Destination</span></span>
<span data-ttu-id="c09f0-116">Путь к магазину данных для перемещения элемента, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="c09f0-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c09f0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c09f0-117">-Force</span></span>
<span data-ttu-id="c09f0-118">Указывает на то, что данной операцией можно переписать файл назначения, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="c09f0-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="c09f0-119">-Path</span><span class="sxs-lookup"><span data-stu-id="c09f0-119">-Path</span></span>
<span data-ttu-id="c09f0-120">Путь к элементу, который нужно переместить или переименовать, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="c09f0-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c09f0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c09f0-121">-Confirm</span></span>
<span data-ttu-id="c09f0-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c09f0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c09f0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c09f0-123">-WhatIf</span></span>
<span data-ttu-id="c09f0-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c09f0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c09f0-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c09f0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c09f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c09f0-126">CommonParameters</span></span>
<span data-ttu-id="c09f0-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c09f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c09f0-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c09f0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c09f0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c09f0-129">INPUTS</span></span>

### <span data-ttu-id="c09f0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c09f0-130">System.String</span></span>

### <span data-ttu-id="c09f0-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c09f0-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c09f0-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c09f0-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c09f0-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c09f0-133">OUTPUTS</span></span>

### <span data-ttu-id="c09f0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c09f0-134">System.String</span></span>

## <span data-ttu-id="c09f0-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c09f0-135">NOTES</span></span>

## <span data-ttu-id="c09f0-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c09f0-136">RELATED LINKS</span></span>

[<span data-ttu-id="c09f0-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c09f0-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="c09f0-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c09f0-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="c09f0-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c09f0-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="c09f0-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c09f0-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="c09f0-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c09f0-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="c09f0-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c09f0-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)

