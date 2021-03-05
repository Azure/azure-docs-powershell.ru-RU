---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: c3ce4a8051867b535ba2aff4429b5bcfa0b9ab53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010627"
---
# <span data-ttu-id="4d1e9-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d1e9-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="4d1e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1e9-103">Удаляет файл или папку из магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4d1e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4d1e9-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d1e9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d1e9-105">DESCRIPTION</span></span>
<span data-ttu-id="4d1e9-106">Для удаления файла или папки из магазина Data Lake Store удаляется **cmdlet Remove-AzDataLakeStoreItem.**</span><span class="sxs-lookup"><span data-stu-id="4d1e9-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4d1e9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4d1e9-107">EXAMPLES</span></span>

### <span data-ttu-id="4d1e9-108">Пример 1. Удаление нескольких элементов</span><span class="sxs-lookup"><span data-stu-id="4d1e9-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="4d1e9-109">Эта команда удаляет файлы, File01.txt и File.csv из магазина Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="4d1e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d1e9-110">PARAMETERS</span></span>

### <span data-ttu-id="4d1e9-111">-Account</span><span class="sxs-lookup"><span data-stu-id="4d1e9-111">-Account</span></span>
<span data-ttu-id="4d1e9-112">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4d1e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1e9-113">-DefaultProfile</span></span>
<span data-ttu-id="4d1e9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d1e9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4d1e9-115">-Force</span></span>
<span data-ttu-id="4d1e9-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d1e9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d1e9-117">-PassThru</span></span>
<span data-ttu-id="4d1e9-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4d1e9-119">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4d1e9-120">-Paths</span><span class="sxs-lookup"><span data-stu-id="4d1e9-120">-Paths</span></span>
<span data-ttu-id="4d1e9-121">Указывает массив путей к удаляемой папке Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="4d1e9-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4d1e9-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="4d1e9-122">-Recurse</span></span>
<span data-ttu-id="4d1e9-123">Указывает на то, что эта операция удаляет все элементы в целевой папке, включая вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="4d1e9-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d1e9-124">-Confirm</span></span>
<span data-ttu-id="4d1e9-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d1e9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d1e9-126">-WhatIf</span></span>
<span data-ttu-id="4d1e9-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d1e9-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d1e9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1e9-129">CommonParameters</span></span>
<span data-ttu-id="4d1e9-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d1e9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1e9-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d1e9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1e9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d1e9-132">INPUTS</span></span>

### <span data-ttu-id="4d1e9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4d1e9-133">System.String</span></span>

### <span data-ttu-id="4d1e9-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="4d1e9-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="4d1e9-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4d1e9-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4d1e9-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4d1e9-136">OUTPUTS</span></span>

### <span data-ttu-id="4d1e9-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d1e9-137">System.Boolean</span></span>

## <span data-ttu-id="4d1e9-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4d1e9-138">NOTES</span></span>

## <span data-ttu-id="4d1e9-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d1e9-139">RELATED LINKS</span></span>

[<span data-ttu-id="4d1e9-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d1e9-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="4d1e9-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d1e9-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="4d1e9-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d1e9-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="4d1e9-143">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d1e9-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="4d1e9-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d1e9-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="4d1e9-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d1e9-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


