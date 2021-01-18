---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504583"
---
# <span data-ttu-id="47b9a-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="47b9a-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="47b9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="47b9a-103">Соединяет один или несколько файлов, чтобы создать один файл в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="47b9a-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="47b9a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47b9a-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47b9a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="47b9a-106">**Cmdlet Join-AzDataLakeStoreItem** соединяет один или несколько файлов, чтобы создать один файл в магазине Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="47b9a-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="47b9a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47b9a-107">EXAMPLES</span></span>

### <span data-ttu-id="47b9a-108">Пример 1. Соединить два пункта</span><span class="sxs-lookup"><span data-stu-id="47b9a-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="47b9a-109">Эта команда соединяет File01.txt File02.txt, чтобы создать файл CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="47b9a-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="47b9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47b9a-110">PARAMETERS</span></span>

### <span data-ttu-id="47b9a-111">-Account</span><span class="sxs-lookup"><span data-stu-id="47b9a-111">-Account</span></span>
<span data-ttu-id="47b9a-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="47b9a-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="47b9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b9a-113">-DefaultProfile</span></span>
<span data-ttu-id="47b9a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47b9a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47b9a-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="47b9a-115">-Destination</span></span>
<span data-ttu-id="47b9a-116">Путь к соединенной позиции в Магазине данных, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="47b9a-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="47b9a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="47b9a-117">-Force</span></span>
<span data-ttu-id="47b9a-118">Указывает на то, что данной операцией можно переписать файл назначения, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="47b9a-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="47b9a-119">-Paths</span><span class="sxs-lookup"><span data-stu-id="47b9a-119">-Paths</span></span>
<span data-ttu-id="47b9a-120">Указывает массив путей к объединяемой папке Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="47b9a-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47b9a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47b9a-121">-Confirm</span></span>
<span data-ttu-id="47b9a-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47b9a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47b9a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b9a-123">-WhatIf</span></span>
<span data-ttu-id="47b9a-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47b9a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b9a-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="47b9a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47b9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b9a-126">CommonParameters</span></span>
<span data-ttu-id="47b9a-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b9a-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47b9a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b9a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47b9a-129">INPUTS</span></span>

### <span data-ttu-id="47b9a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="47b9a-130">System.String</span></span>

### <span data-ttu-id="47b9a-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="47b9a-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="47b9a-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="47b9a-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="47b9a-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="47b9a-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="47b9a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47b9a-134">OUTPUTS</span></span>

### <span data-ttu-id="47b9a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="47b9a-135">System.String</span></span>

## <span data-ttu-id="47b9a-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47b9a-136">NOTES</span></span>

## <span data-ttu-id="47b9a-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47b9a-137">RELATED LINKS</span></span>

[<span data-ttu-id="47b9a-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="47b9a-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="47b9a-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="47b9a-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="47b9a-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="47b9a-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="47b9a-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="47b9a-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="47b9a-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="47b9a-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="47b9a-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="47b9a-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


