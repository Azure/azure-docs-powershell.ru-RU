---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 5f927bd9ef64cc22eda7669e9b0d60127cf503ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214980"
---
# <span data-ttu-id="7f276-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f276-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="7f276-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f276-102">SYNOPSIS</span></span>
<span data-ttu-id="7f276-103">Удаляет файл или папку из магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f276-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7f276-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f276-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f276-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f276-105">DESCRIPTION</span></span>
<span data-ttu-id="7f276-106">Для удаления файла или папки из магазина Data Lake Store удаляется **cmdlet Remove-AzDataLakeStoreItem.**</span><span class="sxs-lookup"><span data-stu-id="7f276-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7f276-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f276-107">EXAMPLES</span></span>

### <span data-ttu-id="7f276-108">Пример 1. Удаление нескольких элементов</span><span class="sxs-lookup"><span data-stu-id="7f276-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="7f276-109">Эта команда удаляет файлы, File01.txt и File.csv из магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f276-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="7f276-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f276-110">PARAMETERS</span></span>

### <span data-ttu-id="7f276-111">-Account</span><span class="sxs-lookup"><span data-stu-id="7f276-111">-Account</span></span>
<span data-ttu-id="7f276-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f276-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7f276-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f276-113">-DefaultProfile</span></span>
<span data-ttu-id="7f276-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f276-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f276-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7f276-115">-Force</span></span>
<span data-ttu-id="7f276-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7f276-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f276-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f276-117">-PassThru</span></span>
<span data-ttu-id="7f276-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7f276-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7f276-119">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7f276-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f276-120">-Paths</span><span class="sxs-lookup"><span data-stu-id="7f276-120">-Paths</span></span>
<span data-ttu-id="7f276-121">Указывает массив путей для удаления файлов, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="7f276-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f276-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="7f276-122">-Recurse</span></span>
<span data-ttu-id="7f276-123">Указывает на то, что в ходе этой операции удаляются все элементы в целевой папке, включая вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="7f276-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f276-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f276-124">-Confirm</span></span>
<span data-ttu-id="7f276-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7f276-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f276-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f276-126">-WhatIf</span></span>
<span data-ttu-id="7f276-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f276-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f276-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f276-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f276-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f276-129">CommonParameters</span></span>
<span data-ttu-id="7f276-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f276-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f276-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f276-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f276-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f276-132">INPUTS</span></span>

### <span data-ttu-id="7f276-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7f276-133">System.String</span></span>

### <span data-ttu-id="7f276-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="7f276-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="7f276-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f276-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f276-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f276-136">OUTPUTS</span></span>

### <span data-ttu-id="7f276-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f276-137">System.Boolean</span></span>

## <span data-ttu-id="7f276-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f276-138">NOTES</span></span>

## <span data-ttu-id="7f276-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f276-139">RELATED LINKS</span></span>

[<span data-ttu-id="7f276-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f276-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="7f276-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f276-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="7f276-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f276-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="7f276-143">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f276-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="7f276-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f276-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="7f276-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f276-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


